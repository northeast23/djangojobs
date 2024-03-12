# Django Jobs

## 1. 목표와 기능
Django 관련 구인정보 제공 

### 1.1 서비스 목표
-  일반 구인사이트보다 구체적인 일자리 정보 제공 

### 1.2 시스템 기능
-  

## 2. 개발 환경 및 배포 URL
### 2.1 개발 스택
- Django 5.0.3, Bootstrap 5.2.3 

### 2.2 배포 URL
- [https://northeast23.github.io/Chantak](https://northeast23.github.io/Chantak/)


### 2.3 URL 구조



## 3. 메인 기능 시퀀스 다이어그램 
### 3.1 메인 기능 
```
- 필수 구현 요구사항
    1. 메인페이지 구현
        - 페이지 제목과 블로그 입장하기 버튼이 있습니다.
        - 회원가입/로그인 버튼이 있습니다.
        - 회원가입 버튼을 클릭하면 회원가입 페이지로 이동합니다.
        - 로그인 버튼을 클릭하면 로그인 페이지로 이동합니다.
    2. 회원가입 기능 구현
        - 회원가입을 할 수 있는 페이지가 있어야합니다.
        - 입력받는 값은 id, password입니다.
    3. 로그인 기능 구현
        - 로그인을 할 수 있는 페이지가 있어야합니다.
        - 입력받는 값은 id, password입니다.
    4. **게시글 작성 기능 구현**
        - 로그인을 한 유저만 해당 기능을 사용 할 수 있습니다.
        - 게시글 제목과 내용을 작성 할 수 있는 페이지가 있어야합니다.
        - 작성한 게시글이 저장되어 게시글 목록에 보여야 합니다.
        - **사진 업로드가 가능하도록 합니다.**
        - **게시글 조회수가 올라갈 수 있도록 합니다.**
    5. 게시글 목록 기능 구현
        - 모든 사용자들이 게시한 블로그 게시글들의 제목을 확인 할 수 있습니다.
    6. 게시글 상세보기 기능 구현
        - 게시글의 제목/내용을 보는 기능입니다.
    7. 게시글 검색 기능 구현
        - 주제와 태그에 따라 검색이 가능하게 합니다.
        - 검색한 게시물은 시간순에 따라 정렬이 가능해야 합니다.
    8. 게시글 수정 기능 구현
        - 로그인을 한 유저만 해당 기능을 사용 할 수 있습니다.
        - 본인의 게시글이 아니라면 수정이 불가능합니다.
        - 게시글의 제목 또는 내용을 수정 하는 기능입니다.
        - 게시글 제목과 내용을 수정 할 수 있는 페이지가 있어야합니다.
        - 수정된 내용은 게시글 목록보기/상세보기에 반영되어야합니다.
    9. 게시글 삭제 기능 구현
        - 로그인을 한 유저만 해당 기능을 사용 할 수 있습니다.
        - 본인의 게시글이 아니라면 수정이 불가능합니다.
        - 게시글을 삭제하는 기능입니다.
        - 삭제를 완료한 이후에 게시글 목록 화면으로 돌아갑니다.
        - 삭제된 게시글은 게시글 목록보기/상세보기에서 접근이 불가능하며,
        접근 시도 시 <존재하지 않는 게시글입니다> 라는 페이지를 보여줍니다.
    10. **회원 관련 추가 기능(UI 직접 구현 필요)**
        - 비밀번호 변경기능
        - 프로필 수정
        - 닉네임 추가
    11. **댓글 기능(UI 직접 구현 필요)**
        - 댓글 추가
        - 댓글 삭제
        - 대댓글
        - 댓글 수정
```

### 3.2 시퀀스 다이어그램  
```mermaid
sequenceDiagram
    actor U as User    
    participant W as Website
    participant S as Web Server

    U->>W: Request recipe
    W->>S: Query available recipes
    S->>cGPT: API Call for recipes
    cGPT-->>S: Return answers
    S-->>W: Return data
    W-->U: Display ingredients & recipe
    
    U->>W: Sign up
    W->>S: Request user registration
    S->>D: Write user info

    U->>W: Agreed newsletter service
    W->>S: Send user info 
    S->>D: Modify user info for newsletter
    S->>U: Send mails 
```




## 4. 프로젝트 구조와 개발 일정
### 4.1 프로젝트 구조

  
![image](https://github.com/northeast23/Chantak/assets/155033413/6093f6b8-9d30-4fef-942e-e58825fc0420)
 

### 4.1 개발 일정(WBS)

```mermaid
gantt
    title job board
    dateFormat  YY-MM-DD
    excludes weekends

    section 기획 
    환경설정   :a1, 24-03-01, 1d
    사이트기획 :a2, 24-03-03, 2d

    section 프론트엔드(FE)
    chatGPT 연결 및 프롬프트 테스트 : 24-02-13, 1d
    home 화면 : 24-02-14, 1d
    로그인/로그아웃 : 24-02-15, 1d
    회원가입 페이지 : 24-02-16, 1d
    인증 접근 권한 : 24-02-19, 3d
    유저 추가 : 24-02-22, 1d
    프로필 페이지 : 24-02-23, 1d       
```

## 5. 와이어프레임 / UI / BM

### 5.1 화면 설계
![image-1](https://github.com/northeast23/Chantak/assets/155033413/41395d5e-77f5-472b-99d4-1c33470f58bb)

### 5.2 실행 화면
![home](https://github.com/northeast23/Chantak/assets/155033413/c8f86f9d-881c-4c49-b6f5-585ba971de80)


## 6. 에러와 에러 해결

