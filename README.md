# Django Jobs

## 1. 목표와 기능
Django 관련 구인정보 제공 

### 1.1 서비스 목표
-  일반 구인사이트보다 구체적인 일자리 정보 제공 

### 1.2 시스템 기능
-  

## 2. 개발 환경 및 배포 URL
### 2.1 개발 스택
- Django 5.0.3, Bootstrap 5

### 2.2 배포 URL
- [https://northeast23.github.io/Chantak](https://northeast23.github.io/Chantak/)


### 2.3 URL 구조



## 3. 메인 기능 시퀀스 다이어그램 
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

