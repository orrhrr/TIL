# git command basic

## Basic Information
- ~ :최상위 디렉토리
- 옵션은 -(하이픈)을 이용해서 사용
- 점(.)하나는 현재 디렉토리를 의미/ 점 두개는 상위 디렉토리를 의미(Ex. cd ./.. = 현재 디렉토리에서 상위디렉토리로 이동
- remove: 논리적인 삭제(실제 하드디스크에는 남아있음. 접근경로를 삭제함. 덮어쓸 파일이 있으면 덮어씀)
- delete: 물리적인 삭제(실제 하드디스크에서도 삭제함)
- 디렉토리는 삭제할 수 없다. 실제 존재하는 것이 아니라 경로이기 때문이다. 디렉토리 내 모든 파일을 지워야만 디렉토리 삭제가능
- git 사용시 프로젝트 단위(폴더)에 머물러서 작업하는게 좋다. 디렉토리를 너무 세부적으로 들어가서 작업하다가 실수할 수 있


## Basic git commands
- pwd: 현재작업 중인 디렉토리 출력 (절대경로)
- ls: 접근가능한 하위 디렉토리 표
- cd: 해당위치로 이동
- touch: 파일만들기
- mv 옮길파일명 옮길위치 :파일 옮기기, 파일 이름 변경
- cp 사본만들파일명 만들위치/사본이름지정(같은위치일경우): 사본만들기
- rm: 파일삭제
- `rm aaa.*`:aaa라는 이름이 들어간 모든 확장자를 삭제한다(모든파일삭제)
- rm -r 디렉토리: 디렉토리 내 파일 및 디렉토리까지 삭제한다.
- clear: 화면 정리하기
- vi: vim으로 들어가기(파일보기)
- cat: 텍스트 내용을 병합해서 보여준다.
- git clone 저장소주소: 저장소복제
- git add 파일명: 해당 파일을 stage area로 올림
- git commit : stage area에 있는 파일들을 commit함
- git push 저장소이름 브랜치명: 설정되어있는 respository 로 push 함
- git status -uall :파일이름까지 자세히 보여줌
- git reset HEAD 파일명: stage area 내 파일을 다시 내려놓기
- git remote rename 기존저장소명 새로운저장소명: 원격저장소명 변경


## Vim commands

- 모든키가단축키가된다.
- 특수 문자 다음엔 반드시 스페이스를 눌러야 적용된다.
- p태그 없어도 자동 문단적용됨
- 응용프로그램이 필요한 파일은 생성해도 실행할 수 없다.
- i: insert mode(입력키)
- esc: Normal mode
- :(콜론):command mode
- #: <h1></h1>같은 기능. 제목
- ##: <h2></h2>같은 기능.소제목(해시태그를 늘려서 사용가능)
- -(하이픈): <li></li>와 같은기능
- 1,2,3(숫자): <ol></ol>와 같은 기능
- [링크텍스트](링크주소)=<a href=""></a>와 같은 기능
- ![대체텍스트](이미지주소)=<img src="" alt="">와 같은기능(width와 height 지정이 불가능)
- ```사용하는언어
	이 사이에 코드 작성
  ```    
(백틱 세개타이핑 후 사용언어, 아랫줄부터 코딩, 마지막에 백틱 세개 재타이이핑)

- `$문장`: 문장 전체 강조
- 문장속`강조`: 강조<<라는 부분만 강조


## Order to use git

1. Make Repository (github)
2. Copy the Clone Code (HTTPS)
3. Type to shell [git clone clone url]
4. Type to shell [git remote -v] - repository confirm
5. Preferences to git (ex. .gitignore) - Url:gitignore.io
6. Do the task
7. Type to shell [git add file] 
stage area에파일을 올리는 이유: 작업단위가 각각 다르기 때문에 서로 다른 commit을 필요로 한다. 앞접시 같은 역할. 하나 작업하는데 연관된 여러 소스를 변경했다면 같이 묶어서 commit한다. 
8. Type to shell [git status] - stage area confirm
9. Type to shell [git commit]
10. Type to shell [git status] - commit confirm
11. If this task Doesn't have matter go push. Type to shell [git push ReopsitoryName BranchName]




## Precautions for commit

- commit 시 고려할 것
1. 시간순서
2. 작업단위별

- commit 제목은 
1. 규격을 따라서 한구절로(문장x).
2. 첫글자 대문자, 띄어쓰기 지키기.
3. 제목 및 내용은 가급적 영어로 표기.
4. 제목은 간단하게 내용은 충실하게.
5. prefix 꼭 달기
- feat: 기능개발관련
- fix: 오류 개선 혹은 버그 패치
- docs: 문서화작업
- test: test 관련
- conf: 환경설정관련
- build: 빌드관련
- ci: continuous integration 관련


