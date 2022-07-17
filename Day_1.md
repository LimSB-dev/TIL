## CLI

1. `touch`

   - 파일을 생성하는 명령어
   - 띄어쓰기로 구분하여 여러 파일을 한꺼번에 생성 가능하다.
   - 숨기 파일을 만들기 위해서는 `.`을 파일명 앞에 붙인다.

   

   ```bash
   $ touch text.txt
   ```

2. `mkdir`

   - make directory
   - 새 폴더를 생성하는 명령어
   - 띄어쓰기로 구분하여 여러 폴더를 한꺼번에 생성 가능하다.
   - 폴더 이름 사이에 공백을 넣고 싶다면 따옴표로 묶어서 입력한다.

   

   ```bash
   $ mkdir folder
   $ mkdir 'happy hacking'
   ```

3. `ls`

   - list segments
   - 현재 작업 중인 디렉토리의 폴더/파일 목록을 보여주는 명령어
   - `-a` : all 옵션. 숨김 파일까지 모두 보여준다.
   - `-l` : long 옵션. 용량, 수정 날짜 등 파일 정보를 자세히 보여준니다.

   

   ```bash
   # 기본 사용
   $ ls 
   
   # all 옵션
   $ ls -a
   
   # all, long 옵션 함께 적용
   $ ls -a -l
   
   # 여러 옵션 축약 가능
   $ ls -al
   ```

4. `mv`

   - move
   - 폴더/파일을 다른 폴더 내로 이동 하거나 이름을 변경하는 명령어
   - 단, 다른 폴더로 이동할 때는 작성한 폴더가 반드시 있어야 한다. 없으면 이름이 바뀝니다.

   

   ```bash
   # text.txt를 folder 폴더 안에 넣을 때
   $ mv text.txt folder
   
   # text1.txt의 이름을 text2.txt로 바꿀 때
   $ mv text1.txt text2.txt
   ```

5. `cd`

   - change directory
   - 현재 작업 중인 디렉토리를 변경하는 명령어
   - `cd ~` 를 입력하면 홈 디렉토리로 이동한다.
   - `cd ..` 를 입력하면 부모 디렉토리로 이동한다.
   - `cd -` 를 입력하면 바로 전 디렉토리로 이동한다.

   

   ```bash
   # 현재 작업 중인 디렉토리에 있는 folder 폴더로 이동
   $ cd folder
   
   # 절대 경로를 통한 디렉토리 변경
   $ cd C:/Users/kyle/Desktop
   
   # 상대 경로를 통한 디렉토리 변경
   $ cd ../parent/child
   ```

6. `rm`

   - remove
   - 폴더/파일 지우는 명령어
   - GUI와 달리 휴지통으로 이동하지 않고, 바로 `완전 삭제`한다.
   - `*(asterisk, wildcard)`를 사용해 `rm *.txt` 라고 입력하면 txt 파일 전체를 다 지운다.
   - `-r` : recursive 옵션. 폴더를 지울 때 사용한다.

   

   ```bash
   $ rm test.txt
   $ rm -r folder
   ```

7. `start, open`

   - 폴더/파일을 여는 명령어
   - `Windows`에서는 start를, `Mac`에서는 open을 사용할 수 있다.

   

   ```bash
   # Windows
   $ start test.txt
   
   # Mac
   $ open test.txt
   ```

8. 유용한 단축키

   - `위, 아래 방향키` : 과거에 작성했던 명령어 조회
   - `tab` : 폴더/파일 이름 자동 완성
   - `ctrl + a` : 커서가 맨 앞으로 이동
   - `ctrl + e` : 커서가 맨 뒤로 이동
   - `ctrl + w` : 커서가 앞 단어를 삭제
   - `ctrl + l` : 터미널 화면을 깨끗하게 청소 (스크롤 올리면 과거 내역 조회 가능)
   - `ctrl + insert` : 복사
   - `shift + insert` : 붙여넣기

## MarkDown

1. 제목 (Headings)

   - `h1 ~ h6` 에 해당하는 제목을 표현한다.

   - `#`을 사용한다.

   - 작성

     ```markdown
     # 제목 1
     ## 제목 2
     ### 제목 3
     #### 제목 4
     ##### 제목 5
     ###### 제목 6
     ```

   - 결과

     <img src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/b1534e2b-b67f-47d0-b966-76b3f50d09ad/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220714%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220714T145808Z&X-Amz-Expires=86400&X-Amz-Signature=80c9828b0abb4bee5af79a540a6898e485e21a8c18eefb3c3b797d916fcc368a&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject" alt="Untitled" style="zoom:200%;" />

2. 목록 (List)

   - 순서가 없는 목록과 순서가 있는 목록을 표현한다.

   - 순서가 없는 목록은 `- * +` 를 사용한다.

   - 순서가 있는 목록은 `1. 2. 3.` 과 같은 숫자를 사용한다.

   - `tab 키`를 이용해서 들여쓰기를 할 수 있다.

   - 작성

     ```markdown
     - 순서가 없는 목록
     	- 서브 목록
     	- 서브 목록
     
     + 순서가 없는 목록
     	+ 서브 목록
     	+ 서브 목록
     
     * 순서가 없는 목록
     	* 서브 목록
     	* 서브 목록
     
     1. 순서가 있는 목록
     	1. 서브 목록
     	2. 서브 목록
     
     1. 혼합 해보기 1
     	- 순서 없음
     	+ 순서 없음
     	* 순서 없음
     2. 혼합 해보기 2
     	1. 순서 있음
     	- 순서 없음
     	2. 순서 있음
     ```

   - 결과

     <img src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/00bafa7d-6880-4280-a763-e65d1c6356ca/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220714%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220714T145910Z&X-Amz-Expires=86400&X-Amz-Signature=a16fb7ebb7ad787dc14a06a634522ad4ce9ca5894fa060b8a414e5209dbb87e6&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject" alt="Untitled" style="zoom:200%;" />

3. 강조 (Emphasis)

   - 글자의 스타일링을 표현한다.

   1. **기울임** : `*글자*` 혹은 `_글자_`
   2. **굵게** : `**글자**` 혹은 `__글자__`
   3. **취소** : `~~글자~~`

   - 작성

     ```markdown
     *이탤릭체1* 
     _이탤릭체2_
     
     **볼드체1**
     __볼드체2__
     
     ~~취소선~~
     ```

   - 결과

     <img src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/77e83882-4710-4bcd-a010-8b2e88cfb543/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220714%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220714T145943Z&X-Amz-Expires=86400&X-Amz-Signature=840abe5172af38c39cfe82ada432af49c41e51cc39817693d2539fea2af2d621&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject" alt="Untitled" style="zoom:200%;" />

4. 코드 (Code)

   - 한 줄 코드인 **인라인 코드**와 여러 줄 코드인 **블록 코드**로 나눌 수 있다.

   1. 인라인(Inline) 코드 : `inline code`처럼 백틱을 통해 코드를 감싸준다.
   2. 블록(Block) 코드 : ````python` 처럼 백틱을 3번 입력하고 코드의 종류를 작성한다.

   - 작성

     ```markdown
     파이썬의 print는 `print("Hello World!")` 과 같이 사용한다.
     ```

     ```python
     for i in range(10):
     	print(i)
     ```

     ```bash
     $ touch test.txt
     ```

     ```
     Just plain text
     ```

   - 결과

     <img src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/9ced236f-5816-41e3-8cd4-677b171bea30/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220714%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220714T145959Z&X-Amz-Expires=86400&X-Amz-Signature=4b1c74eaea216a327fe4a38215a8e49e3c993a37d1ce2fd845086c6e71d29d90&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject" alt="Untitled" style="zoom:200%;" />

5. 링크 (Links)

   - 클릭하면 해당 주소로 이동할 수 있는 링크를 표현한다.

   - `[표시할 글자](이동할 주소)` 형태로 작성한다.

   - 작성

     ```markdown
     [GOOGLE](<https://google.com>)을 눌러서 구글로 이동
     ```

   - 결과

     <img src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/a9050d59-f33b-4e58-a72e-b0c7ac035c79/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220714%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220714T150017Z&X-Amz-Expires=86400&X-Amz-Signature=bed0efa9720f8fbc906bb488a47833fff4811132e7dff2025a36a90ec362c850&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject" alt="Untitled" style="zoom:200%;" />

6. 이미지 (Images)

   - 마크다운 문서에 이미지를 삽입할 수 있다.

   - `![대체 텍스트](이미지 주소)` 형태로 작성한다.

   - `대체 텍스트`란 이미지를 정상적으로 불러오지 못했을 때 표시되는 문구이다.

   - Typora에서는 이미지 파일을 끌어와서 놓아도 자동 업로드 된다.

   - 작성

     ```markdown
     Git 로고
     
     ![Git로고](<https://git-scm.com/images/logo@2x.png>)
     ```

   - 결과

     <img src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/db013257-c43f-49e6-a8f4-4ae8b915a198/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220714%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220714T150032Z&X-Amz-Expires=86400&X-Amz-Signature=dc06e160406ce8088d91ec0f37491b873d1a816c223554326d9ecc46e8122ef9&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject" alt="Untitled" style="zoom:200%;" />

7. 인용 (Blockquote)

   - 주석이나 인용 문구를 표현한다.

   - `>` 를 사용합니다. 갯수에 따라 중첩이 가능하다.

   - 작성

     ```markdown
     > 인용문을 작성
     >> 중첩된 인용문 1
     >>> 중첩된 인용문 2
     >>>> 중첩된 인용문 3
     >>>>> 중첩된 인용문 4
     ```

   - 결과

     <img src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/ae65cfd3-5a2d-49f9-bb6f-45ee987dda66/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220714%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220714T150317Z&X-Amz-Expires=86400&X-Amz-Signature=7c4fa7bf0b70b2df156ace5fbfa008f37b5f2da0c297cc9a6823eede5853d266&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject" alt="Untitled" style="zoom:200%;" />

8. 표 (Table)

   - 테이블(표)를 생성한다.

   - `파이프( | )`와 `하이픈( - )`을 이용해서 행과 열을 구분한다.

   - 테이블 양쪽 끝의 `파이프( | )`는 생략 가능한다.

   - 헤더 셀을 구분할 때는 `3개 이상의 하이픈( - )`이 필요하다.

   - Typora에서는 `ctrl + T` 를 통해서 쉽게 표 생성이 가능하다.

     (Mac은 `option + command + t`)

   - 행을 늘릴 때는 `ctrl + enter` 를 누른다.

   - 작성

     ```markdown
     | 동물   | 종류   | 다리 개수 |
     | ------ | ------ | --------- |
     | 사자   | 포유류 | 4개       |
     | 닭     | 조류   | 2개       |
     | 도마뱀 | 파충류 | 4개       |
     ```

   - 결과

     <img src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/1b8821a7-034a-4d07-a33c-6712c801d0a8/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220714%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220714T150342Z&X-Amz-Expires=86400&X-Amz-Signature=457ea5eeb17971f4f9b4306131d022755232d12a10221cc4a924773e302dbbb7&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject" alt="Untitled" style="zoom:200%;" />

9. 수평선 (Horizontal Rule)

   - 구분 선을 생성한다.

   - `- * _` 을 3번 이상 연속으로 작성한다.

   - 작성

     ```markdown
     ---
     ***
     ___
     ```

   - 결과

     <img src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/5eaf7db0-394b-406a-ae1c-c4ebdf52b905/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220714%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220714T151448Z&X-Amz-Expires=86400&X-Amz-Signature=1619a78c490ff79f27df6c4ef0767a114659b91e49e52b0a5eabb836ce627ded&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject" alt="Untitled" style="zoom:200%;" />

## Git 기초

#### Git 초기 설정

> 최초 한 번만 설정한다.
>
> 매번 Git을 사용할 때마다 설정할 필요가 없다.

1. 누가 커밋 기록을 남겼는지 확인할 수 있도록 이름과 이메일을 설정한다.

   작성자를 수정하고 싶을 때는 이름, 메일 주소만 다르게 하여 동일하게 입력한다.	

```bash
$ git config --global user.name "이름"
$ git config --global user.email "메일 주소"
```

2. 작성자가 올바르게 설정되었는지 확인 가능하다.

```bash
$ git config --global -l

또는

$ git config --global --list
```

#### Git 기본 명령어

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/7142d992-3d01-481c-9d4e-e818c6e185d8/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220714%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220714T151927Z&X-Amz-Expires=86400&X-Amz-Signature=c3c9d0f677fe25c320b6d3e338549a6639b80e25db4cd578aeae252abb2b4f01&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

- `Working Directory (= Working Tree)` : 사용자의 일반적인 작업이 일어나는 곳
- `Staging Area (= Index)` : 커밋을 위한 파일 및 폴더가 추가되는 곳
- `Repository` : staging area에 있던 파일 및 폴더의 변경사항(커밋)을 저장하는 곳
- Git은 **Working Directory → Staging Area → Repository** 의 과정으로 버전 관리를 수행한다.

#### git init

```bash
$ git init
Initialized empty Git repository in C:/Users/kyle/git-practice/.git/

kyle@KYLE MINGW64 ~/git-practice (master)
```

- 현재 작업 중인 디렉토리를 Git으로 관리한다는 명령어
- `.git` 이라는 숨김 폴더를 생성하고, 터미널에는 `(master)`라고 표기된다.
- Mac OS의 경우 `(master)`가 표기되지 않는데, Terminal 업그레이드를 통해 표기할 수 있다.


❗ **주의 사항**

1. 이미 Git 저장소인 폴더 내에 또 다른 Git 저장소를 만들지 않는다. 즉, 터미널에 이미 master가 있다면, git init을 절대 입력하면 안된다.
2. 절대로 홈 디렉토리에서 git init을 하지 않는다. 터미널의 경로가 `~` 인지 확인한다.

#### git status

```bash
$ git status
On branch master

No commits yet

nothing to commit (create/copy files and use "git add" to track)
```

- Working Directory와 Staging Area에 있는 파일의 현재 상태를 알려주는 명령어

- 어떤 작업을 시행하기 전에 수시로 status를 확인하면 좋다.

- 상태

  1. `Untracked` : Git이 관리하지 않는 파일 (한번도 Staging Area에 올라간 적 없는 파일)

  2. ```
     Tracked
     ```

      : Git이 관리하는 파일

     1. `Unmodified` : 최신 상태
     2. `Modified` : 수정되었지만 아직 Staging Area에는 반영하지 않은 상태
     3. `Staged` : Staging Area에 올라간 상태

  ![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/67719520-a1d8-4cbb-81dd-49dea429a7f4/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220714%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220714T152426Z&X-Amz-Expires=86400&X-Amz-Signature=c815769ee7b796bf7f35f869577644a25017e2c6176d9f3e9025d1cca08abfc4&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

  파일의 라이프사이클

#### git **add**

```bash
# 특정 파일
$ git add a.txt

# 특정 폴더
$ git add my_folder/

# 현재 디렉토리에 속한 파일/폴더 전부
$ git add .
```

- Working Directory에 있는 파일을 Staging Area로 올리는 명령어

- Git이 해당 파일을 추적할 수 있도록 만든다.

- `Untracked, Modified → Staged` 로 상태를 변경한다.

- 예시

  ```bash
  $ touch a.txt b.txt
  
  $ git status
  On branch master
  
  No commits yet
  
  Untracked files: # 트래킹 되고 있지 않는 파일 목록
    (use "git add <file>..." to include in what will be committed)
          a.txt
          b.txt
  
  nothing added to commit but untracked files present (use "git add" to track)
  ```

  ```bash
  # a.txt만 Staging Area에 올립니다.
  
  $ git add a.txt
  ```

  ```bash
  $ git status
  
  On branch master
  
  No commits yet
  
  Changes to be committed: # 커밋 예정인 변경사항(Staging Area)
    (use "git rm --cached <file>..." to unstage)
          new file:   a.txt
  
  Untracked files: # 트래킹 되고 있지 않은 파일
    (use "git add <file>..." to include in what will be committed)
          b.txt
  ```

#### git **commit**

```bash
$ git commit -m "first commit"
[master (root-commit) c02659f] first commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 a.txt
```

- Staging Area에 올라온 파일의 변경 사항을 하나의 버전으로 저장하는 명령어
- `커밋 메세지`는 현재 변경 사항들을 잘 나타낼 수 있도록 `의미` 있게 작성하는 것을 권장
- 각각의 커밋은 `SHA-1` 알고리즘에 의해 반환 된 고유의 해시 값을 ID로 가진다.
- `(root-commit)` 은 해당 커밋이 최초의 커밋 일 때만 표시된다. 이후 커밋부터는 사라진다.

#### **git log**

```bash
$ git log
commit 1870222981b4731d14ef91d401c68c0bbb2f6e7d (HEAD -> master)
Author: kyle <kyle123@hphk.kr>
Date:   Thu Dec 9 15:26:46 2021 +0900

    first commit
```

- 커밋의 내역(`ID, 작성자, 시간, 메세지 등`)을 조회할 수 있는 명령어
- 옵션
  - `--oneline` : 한 줄로 축약해서 보여준다.
  - `--graph` : 브랜치와 머지 내역을 그래프로 보여준다.
  - `--all` : 현재 브랜치를 포함한 모든 브랜치의 내역을 보여준다.
  - `--reverse` : 커밋 내역의 순서를 반대로 보여줍니다.
  - `-p` : 파일의 변경 내용도 같이 보여준다.
  - `-2` : 원하는 갯수 만큼의 내역을 보여준다.


💡 **옵션과 인자**

명령어를 사용하면서 `-` 혹은 `--`를 통해 옵션을 사용하는 것을 배웠다. 옵션과 더불어서 인자라는 개념도 존재하는데. 옵션과 인자 무엇이 다를까?

**옵션**은 명령어의 동작 방식을 지정하는 것이다. 따라서 **생략 가능**하다. 단순히 기존 기능보다 부가 적인 기능을 원할 때 사용한다. 예를 들면 `git log --oneline`은 커밋 내역을 한 줄로 보고 싶을 때 사용한다. `oneline` 옵션은 말 그대로 부가 적인 기능이므로, 생략해도 `git log`는 정상 동작한다.

**인자**는 명령어의 동작 대상을 지정하는 것이다. 따라서 **생략이 불가능** 하다. 예를 들면 `git add` 라고만 작성하면 어떤 파일을 Staging Area에 올릴지 모르게 된다. 반드시 `git add a.txt` 와 같이 git add 명령어가 동작할 대상을 지정해야 하는데 이때 `a.txt`와 같은 대상을 인자라고 한다.

## 원격 저장소

> 여태까지는 내 컴퓨터라는 한정된 공간에 있는 로컬 저장소에서만 버전 관리를 진행하였다. 이제는 Github의 원격 저장소를 이용해 내 컴퓨터의 로컬 저장소를 다른 사람과 공유해보자. Git의 주요 목적 중 하나인 협업을 위해 로컬 저장소의 연동 방법을 학습하자.

#### Github에서 원격 저장소 생성

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/55e28914-796f-487f-9ce1-972cf15cc1d1/%EA%B7%B8%EB%A6%BC3.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220714%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220714T234211Z&X-Amz-Expires=86400&X-Amz-Signature=47cef4e0a896a95e2a40fe35626d86d48cbc18ced900407d26bf0afbcd57e27a&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22%25EA%25B7%25B8%25EB%25A6%25BC3.png%22&x-id=GetObject)

`화면 오른쪽 상단 + 버튼을 누르고 New repository를 클릭`

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/40d4c341-35df-4cf7-8586-83afe060d56c/%EA%B7%B8%EB%A6%BC4.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220714%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220714T234506Z&X-Amz-Expires=86400&X-Amz-Signature=3e5e4e7c7fcd5e40400a98fe48ac964dacabad303f3b7375bc6c49b865ab454d&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22%25EA%25B7%25B8%25EB%25A6%25BC4.png%22&x-id=GetObject)

`저장소의 이름, 설명, 공개 여부를 선택하고 Create repository를 클릭 `

#### 로컬 저장소와 원격 저장소 연결

1. 원격 저장소가 잘 생성되었는지 확인 후, 저장소의 주소를 복사한다.

   ![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/798d21e0-9c40-4995-b5ed-fc77b9e75bb1/%EA%B7%B8%EB%A6%BC5.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220715%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220715T010410Z&X-Amz-Expires=86400&X-Amz-Signature=f9792a8c75f459a0ff6809a34076894ea79b79628e79e80b4e360e524977d4a4&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22%25EA%25B7%25B8%25EB%25A6%25BC5.png%22&x-id=GetObject)

2. 기존 실습 때 만들었던 홈 디렉토리의 TIL 폴더로 가서 vscode를 연다.

3. git init을 통해 TIL 폴더를 로컬 저장소로 만들어준다.

   ```bash
   seongbin@Lim MINGW64 ~/Desktop/TIL
   $ git init
   Initialized empty Git repository in C:/Users/seongbin/TIL/.git/
   ```

4. git remote

   로컬 저장소에 원격 저장소를 `등록, 조회, 삭제` 할 수 있는 명령어

   1. 등록

      `git remote add <이름> <주소>` 형식으로 작성한다.

      ```bash
      $ git remote add origin <https://github.com/LimSB-dev/TIL.git>
      
      [풀이]
      git 명령어를 작성할건데, remote(원격 저장소)에 add(추가) 한다.
      origin이라는 이름으로 <https://github.com/LimSB-dev/TIL.git라는> 주소의 원격저장소를 저장한다.
      ```

   2. 조회

      `git remote -v` 로 작성한다.

      ```bash
      $ git remote -v
      origin  <https://github.com/LimSB-dev/TIL.git> (fetch)
      origin  <https://github.com/LimSB-dev/TIL.git> (push)
      
      add를 이용해 추가했던 원격 저장소의 이름과 주소가 출력된다.
      ```

   3. 삭제

      `git remote rm <이름>` 혹은 `git remote remove <이름>` 으로 작성한다.

      > 로컬과 원격 저장소의 연결을 끊는 것이지, 원격 저장소 자체를 삭제하는 게 아니다.

      ```bash
      $ git remote rm origin
      $ git remote remove origin
      
      [풀이]
      git 명령어를 작성할건데, remote(원격 저장소)와의 연결을 rm(remove, 삭제) 한다.
      그 원격 저장소의 이름은 origin이다.
      ```

#### 원격 저장소에 업로드

- 실습 때 작성했던 TIL 파일을 Github 원격 저장소에 업로드 해보자.
- 정확히 말하면, 파일을 업로드하는 게 아니라 커밋을 업로드 하는 것이다.
- 따라서 먼저 로컬 저장소에서 커밋을 생성해야 원격 저장소에 업로드 할 수 있다.

1. **로컬 저장소에서 커밋 생성**

   ```bash
   # 현재 상태 확인
   $ git status
   On branch master
   No commits yet
   Untracked files:
     (use "git add <file>..." to include in what will be committed)
           day1.md
   
   nothing added to commit but untracked files present (use "git add" to track)
   ```

   ```bash
   $ git add Day_1.md
   ```

   ```bash
   $ git commit -m "Upload TIL Day1"
   [master (root-commit) f3d6d42] Upload TIL Day1
    1 file changed, 0 insertions(+), 0 deletions(-)
    create mode 100644 day1.md
   ```

   ```bash
   # 커밋 확인
   $ git log --oneline
   f3d6d42 (HEAD -> master) Upload TIL Day1
   ```

2. git push

   - 로컬 저장소의 커밋을 원격 저장소에 업로드하는 명령어
   - `git push <저장소 이름> <브랜치 이름>` 형식으로 작성한다.
   - `-u` 옵션을 사용하면, 두 번째 커밋부터는 `저장소 이름, 브랜치 이름`을 생략 가능하다.

   ```bash
   $ git push origin master
   
   [풀이]
   git 명령어를 사용할건데, origin이라는 이름의 원격 저장소의 master 브랜치에 push 한다.
   
   ------------------------------------------------
   
   $ git push -u origin master
   이후에는 $ git push 라고만 작성해도 push가 된다.
   ```

3. vscode 자격 증명

   ![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/b28d0353-708a-43eb-9e97-8cc67d03fd4f/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220715%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220715T010352Z&X-Amz-Expires=86400&X-Amz-Signature=5b78b9b1cc81d5e2c4179ec1d912812198f3700015fb9e774b3426cdf90f372c&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

   Sign in with your browser를 클릭한다.

   ![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/6dfe2042-1157-45fb-a444-3ce992a9b7fd/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220715%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220715T010336Z&X-Amz-Expires=86400&X-Amz-Signature=9c5d06191e17654958655c941ed75a355c6ff3da2d7981483ee4b1e522082258&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

   Authorize GitCredentialManager를 클릭한다.

   ![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/fd24bd5f-4b46-4618-bb90-4ab5e90cdd3e/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220715%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220715T010327Z&X-Amz-Expires=86400&X-Amz-Signature=838d06b140cc9e02cedeca6697d546092ef24b921ebeb36472461d1c8dfd31a0&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

   정상적으로 자격 증명이 완료 된다.

   이후 git push 완료

   ```bash
   $ git push -u origin master
   info: please complete authentication in your browser...
   Enumerating objects: 3, done.
   Counting objects: 100% (3/3), done.
   Writing objects: 100% (3/3), 218 bytes | 218.00 KiB/s, done.
   Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
   To <https://github.com/LimSB-dev/TIL.git>
    * [new branch]      master -> master
   Branch 'master' set up to track remote branch 'master' from 'origin'.
   ```

4. **원격 저장소에서 정상 업로드 확인**

   ![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/6d5698c4-ea50-4e47-a766-feebbd5b7a3a/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220715%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220715T010312Z&X-Amz-Expires=86400&X-Amz-Signature=68851e68099b6c6a86ecfdda467482b126fdf254dd93d29f75841047573d92c0&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

❗ **(주의) Github 원격 저장소에 절대로 파일을 드래그해서 업로드 하지 않는다!!!!**

가끔 Github를 구글 드라이브처럼 여겨서, 파일을 직접 드래그해서 올리는 경우가 있다. Git 명령어를 학습했기 때문에, 반드시 git add → git commit → git push 의 단계로만 업로드 해야한다.

그 이유는 로컬 저장소와 원격 저장소의 동기화 때문이다. 로컬 저장소에서 변경이 먼저 일어나고, 그 변경 사항을 원격 저장소에 반영하는 형태여야 한다. 하지만, Github에 드래그를 해서 파일을 업로드하면 원격 저장소에 변경이 먼저 일어나는 형태가 되기 때문에 이러한 행동을 지양해야 한다.

5. `git push`를 그림으로 이해하기

![](https://s3.us-west-2.amazonaws.com/secure.notion-static.com/357df618-2ddf-4f18-b96c-c1b0787a1a45/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220717%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220717T135009Z&X-Amz-Expires=86400&X-Amz-Signature=fef4ba8449d023c550efa28295624fcd274810701bdb2480139d8c4f8edca5d5&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject)

로컬 저장소의 commit 이력이 원격 저장소에 그대로 반영된다.
