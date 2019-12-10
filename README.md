# TestExam

# 서버 사용방법

##  회원가입
신규 유저의 등록
+ ### 요청

    + #### [POST] /users/signup
    
    + #### 전달값

    <pre>
    {
        'username':'hongildong',
        'password':'hong123',
        'name':'홍길동'
    }
    </pre>

    form-data 샘플

    |키|값|
    |-|-|
    |username|hongildong|
    |password|hong123|
    |name|홍길동|

+ ### 결과

    + #### 성공
    <pre>
    {
        '_id':'1234567890',
        'username':'hongildong',
        'password':'hong123'
        'name':'홍길동'
        'salt':'asdfasdfasdf'
    }
    </pre>

    + #### 실패
    <pre>
    {
        'message':'400 Bad Request'
    }

## 로그인
+ ### 요청

    + #### [POST] /users/login

    <pre>
    {
        'username':'hongildong',
        'password':'hong123',
    }
    </pre>

+ ### 결과

    + #### 성공
        <pre>
        {
            '_id':'1234567890',
            'username':'hongildong',
            'name':'홍길동'
        }
        </pre>

        + #### 실패
    <pre>
    {
        'message':'400 Bad Request'
    }