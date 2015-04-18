  * 상위 항목 : [멜론(음원사이트)](%EB%A9%9C%EB%A1%A0%28%EC%9D%8C%EC%9B%90%EC%82%AC%EC%9D%B4%ED%8A%B8%29.md), [DRM](DRM.md)  

DCF란 DRM Contents File의 약자로서,
[SK텔레콤](SK%ED%85%94%EB%A0%88%EC%BD%A4.md)`[1]`에서의 합법적인 음원 다운로드 서비스 및 디지털
컨텐츠 저작권 보호를 위하여 다운로드시 [MP3](MP3.md) 파일에 [DRM](DRM.md) 기술을 적용하여 생성된
음원파일이다.  
DCF 파일은 MP3 음원에 암호 코드를 덧붙이는 방식으로 제작되며, 원본 MP3 파일과 음질의 차이가 없으며 파일 크기도 거의 동일하다.

파일에 적용된 알고리즘은 [멜론](%EB%A9%9C%EB%A1%A0%28%EC%9D%8C%EC%9B%90%EC%82%AC%EC%9D%B4%ED%8A%B8%29.md)을 위해 SKT 자체 개발한 SSE 알고리즘으로,

  * 휴대폰의 제한된 리소스에서 암/복호화를 위해 연산부담 최소화한 알고리즘
  * AES 대비 6.6배 속도  

[출처](http://redcamel.x-y.net/wikix/index.php?goto=MelonDcf)  
라는 특징을 갖고있...긴 한데 멜론이 지원되는 기기가 아닌 이상 절대 다수의 기기에서 전혀 호환 안된다. 음원파일계의
[ALZ](ALZ.md)랄까. `[2]`

[아이튠즈 스토어](%EC%95%84%EC%9D%B4%ED%8A%A0%EC%A6%88%20%EC%8A%A4%ED%86%A0%EC%96%B4.md), [벅스](%EB%B2%85%EC%8A%A4.md) 등의 음원판매 사이트들에서 DRM 자체가 없어지는 추세인데다가 최근에는
[스마트폰](%EC%8A%A4%EB%A7%88%ED%8A%B8%ED%8F%B0.md)의 유행으로 음원파일 자체를 재생 가능하다 보니 안
쓰는게 나은 편. 오히려 멜론에서 DRM-free 파일을 이용권 다운로드에 포함시키면서, 멜론무제한폰이 아닌 한 이걸 쓰는 멜론 사용자가
없을 정도다.

한때 SK텔레콤으로 출시되는 모든 단말기에 dcf를 재생할 수 있는 멜론플레이어가 탑재되긴 했는데, 이 물건은 또 멀쩡한 mp3 파일을
PC의 멜론플레이어에서 dcf로 변환한 뒤 전송해야만 재생되는 그런 물건이었다. 그나마 멜론 지원 MP3 플레이어는 그나마 나은데 휴대전화
단말기로의 전송속도는 그야말로 인내심 테스트다. 멜론플레이어는 첫 등장 당시 상당히 무거운 프로그램이었는데 변환 속도도 느린데다가 전송
속도도 느려서 그야말로 이용자를 해탈의 경지에 오르게 하는 마법의 프로그램. 당연히 SKT 소비자들에게는 욕을 바가지로 얻어먹었지만,
법원에서 이걸 쉴드쳐주는 판결을 내리면서 꿈도 희망도 없어졌다.[#](http://news.mt.co.kr/mtview.php?no=2007
122715055329795&vgb=column&columnType=&code=column121) 그러나 스마트폰의 출시로 음악을 감상하는데
있어 MP3을 그대로 넣게 할 수 있는 시스템은 SK 텔레콤 사용자들에게 그야말로 광명을 안겨주었다.

`\----`

  * `[1]` 멜론은 처음에 SKT가 런칭한 사이트다. 현 운영사인 로엔엔터테인먼트는 SKT의 자회사였다.
  * `[2]` 현재 SKT 출시 안드로이드 기기 펌웨어에는 DCF를 구동하는 DRM서버인증관련 파일이 백그라운드로 돌아간다. 그래서 순정뮤직플레이어 및 대표적인 예로 PlayerPRO라는 앱으로 DCF가 구동이 가능하다! 하지만 타 통신사는 해당 DRM관련 파일이 없기에 같은기종이라도 재생불가, 또한 넥서스나 커스텀롬을 올릴경우도 불가하다.
