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

     ![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1b8821a7-034a-4d07-a33c-6712c801d0a8/Untitled.png)

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

     <img src="https://s3.us-west-2.amazonaws.com/secure.notion-static.com/1b8821a7-034a-4d07-a33c-6712c801d0a8/Untitled.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Content-Sha256=UNSIGNED-PAYLOAD&X-Amz-Credential=AKIAT73L2G45EIPT3X45%2F20220714%2Fus-west-2%2Fs3%2Faws4_request&X-Amz-Date=20220714T150342Z&X-Amz-Expires=86400&X-Amz-Signature=457ea5eeb17971f4f9b4306131d022755232d12a10221cc4a924773e302dbbb7&X-Amz-SignedHeaders=host&response-content-disposition=filename%20%3D%22Untitled.png%22&x-id=GetObject" alt="Untitled" style="zoom:200%;" />