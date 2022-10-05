
### Jira에서 티켓 못찾았을때 발생하는 오류를 스킵하고 싶을 때

중간에 continue-on-error: true 한줄 추가

```
- name: Find in Jira ticket
  continue-on-error: true
  uses: atlassian/gajira-find-issue-key@master
  id: jira-ticket
  with:
  string: ${{ github.event.ref }}
```

- **true** 설정의 장점
  - 티켓을 못찾더라도 Action이 Success로 지나가기 때문에 Action에서 에러표시 나는것을 막을 수 있음
  - Jira ticket만 못찾았고 배포에는 문제가 없기 때문에 스킵하고 넘길 수 있음
  - Github action에서 에러가 나면 매우 크리티컬 이슈라고 인식 할 수 있음
- **false** 설정의 장점 (false가 default)
  - Jira 티켓 설정을 개개인이 안할수도 있음
  - Github Action에서 에러가 나니 문제를 보고 잘못 설정된 티켓을 수정 할 수 있음.
