  * 관련 항목 : [밀레니엄 문제](%EB%B0%80%EB%A0%88%EB%8B%88%EC%97%84%20%EB%AC%B8%EC%A0%9C.md)  

## Contents

    

1. P 문제와 NP 문제 
2. 이해의 문제 
3. NP-난해 문제 
4. NP-완전 문제 
5. 유명한 문제 
6. 수학자들의 문제 
7. 돈의 문제 
8. 암호계의 문제 
9. 정복의 문제 
10. 여담의 문제 

[수학](%EC%88%98%ED%95%99.md)계의 [최종보스](%EC%B5%9C%EC%A2%85%20%EB%B3%B4%EC%8A%A4.md)인 [밀레니엄문제](%EB%B0%80%EB%A0%88%EB%8B%88%EC%97%84%20%EB%AC%B8%EC%A0%9C.md) 중 하나.

**P 문제와 NP문제가 같은지, 다른지를 증명**하는, 100만 달러짜리 문제.  
이 문제는 나온 지 40여년이나 지났는데도 아직 풀리지 않고 있다. <del>이 항목의 목차는 [암묵의룰](%EC%95%94%EB%AC%B5%EC%9D%98%20%EB%A3%B0.md)로 ㅇㅇ의 문제로 작성되었다.</del>

[[edit](http://rigvedawiki.net/r1/wiki.php/P-NP%20%EB%AC%B8%EC%A0%9C?action=ed
it&section=1)]

## 1. P 문제와 NP 문제 ¶

'P 문제'란 **결정론적 튜링 머신**으로 다항식 시간 내에 해결이 가능한 문제로, 간단히 말해서 요즘 쓰이는
[컴퓨터](%EC%BB%B4%ED%93%A8%ED%84%B0.md) 같은 계산장치를`[1]` 이용해 '합리적인 시간 내에'`[2]` 풀
수 있는 형태의 문제이다. 이를 테면 입력`[3]`의 크기가 '1'일 때 1초, '10'일 때 10초 ... 이런 식이라면 P(n) =
O(n)의 꼴인 다항식 형태로 시간이 기술되므로 P 문제라고 볼 수 있다. 하지만 문제의 크기가 '1'일 때 2초, '10'일 때
2^10초, '100'일 때 2^100초 ... 이런 식으로 폭발적인 증가를 한다면 P(n) = O(2^n)꼴 즉, 지수함수가 되어 다항식
형태로 나타낼 수 없으므로 P 문제가 아니다. 즉 '입력의 크기'에 따라 '문제를 풀기 위해 필요한 시간이 다항식으로 표현될 수 있느냐
아니냐'가 관건.

  

'NP 문제'란 **비결정론적 튜링 머신**이라는 장치로 다항식 시간 내에 풀 수 있는 문제를 가리킨다. 이 기계는 문제에 대한 여러 종류의
답을 동시에 검사할 수 있는 계산 장치로, 쉽게 말하면 무수히 많은 채점 전용 PC를 묶어 놓은 [크고아름다운](%ED%81%AC%EA%B3%A0%20%EC%95%84%EB%A6%84%EB%8B%A4%EC%9A%B4.md) 계산 장치라고
보면 된다. 이 장치에 무수히 많은 값을 입력한다면 장치 안에 있는 무수히 많은 채점용 PC가 각 입력값이 주어진 문제의 해답인지를 동시에
검사할 것이고, 그 중 "내 값이 정답이오!"라고 보고하는 PC가 나올 것이다. 여기까지 걸리는 시간은 앞서 언급한 "결정론적 튜링 머신"이
1개의 해답을 검사하는 시간과 같다. 즉, 비결정론적 튜링 머신으로 주어진 문제를 다항식 시간 내에 풀 수 있으려면 _결정론적 튜링 머신으로
다항식 시간 내에 주어진 답이 옳은지 틀린지를 판별해낼 수 있어야 한다._

  

정리하자면, NP 문제란 문제의 답이 Yes인 경우 답이 Yes라는 것을 다항식 시간 내에 확인할 수 있는 적당한 모범답안이 존재하는 문제를
말한다. 반대로 답이 No라는 것만을 다항식 시간 내에 확인할 수 있는 문제는 'co-NP 문제'라고 부른다.

[[edit](http://rigvedawiki.net/r1/wiki.php/P-NP%20%EB%AC%B8%EC%A0%9C?action=ed
it&section=2)]

## 2. 이해의 문제 ¶

NP 문제에 대해 쉽게 이해하기 위해서 예를 들어보자. 어떤 그래프가 주어졌을 때, "그 그래프의 모든 점을 정확하게 한 번씩만 지나는
경로가 존재하는가?" 이를 '해밀턴 경로 문제'라고 하는데, 만약 그 답이 Yes이고 모범답안으로서 그 그래프상의 모든 점을 정확하게 한
번씩만 지나는 경로가 주어진다면, '그런 경로가 존재한다'는 것을 확인할 수 있을 것이다. 즉 적절한 모범답안이 주어진 경우 Yes라는
대답은 확인할 수 있다. 따라서 '해밀턴 경로 문제 = NP 문제'이다. 그러나 그 답이 No라면, 설사 '그런 조건을 만족하지 않는
경로'가 주어진다고 하더라도 '그런 경로가 존재하지 않는다'는 것을 확인할 수는 없을 것이다. 다시 말해서 No라는 답을 다항식 시간 내에
확인할 수 있게 해 주는 종류의 모범답안은 알려져 있지 않다. 따라서 '해밀턴 경로 문제 = co-NP 문제'가 아니다. 보다 정확하게는,
'co-NP 문제'라고 증명되지 않았다. 반대로 어떤 그래프가 주어졌을 때, "그 그래프의 모든 점을 정확하게 한 번만 지나는 경로는
없는가?"라는 문제라면 이는 co-NP 문제일 것이다. `[4]`

  

  * 참고로 '[바둑](%EB%B0%94%EB%91%91.md) 같은 게임에서 필승법이 존재하는가?'는 NP 문제도 co-NP 문제도 아니다. 예컨대 [바둑](%EB%B0%94%EB%91%91.md)에서 '흑이 이기는 어떤 수순'이 주어진다고 하더라도 다른 모든 수순들을 검토해서 서로 비교하지 않는 한 그것이 '흑'에게 필승법이 존재한다는 의미인지 검증할 방법이 없다. 즉 '필승법이 존재하는가?'라는 질문에 대해서는 어떤 기보가 주어지더라도 Yes라는 대답도 No라는 대답도 다항식 시간 내에 확인할 수 없는 것이다.
  * 이와 같은 문제에서 '다항식 시간 내에' 해결 가능하다는 것은 다음과 같은 뜻이다. : 바둑판에는 19x19개의 격자가 있는데, 이 격자의 수가 x개가 있을 때, 문제 풀이에 걸리는 시간의 최대치가 x에 대한 다항식으로 주어진다는 뜻이다. 바둑판 문제의 경우에는 **대략** x!개`[5]`의 경우를 확인하게 되므로, P 문제가 아니다. 이 문제는 'EXP 완전 문제'임이 증명되어 있다. 즉 이 문제를 T의 시간 내에 풀 수 있으면 모든 지수함수적(exponential) 시간이 걸리는 문제를 'T + 다항식' 시간 내에 풀 수 있다.  

종종 NP 문제에 대해서 "P 문제가 아닌 것"으로 설명하는 경향이 있지만, P 문제는 다항식 시간 동안 '답을 찾을 수 있는' 문제이고
NP 문제는 다항식 시간 동안 '주어진 답이 맞는지 확인할 수 있는' 문제이므로 이 둘은 상호배타적인 관계가 아니다. 다항식 시간 내에 직접
답을 구할 수 있다면 당연히 주어진 답이 맞는지 역시 확인할 수 있으므로, '모든 P 문제는 NP 문제이며 그와 동시에 co-NP
문제'이기도 하다.`[6]`

  

사실 더 쉽게 설명할 수 있다. [Big-O](Big-O.md) 표시 기준으로 비결정론적 튜링머신으로 O(n^p)만큼 시간이 걸리는
문제를 결정론적 튜링머신으로 풀면 O(n^(p+q))만큼의 시간이 걸리는지, 또한 '모든 NP 문제를 이런 식으로 환원할 수 있는지를
확인'하는 것이다.`[7]` 참고로 P문제는 이미 O(n^p)이기 때문에 NP문제로 풀면 아무리 못 해도 O(n^p)는 나온다.`[8]`
이렇게 환원되는 알고리즘(그리고 문제)을 찾기 위해 지금도 많은 수학자들이 [고심하고있](%EA%B3%B5%EB%B0%80%EB%A0%88.md)지만 대부분은 명확한 답을 내놓지 못하고 있다.

  

[초한기수](%EC%B4%88%ED%95%9C%EA%B8%B0%EC%88%98.md)의 개념을 빌리자면, '알레프_0'개의 답을 동시에
검사할 수 있는 비결정론적 튜링머신에서 '알레프_0'규모의 시간복잡도가 나왔는데, 결정론적 튜링머신에 돌릴 때 '알레프_0'규모의
시간복잡도가 나오면 'P = NP'라 말할 수 있으며`[9]`, 그렇지 않은 경우`[10]`는 'P ≠ NP'라 말할 수 있는 것이다.
<del>하하, 알레프 판이네</del> 자세한 개념은 해당 항목을 볼 것. 실제로 [이런 식으로 접근하는
사람](http://libertyenvironment.com/non-fiction/mathematical-foundations/p-v-np-
resolved-in-a-decantorized-foundation-for-mathematics/)도 있긴 한데, 이 경우 **증명
불가능함이 증명된** [연속체 가설](%EC%97%B0%EC%86%8D%EC%B2%B4%20%EA%B0%80%EC%84%A4.md)과도
직결되므로, 결국 [수학 공리 자체의한계](%EB%B6%88%EC%99%84%EC%A0%84%EC%84%B1%20%EC%A0%95%EB%A6%AC.md)에 부딪힐 수 밖에
없다. 여기에 초한기수 개념을 도입한다는 것 자체가
**[알고리즘](%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98.md)의 '유한성'을 침해하는 행위**라서 주류
수학계에서 받아들이지 않고 있다. <del>100만 달러 주기 싫었나보다.</del>`[11]`

  

[[edit](http://rigvedawiki.net/r1/wiki.php/P-NP%20%EB%AC%B8%EC%A0%9C?action=ed
it&section=3)]

## 3. NP-난해 문제 ¶

모든 NP 문제를 다항식 시간 내에 어떤 문제로 환원(reduction 또는 transformation)할 수 있는 경우, 그 문제는
'NP-난해(NP-hard) 문제'라고 부른다. 즉 NP-난해 문제를 다항식 시간 내에 풀 수 있으면 모든 NP 문제를 다항식 시간 내에 풀
수 있다. 물론 NP-난해 문제는 NP 문제가 아닐 수도 있다. (즉 NP보다 풀기 어려운 문제일 수도 있다.)

  

[[edit](http://rigvedawiki.net/r1/wiki.php/P-NP%20%EB%AC%B8%EC%A0%9C?action=ed
it&section=4)]

## 4. NP-완전 문제 ¶

NP 문제들 중에서 NP-난해 문제인 것을 가리켜 'NP-완전(NP-complete) 문제'라고 부른다. NP-완전 문제를 풀 수 있으면
모든 NP 문제를 풀 수 있게 되는 셈이므로 NP 문제들 중에서는 가장 어려운 종류의 문제들인 셈이다. 위에서 예로 든 해밀턴 경로 문제도
대표적인 NP-완전 문제들 중 하나이다.

  

만약 NP-완전 문제가 P 문제라면 '모든 NP 문제가 P 문제'라는 것이 증명되는 셈이다. 바로 이것이 포인트이다. "모든 NP 문제가
사실은 P인데 우리가 변환법을 찾지 못하는 것인가?"라는 명제, 즉 'NP=P'가 옳으냐 그르냐에 대한 답을 찾는 것. 만약 NP=P라고
증명되면 그 동안의 알고리즘에 대한 연구가 완전히 바뀌는 [대격변](%EB%8C%80%EA%B2%A9%EB%B3%80.md)이
일어나므로 이 증명은 [수학](%EC%88%98%ED%95%99.md)계 뿐만이 아닌 여러 학술계열의 주목을 받고 있다.

  

참고로 '어떤 문제를 다항식 시간 내에 해결할 수 있는가 아닌가'는 '그 문제를 해결하는데 평균적으로 얼마나 시간이 걸리는가?'가 아니라
'최악의 경우(worst case)에 시간이 얼마나 걸리는가?'를 기준으로 한다. 즉 '다항식 시간 내에 해결할 수 없는 경우'가 하나라도
있으면 그것은 P 문제가 아니며, P 문제가 아니라고 생각되는 NP 문제라고 하더라도 평균적으로는 다항식 시간 내에 해결할 수도 있다.

  

[[edit](http://rigvedawiki.net/r1/wiki.php/P-NP%20%EB%AC%B8%EC%A0%9C?action=ed
it&section=5)]

## 5. 유명한 문제 ¶

  * 유명한 NP 문제 중 하나인 '거대한 자연수의 약수를 찾는 문제'의 경우를 보자. 그 자연수가 거대한 두 소수의 곱인 경우는 소인수분해를 할 방법이 알려져 있지 않다. 그러나 만약 자연수를 무작위로 뽑는 경우라면 높은 확률로 그 자연수의 약수를 적어도 하나는 찾을 수 있다. 우선 '2로 나누어질 확률'부터가 1/2이며, '2, 3, 5, 7 중 적어도 하나로 나누어질 확률'은 3/4이 넘기 때문이다. 즉 대부분의 경우에는 약수를 찾을 수 있지만 그 자연수가 거대한 두 소수의 곱인 경우에는 약수를 찾을 수 없기 때문에, (즉 약수를 찾을 수 없는 경우가 '존재'하기 때문에) 이 문제는 (현재로서는) P 문제가 아닌 것이다.  

  * 여행하는 세일즈맨 문제(Travelling Salesman Problem, TSP)의 경우 'NP-완전 문제'이지만, '무작위 알고리즘'을 이용하면 많은 경우에 비교적 높은 확률로 최적의 해답이나 그에 가까운 것을 찾을 수 있다. 그러나 무작위 알고리즘으로는 모든 경우에 항상 최적의 해답을 찾을 수 있는 것은 아니기 때문에 이 문제는 P 문제가 아니다.   

흔히 알려진 "NP 문제 = P 문제 + NP-완전 문제"라는 공식은 옳지 않다. P 문제라고도 NP-완전 문제라고도 증명되지 않은 NP
문제들도 있기 때문이다. 대표적인 것이 '거대한 자연수의 소인수분해 문제'와 '이산 로그 문제'이다. 물론 이런 문제들이 NP-완전 문제가
아니라는 것도 증명되지 않았다. 이는 당연한 일인데, 모든 NP 문제가 P 문제라면 이는 모든 P 문제가 NP-완전 문제라는 뜻도 되기
때문이다. 즉 만약 어떤 NP 문제가 NP-완전 문제가 아니라는 것이 증명되면, 그것은 'P=NP가 틀렸다'는 것에 대한 증명도 된다.

  

다만 P≠NP라고 가정하는 경우 NP-완전 문제가 아닌 NP 문제가 존재한다는 것은 증명되어 있다. 그러나 이것도 특수하게 만들어진 문제를
이용한 존재증명만이 되어 있을 뿐, P=NP가 아니라는 가정하에서도 실제로 의미가 있는 NP문제 중에서 어떠한 것도 NP-완전 문제가
아니라고 증명하지는 못하고 있다.

  

[[edit](http://rigvedawiki.net/r1/wiki.php/P-NP%20%EB%AC%B8%EC%A0%9C?action=ed
it&section=6)]

## 6. 수학자들의 문제 ¶

  

대부분의 학자들은 P=NP가 아닐 것이라고 믿는다. 이유는 간단한데, 수많은 학자들이 여러 NP 문제들에 대해서 '다항식 시간 내에 풀 수
있는 알고리즘'을 찾으려고 노력해 왔지만 전혀 성과가 없었기 때문이다. 또다른 이유로는, 임의의 명제를 증명하는 문제는 NP이고, 검증하는
문제는 P인데, 증명은 검증보다 본질적으로 어려운 문제일 것이므로 NP와 P가 같을 수 없다는 믿음이 있다. 물론 믿음과 증명은 별개이므로,
P=NP가 맞다고 믿고 있는 수학자들도 존재한다.

  

[[edit](http://rigvedawiki.net/r1/wiki.php/P-NP%20%EB%AC%B8%EC%A0%9C?action=ed
it&section=7)]

## 7. 돈의 문제 ¶

이 문제는 100만 달러가 걸린 [밀레니엄문제](%EB%B0%80%EB%A0%88%EB%8B%88%EC%97%84%20%EB%AC%B8%EC%A0%9C.md) 중 하나이다.
만약 이 문제를 푼다면, 덤으로 핵전쟁이라도 나서 인류가 다시 돌도끼 들고 뛰어다니기 전까지는 당신의 이름이 대학교 전공 교과서에 실리게 될
수 있다. 물론 'P=NP가 틀렸다'는 것을 증명했을 경우고, 만약 'P=NP가 맞다'는 것을 증명이라도 하는 날이면 대학교 교과서가 아니라
꼬꼬마들 보는 [위인전](%EC%9C%84%EC%9D%B8%EC%A0%84.md)에 당신의 이름이 실리게 될 것이다. P=NP라면
그야말로 암호계의 대격변이 일어나기 때문에.

  

[[edit](http://rigvedawiki.net/r1/wiki.php/P-NP%20%EB%AC%B8%EC%A0%9C?action=ed
it&section=8)]

## 8. 암호계의 문제 ¶

참고로 모든 [암호](%EC%95%94%ED%98%B8.md)계는 NP 문제이다.`[12]` 적어도 비밀키를 아는 사람은 해독할 수
있어야 하므로, 비밀키가 주어지는 경우 그 비밀키가 맞는지 당연히 확인할 수 있기 때문이다. 따라서 모든
[암호](%EC%95%94%ED%98%B8.md) 해독은 NP 문제일 수밖에 없고, P=NP라면 거의 모든 종류의
[암호](%EC%95%94%ED%98%B8.md)는 안전할 수 없게 된다. 그래도
[암호](%EC%95%94%ED%98%B8.md)의 사용 방법을 제한해서 비밀키 하나당
[암호](%EC%95%94%ED%98%B8.md)화를 딱 한번만 하는 [OTP](OTP.md) 등이 해결책이 되겠지만 P=NP라면
이마저도 조건이 까다로워져 평문 n 바이트를 보내려면 비밀키 n 바이트를 미리 안전한 경로로 보내야 한다.

  

[양자컴퓨터](%EC%96%91%EC%9E%90%EC%BB%B4%ED%93%A8%ED%84%B0.md)가 주목을 받는 이유는 거대한
수의 소인수분해와 이산 로그 문제라는, 암호에서 흔히 사용되는 두 NP 문제를 다항식 시간 내에 해결할 수 있기 때문이다. 그러나
양자컴퓨터라고 모든 NP 문제를 해결할 수 있는 것은 아니다. 소인수분해 문제와 이산 로그 문제를 제외한 NP 문제들, 특히 NP-완전
문제들은 현재로서는 해결할 양자 [알고리즘](%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98.md)이 없기 때문에,
지금 당장 양자컴퓨터가 실용화된다고 하더라도 대부분의 NP 문제들은 풀 수 없다.

  

[[edit](http://rigvedawiki.net/r1/wiki.php/P-NP%20%EB%AC%B8%EC%A0%9C?action=ed
it&section=9)]

## 9. 정복의 문제 ¶

참고로 국내의 김 모 교수가 대략 2003년부터 연말즈음 되면 이 문제를 풀었다고 언론에 나곤 했는데, 일단 못 풀었다가 정설이다. 다른
학자의 말에 의하면 이 문제에 대해서 제대로 인식하고 있는지 조차도 의심스럽다고. 이 문제가 컴공에서 비롯한 문제라 수학자들이 접근하기
위해서는 컴공에 관한 기반지식이 상당히 요구되는데 그런부분에서 신뢰할만하지 않다고. 실제로 관련논문은 이미 오류가 드러났다고 한다.

  

이후 2010년에는 인도계 미국인인 비나이 데오라리카가 증명했다고 주장하고 있다.[관련
기사](http://www.hankyung.com/news/app/newsview.php?aid=2010081233991) 하지만 논문
검증에 참여한 학자들은 이 논문에 오류가 있으며, 따라서 P-NP 문제 해결에 실패했을 뿐만 아니라 중요한 진전을 이룬 점조차 없다고
평가하고 있다. 사실 P-NP 문제를 해결했다는 논문은 해마다 수십 개씩 쏟아져나오고 있지만 하나같이 오류와 반례가 드러나, 아직도 별다른
진전이 없는 상태가 이어지고 있다.

  

어쨌든, 현재까지는 증명에 성공한 사람이 없다.

  

[[edit](http://rigvedawiki.net/r1/wiki.php/P-NP%20%EB%AC%B8%EC%A0%9C?action=ed
it&section=10)]

## 10. 여담의 문제 ¶

아래의 여담(?)처럼 간단하게나마 P와 NP의 차이를 설명할 수는 있다. 하지만 이건 일상적인 얘기이고, 실제로는 **수학적인 증명**을
필요로 하는지라 아래처럼 썼다가는 다른 학자들에게 논파당하거나 비웃음거리가 되니 직관적으로만 알아두자.

  

  * 수학적이 아니라 직관적으로 증명하려면, **시험 볼 때 시험 문제를 쉽게 풀 수 있는지** 를 알면 된다. <del>참 쉽죠?</del>
  * [지뢰찾기](%EC%A7%80%EB%A2%B0%EC%B0%BE%EA%B8%B0.md)를 예로 들자면, 언젠가는 여러개 중에 하나를 '찍어야 하는' 상황이 나오게 된다. 그런데 찍는다는 건 오직 비결정론적 튜링머신으로만 해결 가능하다. 결정론적 튜링머신은 읽은 데이터 하나에는 오직 하나의 명령만이 수행되기 때문이다. [난수](%EB%82%9C%EC%88%98.md)를 쓰면 해결될 수는 있으나, 컴퓨터에서 쓰이는 난수는 의사난수이므로 다시 결정론적 튜링머신의 한계로 돌아가며, 의사난수가 아닌 난수의 생성도 비결정론적 튜링머신으로만 가능하다.
  * 이미 [쿠르트 괴델](%EC%BF%A0%EB%A5%B4%ED%8A%B8%20%EA%B4%B4%EB%8D%B8.md)이 [불완전성 정리](%EB%B6%88%EC%99%84%EC%A0%84%EC%84%B1%20%EC%A0%95%EB%A6%AC.md)를 통해 튜링머신의 전신인 '괴델 수'가 불완전함을 증명한 바 있다. 훗날 [앨런 튜링](%EC%95%A8%EB%9F%B0%20%ED%8A%9C%EB%A7%81.md)도 튜링머신을 통해 불완전성 정리를 확인한 바 있다. 결국 이 문제가 **튜링머신**(그리고 '괴델 수')에 묶여 있는 한 수학적인 범위 내에서 증명하는 것은 불가능에 가깝다. 이 문제를 확실하게 증명하려면 어떻게든 수학적 계산 이외의 지식을 동원해야 한다.  

창작물에서는 [Numb3rs](Numb3rs.md)의 주인공 수학교수가 해결하려고 매달렸던 게 이 문제다. FBI 수사관인 형이
사건해결의 조언을 구하려고 하지만 정신적 충격을 겪은 주인공이 이 문제에 다시 매달려서 외부와의 소통을 완전히 차단해버려서 고생하는
에피소드도 있다.

`\----`

  * `[1]` 이는 솔직히 말해 잘못된 표현으로, 엄연히 말하자면 한 테이프의 정보를 사용, 변경하여 일을 처리하는 "가상"의 기계다. 그리고 이 기계가 바로 컴퓨터의 CPU가 하는 짓이랑 똑같아서, 컴퓨터의 능력을 테스트 하기 위해 만들어진 가상의 장치다
  * `[2]` 어디까지나 이론적으로. 1023 * n10^23같은 시간이 드는 알고리즘도 P이기 때문에 합리적이라고 취급한다. **이론적으로는.**
  * `[3]` 인스턴스라고 표현한다.
  * `[4]` 참고로 해밀턴 경로 문제가 바로 NP-완전 문제로, 이게 P 문제라는 걸 증명하거나 P 문제가 아니라는 걸 증명하면 당신은 이 문제를 해결 한 것이므로 검증 밎 여러 수순만 제대로 거치면 당신은 평생 손가락 하나 까딱 안해도 살 수 있는 부자가 된다.
  * `[5]` '대략'인 이유는 착수 금지인 자리도 있지만, 돌을 따내고 그 자리에 다시 놓는 것이 가능하기 때문.
  * `[6]` 참고로 그 역은 아직 증명도 반증도 되지 않았다. 즉 'NP 문제이면서 동시에 co-NP 문제이지만 P문제가 아닌 문제가 존재하는가' 역시 지금으로서는 알 수 없고, 몇몇 후보만 거론되고 있다.
  * `[7]` 당연히 모든 경우에서 0 ≤ q이다.
  * `[8]` 여기서 못한다는 말은 P 알고리즘을 그대로 NP에 적용하는 경우를 말하는 것이다. NP 알고리즘이라 해도 P보다 엉망으로 짜면 오히려 결과가 안 좋을 수도 있다.
  * `[9]` '알레프_0'의 자연수 제곱은 모두 '알레프_0'이다. 해당 항목의 '자연수 vs 유리수' 부분을 볼 것.
  * `[10]` 즉, '알레프_1'이나 '알레프_2' 이상 규모의 시간복잡도가 나온 경우
  * `[11]` '증명 불가능'이 증명되어도 그 결론을 이끄는 논리에 오류가 없다면 '증명'한 것으로 인정된다. 지금까지 '증명'한 학자가 없는 건 논리에 오류가 드러났기 때문.
  * `[12]` 역은 성립하지 않는다. [암호](%EC%95%94%ED%98%B8.md)계에서 사용되려면 '최악의 경우'가 아니라 '평균적인 경우'에 다항식 시간 내에 풀 수 없는 NP 문제일 필요가 있다.

