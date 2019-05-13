## Git Usage Guide

*[Reference Posts - Psyche](https://medium.com/@psychet_learn)*

*[Reference Page - Guide](https://github.com/KennethanCeyer/tutorial-git#clap-%EC%8B%9C%EC%9E%91%ED%95%98%EB%A9%B0)*

*[Reference Post - along with process '토끼와 거북이'](<https://milooy.wordpress.com/2017/06/21/working-together-with-github-tutorial/>)*

**깃허브(GitHub)는 분산 버전 관리 툴인 **깃(Git)을 사용하는 프로젝트를 지원하는 웹호스팅 서비스이다.



**Github Usage Purpose**

- 빠른 협업환경 조성
- 누가, 언제, 무엇을, 왜, 어떻게 수정했는지 코드리뷰가 가능
- 이슈트래커(Issue Tracker) 지원
- 깃헙(GitHub)을 이용하여 자신의 git을 쉽게 공유 가능
- 지속적인 통합(Continuous Integration) 지원
- Visual Studio, JetBrains IntelliJ, Android Studio 등 대부분의 IDE에서 git 연동 제공



**GitHub Role**

- 소스 병합(merge, rebase)
- 소스 리비전 관리(reset, commit, branch)
- 소스 릴리즈(push)
- 소스 태깅(tag)
- 소스 변경사항 검토(diff, log)



**GitHub Overall**

Clone -



**How to update Repository**

- **Set Environment** : 처음 시작하는 것이라면 git의 config 과정을 진행해야 합니다.

  1. `git config` 명령어를 이용하여 계정에 대한 정보를 설정합니다.

     ```
     $ git config --global user.name "Kenneth"
     $ git config --global user.email "kenneth@pigno.se"
     ```

  2. git은 초기에 `git init`작업을 진행합니다.(GitHub에서 clone을 받은 경우엔 이 작업이 필요하지 않습니다.); 이제 git remote를 할 수 있습니다.

     ```
     $ git init
     ```

  3. git 리모트 URL을 이용하여 원격저장소에 저장된 파일을 컴퓨터로 복사해올 수 있습니다.

     ```
     $ git remote add origin https://github.com/KennethanCeyer/tutorial.git
     ```

  4. 이때 `git clone` 명령어를 사용하여 복사를 시작합니다.

     ```
     $ git clone https://github.com/KennethanCeyer/tutorial.git
     ```

  5. `git clone`을 통해 원격파일을 복사해오면, `origin` 에는 기본적으로 클론해온 리모트 URL이 저장되있습니다.

  6. git 연결을 보다 안전하고 빠르게 하기 위해서는 [`SSH Key`](https://git-scm.com/book/ko/v1/Git-%EC%84%9C%EB%B2%84-SSH-%EA%B3%B5%EA%B0%9C%ED%82%A4-%EB%A7%8C%EB%93%A4%EA%B8%B0) 등록을 권장합니다.

  

- **FAC**(Frequently-Asked-Codes)

  - **git clone** : 저장소 (로컬컴퓨터로) 가져오기. git init까지 자동으로 설정된다.

    ```
    git clone <URL>.git
    ```

  - **git remote** : 저장소 URL 설정하기

    - 저장소 추가/삭제/수정

      ```
      # 저장소 추가
      git remote add <저장소 이름> <추가할URL>.git
      # 저장소 삭제
      git remote remove <저장소 이름>
      # 저장소 수정
      git remote set-url <저장소 이름> <수정된URL>.git
      ```

  - **git status** : 상태확인; 현재 저장소에 있는 내용과 로컬 컴퓨터에 있는 내용이 얼마나 다른지에 대해서 알려주는 명령어

  - **git add(Staged상태) / git commit** : 수정사항 확정하기

    - 수정된 (전체)파일 저장소에 올리기 / add한 파일들을 저장소에 올릴 것을 확정

      ```
      # 이 단계에서 git status 명령 호출시, 수정사항이 '빨간색'으로 표시됨
      # 수정된 파일을 저장소에 올릴 준비
      git add <file name>
      # 수정된 전체 파일을 저장소에 올릴 준비
      git add *
      # ignore 파일이나, 삭제한 파일 이력까지 커밋을 하실 경우, -f 옵션을 이용합니다.
      
      # 이 단계에서 git status 명령 호출시, 수정사항이 '초록색'으로 표시됨
      # add 시킨 수정된 파일을 저장소에 올릴 것을 확정
      git commit -m "commit detail contents" # 몇개의 파일이 얼마나 수정됐는지 출력됨.(저장소 반영 전, 로컬컴퓨터에서만 확정됨)
      ```

      - `-m` 옵션을 이용하여 커밋 메시지를 작성하는 것을 권장합니다.

      - 실수로 커밋을 하여, 다시 커밋을 할 경우 커밋을 덮어씌울 수 있습니다. 이때 `--amend` 옵션을 이용합니다.

        ```
        $ git add <file name>
        $ git add *
        $ git commit -m "UI 레이아웃 이슈 수정."
        
        # 수정사항 발생
        $ git add *
        $ git commit -m "UI 레이아웃 이슈 수정 및 관리자 벨리데이션 추가." --amend
        ```

        

  - **git push** : 수정사항을 저장소에 반영하기

    ```
    git push <저장소 이름> master
    ```

  - **git pull** : **수정된** 저장소 내용 불러오기 (전체내용불러오기 X); 공동작업시 유용; '초록색 +' : 어떤 파일이 얼마나 최신화 되었는지 나타내 줍니다. 

    ```
    git pull <저장소 이름> master
    ```

  - 



