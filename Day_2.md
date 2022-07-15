## .gitignore

> 특정 파일 혹은 폴더에 대해 Git이 버전 관리를 하지 못하도록 지정하는 것



#### .gitignore에 작성하는 목록

- 민감한 개인 정보가 담긴 파일
- OS에서 활용되는 파일
- IDE 혹은  Text editor 등에서 활용되는 파일
    - ex) python -> .idea/
- 개발 언어 혹은 프레임워크에서 사용되는 파일
    - 가상 환경: `venv/`
    - `__pycache__`



#### .gitignore 작성 시 주의 사항

- 반드시 이름을 `.gitignore`로 작성한다. 파일명 앞의 dot은 숨김 파일이라는 의미이다.
- `.gitignore` 파일은 `.git` 폴더와 동일한 위치에 생성
- 제외하고 싶은 파일은 반드시 `git add` 전에 `.gitignore`에 작성, 저장



❗ **왜 git add 전에 .gitignore에 작성해야 할까요?**

`git add a.txt` 라고 작성하면, 이제 Git은 `a.txt`를 버전 관리의 대상으로 여긴다.
한 번 버전 관리의 대상이 된 `a.txt`는 이후에 .gitignore에 작성하더라도 무시되지 않고 계속 버전 관리의 대상으로 인식된다.

따라서 제외 하고 싶은 파일은 반드시 git add 전에 .gitignore에 작성해야 한다!

#### .gitignore 쉽게 작성하기
> .gitignore의 내용을 쉽게 작성할 수 있도록 도와주는 두 개의 사이트

1. 웹 사이트: [gitignore.io](https://www.toptal.com/developers/gitignore/)
2. [gitignore 저장소](https://github.com/github/gitignore)
3. Python에 대한 .gitignore 예시
    ![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/fd7bd601-9433-418a-b08e-7b027db9a301/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220715%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220715T015931Z&X-Amz-Expires=86400&X-Amz-Signature=84ca371dcfcc57fd6e72ccddf8d1c83bdee215e5ba471df19b9caf78fe5b1124&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

## clone & pull

#### 원격 저장소 가져오기

> 지금까지는 로컬 저장소의 내용을 원격 저장소에 업로드하는 것을 학습했다.
이번에는 반대로, 원격 저장소의 내용을 로컬 저장소로 가져오는 것을 배워보자



**git clone**

- 원격 저장소의 커밋 내역을 모두 가져와서, 로컬 저장소를 생성하는 명령어

- clone은 `복제` 라는 뜻으로, `git clone` 명령어를 사용하면 원격 저장소를 통째로 복제해서 내 컴퓨터에 옮길 수 있다.

- `git clone <원격 저장소 주소>` 의 형태로 작성

  ```bash
  $ git clone https://github.com/LimSB-dev/TIL.git
  Cloning into 'TIL'...
  remote: Enumerating objects: 3, done.
  remote: Counting objects: 100% (3/3), done.
  remote: Total 3 (delta 0), reused 3 (delta 0), pack-reused 0
  Receiving objects: 100% (3/3), done.
  ```

  위에 작성한 대로 실행하면, `Github의 LimSB-dev이라는 계정의 TIL 원격 저장소를 복제`하여 내 컴퓨터에 TIL이라는 이름의 로컬 저장소를 생성하게 된다.

- git clone을 통해 생성된 로컬 저장소는 `git init` 과 `git remote add`가 이미 수행되어 있다.

#### git pull

- 원격 저장소의 변경 사항을 가져와서, 로컬 저장소를 업데이트하는 명령어

- 로컬 저장소와 원격 저장소의 내용이 완전 일치하면 git pull을 해도 변화가 일어나지 않는다.

- `git pull <저장소 이름> <브랜치 이름>`의 형태로 작성한다.

  ```bash
  $ git pull origin master
  From https://github.com/LimSB-dev/git-practice
   * branch            master     -> FETCH_HEAD
  Updating 6570ecb..56809a9
  Fast-forward
   README.md | 1 +
   1 file changed, 1 insertion(+)
  
  
  [풀이]
  git 명령어를 사용할건데, origin이라는 원격 저장소의 master 브랜치의 내용을 가져온다(pull).
  ```

 💡 **git clone vs git pull**

clone과 pull이 모두 원격 저장소로부터 가져오는 명령어라서 조금 혼동될 수 있다.

`git clone`은 git init처럼 처음에 한 번만 실행한다. 즉 로컬 저장소를 만드는 역할. 단, git init처럼 직접 로컬 저장소를 만드는 게 아니라, Github에서 저장소를 복제해서 내 컴퓨터에 똑같은 복제본을 만든다는 차이가 있다.

`git pull`은 git push처럼 로컬 저장소와 원격 저장소의 내용을 동기화하고 싶다면 언제든 사용한다. 단, push는 로컬 저장소의 변경 내용을 원격 저장소에 반영하는 것이고, pull은 원격 저장소의 변경 내용을 로컬 저장소에 반영하는 것이다. **즉 방향이 다르다!**

#### 내 컴퓨터 ↔ Github(원격 저장소) ↔ 강의장 컴퓨터

> 두 개 이상의 로컬 저장소에서 하나의 원격 저장소에 접근하면 어떻게 될까? 집과 강의장을 오가면서 `clone, push, pull` 하는 과정을 살펴보자.



**규칙**

- 수업 때는 두 개의 폴더를 `"내 컴퓨터"`와 `"강의장 컴퓨터"` 라고 가정
- 내 컴퓨터에 있는 로컬 저장소의 이름은 `TIL-home`
- 강의장 컴퓨터에 있는 로컬 저장소의 이름은 `TIL-class`
- Github에 있는 원격 저장소의 이름은 `TIL-remote`



**사전 세팅**

- 홈 디렉토리 안에 `TIL-home` 폴더를 생성

- Github에서 `TIL-remote` 라는 이름의 원격 저장소를 생성

- `TIL-home` 폴더에서 vscode를 연다.

- 아래와 같은 절차를 진행

  ```bash
  # TIL-home
  
  $ git init
  $ touch Day_1.md
  $ git add .
  $ git commit -m "집에서 Day1 작성"
  $ git remote add origin <https://github.com/LimSB-dev/TIL-remote.git>
  $ git push origin master
  ```

  `TIL-home` 로컬 저장소의 내용이 `TIL-remote` 원격 저장소에 그대로 반영된다.

- 결과

  ![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/2b2cb06c-f92a-4688-928c-a0253074c18c/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220715%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220715T025222Z&X-Amz-Expires=86400&X-Amz-Signature=32e6640a2928dc4ae3b6c0194b83a2cd4fcbc80a7a47cf59511759326f3f7c00&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

#### git clone

> 이제 강의장에 왔다 가정해보자, 현재 강의장 컴퓨터에는 TIL 폴더가 없다.

- Github에 있는 `TIL-remote`에서 `git clone`을 통해 내려 받는다.

  ```bash
  # TIL-class
  
  $ git clone <https://github.com/LimSB-dev/TIL-remote.git> TIL-class
  ```

  **원격 저장소는 `TIL-remote` 이지만, 위와 같이 작성하면 강의장 컴퓨터에는 `TIL-class`라는 이름으로 로컬 저장소가 생성된다.**

- 결과

  ![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/132461a5-d490-4417-b8e4-11d82d1a0252/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220715%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220715T034035Z&X-Amz-Expires=86400&X-Amz-Signature=bda657a244c3e81d7e0ee6f54c4a0957d22573e26265a5cdbc0c69b8671c97e9&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

#### git push

> 강의장 컴퓨터 → 원격 저장소

- 강의장에서 새로운 파일을 만들고 원격 저장소에 업로드

  ```bash
  # TIL-class
  
  $ touch day2.md
  $ git add .
  $ git commit -m "강의장에서 Day2 작성"
  $ git push origin master
  ```

- 결과

  ![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/13e9eb36-2521-41d1-9b7a-181204c8983b/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220715%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220715T034107Z&X-Amz-Expires=86400&X-Amz-Signature=f5aaf9fd7bccab826cceb2d9feab7752683ce6d5709336b2d0dd62c682b4d900&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

#### git pull

> 원격 저장소 → 내 컴퓨터

- 내 컴퓨터에는 Day_2.md가 없다. 왜냐하면 강의장 컴퓨터에서 Day_2.md를 만들어서 원격 저장소에 push 했기 때문이다. 따라서 원격 저장소에서 Day_2.md에 대한 내역을 가져와야 한다.

  ```bash
  # TIL-home
  
  $ git pull origin master
  ```

- 결과

  ![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/0ec0a1de-5218-428b-b6e7-24d9221eb1fd/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220715%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220715T034204Z&X-Amz-Expires=86400&X-Amz-Signature=a3c93b3b300a30a20d92658255eaf057f16e9c4a6df1d8124e337282d2aac7ce&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

  이제 `내 컴퓨터, Github, 강의장 컴퓨터`의 내용은 동일하다.

- **주의 사항**

  ❗ **만약 TIL-home에서 pull이 아니라 commit을 먼저한 후 pull을 하면 어떻게 될까?**

  ​	**다음 세 가지의 경우가 있을 수 있습니다.**

  1. 내 컴퓨터와 강의장 컴퓨터에서 **서로 다른 파일을 수정**한 경우 → 정상적으로 git pull
  2. 내 컴퓨터와 강의장 컴퓨터에서 **같은 파일을 수정했지만, 수정한 라인이 다른** 경우 → 정상적으로 git pull
  3. 내 컴퓨터와 강의장 컴퓨터에서 **같은 파일의 같은 라인**을 수정한 경우 → **충돌(conflict)**이 발생, 어느 내용을 반영할지 직접 선택

  

  ❗ **만약 TIL-home에서 pull이 아니라 commit을 먼저한 후 바로 push 하면 어떻게 될까?**

  **아래와 같은 에러 메시지가 나타나면서 push가 실패**

  ```BA
  To https://github.com/LimSB-dev/TIL-remote.git
  
  ! [rejected]     master -> master (non-fast-forward)
  
  error: failed to push some refs to 'https://github.com/LimSB-dev/TIL-remote.git'
  ```

  원격 저장소의 내용을 먼저 받아오지 않고, 로컬 저장소에서 새로운 커밋을 생성했기 때문에 서로의 커밋 내역이 달라져서 그렇다.

  만약 로컬 저장소와 원격 저장소의 내용이 다르다면 일단 git pull을 통해 동기화를 시키고 새로운 커밋을 쌓아 나가야 한다.
