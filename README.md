# 데이트팝 레포지토리 양식

## 프로젝트 설명

## 실행방법

## 배포방법

## Git commit 방법

## Github action SECRET KEY 설정

Github -> Settings -> Secrets -> Actions -> New repository secret


### Slack

- PR_SLACK_WEBHOOK: 슬랙 보낼 채널의 웹훅 주소

위 설정을 한다면
- PR 생성 시 슬랙으로 알림이 감.

### Jira

- JIRA_BASE_URL: jira의 주소
- JIRA_USER_EMAIL: jira에서 사용하는 이메일
- JIRA_API_TOKEN: jira에서 위 이메일로 생성한 API token

위의 설정은 노션 페이지에 정리되어있음. 이 [페이지](https://www.notion.so/10fingers/Jira-API-Key-e17da0fbe0ce40d39781055ac3b153cc) 공유 금지.

위 설정을 한다면
- 새 브랜치를 만든다면 관련된 지라 티켓을 찾아서 ToDo -> InProgress로 옮겨줌.
- develop이나 release브랜치로 PR이 머지된다면 InProgress -> Done로 옮겨줌.


## Github action 관련 추가 기능

[여기](https://github.com/datepop/template/blob/main/docs/github_action.md)에서 확인!