![Realtek.gif](//rv.wkcdn.net/http://rigvedawiki.net/r1/pds/Realtek/Realtek.gi
f)

[GIF image (2.82 KB)]

홈페이지 : <http://www.realtek.com.tw/>

주로 [메인보드](%EB%A9%94%EC%9D%B8%EB%B3%B4%EB%93%9C.md) 의 내장 사운드 카드나 유/무선 네트워크
칩을 만드는 [중화민국](%EC%A4%91%ED%99%94%EB%AF%BC%EA%B5%AD.md)의 회사이다. 과거에는 그래픽카드도
만들었었다.

이 회사의 사운드 칩은 독/과점을 걱정해야 할 정도로 출시된 대부분의`[1]` 메인보드와
[노트북](%EB%85%B8%ED%8A%B8%EB%B6%81.md)
[컴퓨터](%EC%BB%B4%ED%93%A8%ED%84%B0.md) 의 내장 사운드 카드로 사용되어지고 있고, 네트워크 칩도 대부분의
메인보드에 많이 사용되고 있다.

또한 안드로이드 장비의 Wi-Fi 무선 칩도 Realtek 사의 제품이 채용되고 있기도 하다.

이 회사 제품의 가장 큰 장점은 바로 **단가가 싸다** 는 점이다. 동급의 Atheros`[2]` 칩이나
[인텔](%EC%9D%B8%ED%85%94.md) 무선 칩보다 **매우** 싸다.

[이베이](%EC%9D%B4%EB%B2%A0%EC%9D%B4.md)에서 802.11n 지원 무선카드를 검색해 보면
[인텔](%EC%9D%B8%ED%85%94.md)과 Atheros 고급형의 값은 각각 20달러 근방인데, 이 회사의 칩은 6 -
9달러, 비싸봐야 11달러이다.(2013년 1월 22일 기준)

사운드 칩은 모르겠으나, 네트워크 칩의 가장 큰 단점은 바로 핑이 튀기는(즉, 네트워크가 갑자기 끊어졌다 연결되는) 현상이다. 이 현상은
특히 무선카드에서 심하여 연결이 잘 되다가 갑자기 끊어져서 대용량 파일 다운로드가 취소되든가, 온라인 게임이 끊기는 등의 문제가 발생한다.
Wi-Fi Alliance에서 인증을 받았지만 왜 이런지는 모르겠다... 이건 유선도 마찬가지다. 유선은 드라이버 버전을 많이 타는 편이라
잘 안 맞는 드라이버 버전을 설치할 경우에는 핑이 막 튄다. 이건 구버전이라서 그런 것이 아니라 최신 버전으로 설치해도 이렇다. 그나마
메인보드 제조사에서 제공하는 드라이버로 설치할 경우에는 이런 현상은 많이 줄어든다.

또한, Realtek의 Bluetooth 4.0 지원 무선칩인 RTL7823AE 의 경우, 드라이버 설치 프로그램이 Windows의 기본
언어설정을 건드리는 만행을 저지르기도 한다.

[리눅스](%EB%A6%AC%EB%88%85%EC%8A%A4.md)의 경우는 무선 칩의 드라이버가 기본 제공되지 않기도 하고, 몇몇
**공식** 드라이버는 [커널 패닉](%EC%BB%A4%EB%84%90%20%ED%8C%A8%EB%8B%89.md) 을 일으키기도
한다.  
리눅스에서 Realtek 무선 칩 드라이버를 사용하느니 차라리 소형 **USB 무선 랜카드**를 사서 사용하자. 그게 정신건강에 훨씬
덜해롭다. (실제로 누군가 2박 3일동안 개고생해서 핑이 튀는 문제를 해결했지만 그래도 불안정. 열받은 끝에 그냥 무선 랜카드를 갈아치운
사람도 있다.[#](http://luckyyowu.tistory.com/165))

리눅스를 지원하는 무선 랜카드로 IPTIME의 n100mini ([#](http://prod.danawa.com/info/?pcode=189
0786&cate1=863&cate2=895&cate3=1084&cate4=0))나 ZIO의 1570nu ([#](http://prod.da
nawa.com/info/?pcode=1485212&cate1=863&cate2=895&cate3=1084&cate4=0)) 정도가 괜찮다.
두 제품 모두 리눅스 드라이버를 지원한다.  
단 n100mini 는 리눅스 드라이버를 지원하기는 하지만 거의 불량품이나 마찬가지 수준. ZIO 제품은 잘 모르겠다.

호환성도 극악이다. 끊긴다고 공유기를 탓하기 전에 본인 노트북의 무선랜카드 칩셋부터 확인하자.(사실 같은 Realtek 공유기와 무선랜끼리는
호환이 잘된다. 하지만 다른 걸 만나는 순간...)  
업무용/일반용으로는 만점이지만, 게임이나 다른 네트워크 전문 작업을 위해서는 다른 무선카드로 바꾸는 것을 추천한다.

저 특유의 마스코트 때문에 사람들 사이에서는 꽃게칩 혹은 꽃게텍으로 통하고 있다.

![realtek.png](//rv.wkcdn.net/http://rigvedawiki.net/r1/pds/realtek.png)

[PNG image (50.44 KB)]

오디오 코덱들의 넘버링이 꽤나 혼란스러운데 대략적인 스펙은 위와 같다. <del>봐도 모르겠어요</del><del>본격 시궁창 스펙. 그러니
우리는 리얼텍을 멀리하고 외장 사운드카드와 dac를 가까히 해야합니다.</del>

`\----`

  * `[1]` [VIA](VIA.md)의 오디오 칩셋을 사용하는 제품도 상당수 있다.
  * `[2]` [퀄컴](%ED%80%84%EC%BB%B4.md)(Qualcomm)의 자회사로서, 유/뮤선 네트워크와 [블루투스](%EB%B8%94%EB%A3%A8%ED%88%AC%EC%8A%A4.md) 칩을 만든다.

