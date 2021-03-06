---
layout: post
title: '최악의 CTO를 만났던 썰'
subtitle: '나의 가치관을 흔들었던 그사람'
date: 2019-11-14 10:46:13 -0400
background: '/img/posts/06.jpg'
---

## 인터넷에서만 보던 그 일이 실제로 일어났습니다.

흔히 인터넷에서만 떠돌던 빌런 개발자들 이야기! 남의 이야기인줄 알았습니다 그런데..

<center><img class="img-fluid" src="https://drive.google.com/uc?id=1tH1Y31mj7Qbg7X9k-FGomHNayFu3Zdve"></center><br>
<span class="caption text-muted">그게 저한테 일어날 줄 몰랐습니다.</span>

### 면접부터 느낌이 좋지 않았다

면접을 보면서부터 느낌이 싸했습니다.

```
나 : 여기 회사 안드로이드 프로젝트는 MVVM으로 적용되어있나요?
CTO : ?? 그냥 싱글톤으로 되어있을걸?
나 : 아.. (뭐지.. 잘 못 들으셨나?)
```

물론 싱글톤도 하나의 패턴이긴 한데.. 저는 아키텍처 패턴을 물어본 거였고  
저분은 생성패턴중 하나인 싱글톤을 말씀하시더라고요  
면접질문도 그냥 시리얼 통신해봤어? API 연동해봤어?  
이런 간단한 질문 몇 개로 3분만에 기술면접이 끝났습니다.

![대장금짤](https://drive.google.com/uc?id=1zyNtUris7vMdw25nhUB-D-BXfRMJUFIf 'wtf'){:.aligncenter width="300" hegith="300"}
<span class="caption text-muted">카레도 3분인데 말이죠ㅋㅋ</span>

### 안될놈은 안돼

물론 저도 부족한 거 많고 모르는 거 많지만 그래도 경력이 10년이 넘고  
CTO 위치에 있으면 알 거라고 생각했습니다. `(연차 != 실력)`  
그래서 속으로 여긴 오면 안 되겠다 생각하고 있었는데 갑자기 대표님이 들어오시더니 바로 출근했으면 좋겠다 채용할 테니 우리 이제 면접 안 봐도 괜찮지? 면접 안 본다  
이러시는 바람에 정신 차리기도 전에 알겠다고 대답을 해버렸습니다.  
(뒷이야기지만 이 회사에 출근하고 일주일 뒤 다른 회사 합격 소식을 들었고 이때가 마지막 탈출기회였지만 날려먹었죠ㅜㅜ)

<center><img class="img-fluid" src="https://drive.google.com/uc?id=1Rv6aM-IBgVHy2KoN8Y4M9ga1Unc_9F09" width="300" height="300"></center>
<span class="caption text-muted">안될놈은 안돼!</span>

### 지옥의 시작

출근 첫날 프로젝트를 열어보니 그저 웃음만 나오더군요  
변수명 a, b, c, a1, a2, a3 이런 건 기본이고 (저렇게 할 거면 주석이라도 달아놓던가)  
그 흔한 중복 클릭 처리도 안 되어있고  
개발서버 없고 CI/CD 없고 문서도 없고 아무것도 없었습니다.  
개발서버가 없다 보니 테스트도 실제 데이터로 테스트를 하는 클라스  
저 같은 쫄보는 무서워서 못하겠던데 CTO의 강심장이 부러웠습니다.ㅎㅎ  
![대장금짤](https://drive.google.com/uc?id=1U0aVSTMTLRzjR9LIZEb21bV7TetaK8Y1 'wtf'){:.aligncenter width="300" hegith="300"}

멍청했던 게 여기서 바로 탈출했어야 했는데 여기서 또 책임감과 욕심이 발동해서  
그래 내가 여기 다 바꾸면 돼! 내가 열심히 해서 안정화 시켜야겠다! 해서  
뜯어고치고 있었죠 근데 고치다 보니 이상했습니다.  
페이징 처리 없이 모든 데이터를 한 번에 내려주고 있고 이상한 데이터들도  
같이 내려오더군요 모든 통신은 GET으로만 하고..  
그래서 아 이건 서버도 다 뜯어고쳐야겠다 판단이 들어서 건의를 했죠  
그랬더니 퀄리티 좋고 잘 돌아가는데 뭘 고치냐 괜히 고치다 버그만 더 생긴다  
이러면서 거절하시더군요

![대장금짤](https://drive.google.com/uc?id=1hjB_ZY4vmiBFEiG9GZVPXyjJ2Es_tdx5 'wtf'){:.aligncenter width="400" hegith="400"}
<span class="caption text-muted">문제가 많아서 고쳐야한다고 생각이들어서 고쳐야겠다고 말한것뿐인데 왜 나대냐 하시면 ㅠㅠ </span>

> 너무 어이가없어서 이런 사람들이 많은가 하고 검색을 해보니  
> 생각보다 빌런들이 많더군요 ㅎㅎ 한번도 본적이 없고 얼굴도 모르는 분들이지만  
> 그분들이 작성했던 빌런들 후기를 보면서 동지애까지 생겼습니다. ㅎㅎㅎ

그래도 쉽게 포기할 제가 아니였죠 3개월을 설득할려고 노력했습니다.

1. 서로 다른 서비스인데 한아이디로 로그인이 가능
   - 분리시켜달라니깐 URL만 나눠줌 ㅋㅋㅋ  
     (아니 유저 테이블을 분리시키라고 임마!! 같은집에 문을 하나더 만들면 되겠냐!!)
1. 다른 서비스인데 같은 디비를 쓰다보니 다른 서비스에있는 데이터가 내려옴
   - 자기 일하기 싫어서 거절 및 하드코딩으로 그냥 구분해 시전 ㅋㅋ
1. 할부결제는되는데 할부결제취소가 안됨
   - 취소를 할려면 서버에서 할부 데이터를 내려줘야하는데 그거 만들기 귀찮다고 직접 취소하라고해를 시전하면서 거절
1. 할인을 적용하면 할인적용전 가격으로 되돌릴수 없음
   - 디비에 가격 데이터를 바꿔버려서 이거 수정할려면 손많이간다고 거절(손많이가도 컬럼 추가하라고! 일은 제대로 해야할거아냐!!)
1. API문서가 없음
   - 답답해서 제가 하나하나 물어보면서 만들었음(물론 짧게 일해서 모든 프로젝트를 다 못만들었지만)
1. 문서를 만들고 공유를해도 확인을 안함
   - 개발팀에 필요한 문서 만들어서 공유를해도 확인을 안하길래 출근,점심,퇴근전에 한번씩만 확인해달라고 간곡히 부탁드려도 영혼없는 알겠다를 시전하고 퇴사할때까지도 절대 확인안함
1. 실제 디비에 직접 접속해서 데이터수정
   - 할말이없네요 ㅎㅎ
1. 실제 서버에 붙어서 실시간으로 코드 수정
   - 이렇게 하면 안된다고 건의를 했지만 자긴 이게 편하다하면서 거절
1. 서버에 로그를 하나도 안남기던 CTO
   - 서버에 로그를 남겨야지 문제터지면 원인파악 쉽지 않겠냐했더니 이거 작업하는게 만만치가 않다면서 거절 ㅋㅋㅋ

> 이외에도 많은 일이 있습니다. 궁금하신분은 개인적으로 연락을 ㅎㅎㅎ

### 제가 졌습니다

네 3개월간의 싸움 끝에 제가 졌습니다  
절이 싫으면 중이 떠나는 게 맞다는 말도 떠오르면서 계속 이런 사람과 이런 환경에서 일하다 보면 저도 모르게 이상한 사람이 될까봐 퇴사를 결심했습니다.  
물론 회사 문제도 있습니다 4대 보험료 미납에 월급도 밀리고 ㅎㅎ

<h3 class="section-heading">마무리</h3>

후.. 저 때 생각하니 지금도 고구마 한 박스 먹은 것처럼 답답하네요 ㅎㅎ  
그래도 이번 일을 겪으면서 저의 잘못을 깨달은 게 있는데  
설득 방법이 잘못됨을 느꼈습니다. 마침 이것을 잘 표현해주는 말이 있어서  
이 말로 마무리하겠습니다. 모두 행복한 코딩 되시길 ㅎㅎ

<center>
<blockquote class="blockquote">
<q>
    배를 만들고 싶다면, 사람들을 시켜 나무를 모으고<br>
    역할을 나누고 명령을 내리면서 북을 칠 것이 아니라,<br>
    거대하고 끝없는 바다를 갈망하게 만들어라.
</q><br>
- 앙투안 드 생텍쥐베리 - <br>
</blockquote>
</center>
