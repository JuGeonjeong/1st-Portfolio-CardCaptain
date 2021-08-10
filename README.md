# __Portfolio__
## [ _Card Captain_ ] - 카드의 모든 혜택
![메인](https://user-images.githubusercontent.com/81910342/128857814-db0351c5-4e07-4032-9793-282e99b680f2.png)
***
>## ⁍ Project Info ⁌
* 프로젝트 명 : Card Captain
* 개발 기간 :  2021.06.01 ~ 2021.08.03
* 참여 인원 : 5명
* 담당 업무 : 디자인레이아웃, 로그인, 회원가입, ID/PW 찾기, My page, 관리자페이지-회원

>## ⁍ Use Technology ⁌
* 개발 환경 : <img src="https://img.shields.io/badge/Windows 10-0078D6?style=flat-square&logo=Windows&logoColor=white"/>  
* 사용 도구 : <img src="https://img.shields.io/badge/Eclipse-2C2255?style=flat-square&logo=Eclipse&logoColor=white"/> <img src="https://img.shields.io/badge/SQL Developer-F80000?style=flat-square&logo=ORACLE&logoColor=white"/>    
* 사용 기술 : <img src="https://img.shields.io/badge/JAVA-007396?style=flat-square&logo=JAVA&logoColor=white"/> <img src="https://img.shields.io/badge/JAVASCRIPT-F7DF1E?style=flat-square&logo=JAVASCRIPT&logoColor=black"/> <img src="https://img.shields.io/badge/CSS-1572B6?style=flat-square&logo=css3&logoColor=white"/> <img src="https://img.shields.io/badge/HTML-E34F26?style=flat-square&logo=HTML5&logoColor=white"/> <img src="https://img.shields.io/badge/SPRING-6DB33F?style=flat-square&logo=SPRING&logoColor=white"/> <img src="https://img.shields.io/badge/ORACLE-F80000?style=flat-square&logo=ORACLE&logoColor=white"/> <img src="https://img.shields.io/badge/JQUERY-0769AD?style=flat-square&logo=JQUERY&logoColor=white"/>

>## ⁍ Introduction ⁌
>## ⁍ Develop Detail ⁌
* 제안
  * -123
* 기획
  * 카드는 왜 필요한가?
    * 신용카드 및 체크카드의 사용 多
    * 카드 및 체크카드 소비 일상화 
    * 인터넷과 온라인 쇼핑몰 등 사업영역 발전
  * 하지만 !
    * 신용카드와 체크카드 종류는 수백가지가 존재, 그에 따른 혜택 또한 수백가지가 존재

* 디자인
  * 청결하고 안정적인 <img src="https://img.shields.io/badge/코발트블루-0047AB?style=for-the-badge&logo"/>(#0047AB)를 사용했습니다. 여러카드의 다양한 디자인들을 안정감을 더불어 돋보이게 해줍니다.
    <details>
      <summary>이미지보기👀</summary>

    |feature|Description|
    |:--:|:--:|
    |메인페이지|![스크린샷(129)](https://user-images.githubusercontent.com/81910342/128695317-ec154d4f-f5f1-4c38-84d7-8e361b9dc896.png)
    |카드사별 순위|![스크린샷(132)](https://user-images.githubusercontent.com/81910342/128695374-9338785c-10f3-464a-8a98-619d89c1ddf4.png)
    |카드 비교|![스크린샷(133)](https://user-images.githubusercontent.com/81910342/128811160-3212877a-ce00-4c7e-bd75-3aee11c24208.png)
    |전체카드순위|![스크린샷(131)](https://user-images.githubusercontent.com/81910342/128811220-5b7e736b-0ef0-432d-94a4-df3594a92118.png) ![스크린샷(137)](https://user-images.githubusercontent.com/81910342/128813314-38d65f0a-59f2-43db-9a37-11b0eb6de965.png)

  </details>

* DB설계
  * ERD - 
  * 메타데이터 - 
  * 테이블정의서 - 
    <details>
    <summary>이미지보기👀</summary>

    |feature|Description|
    |:--:|:--:|
    |ERD|![erd11](https://user-images.githubusercontent.com/81910342/128841759-c2abd214-1f6d-4b4d-bc8a-0cd65f7b518e.PNG)
    |메타데이터|![메타데이터](https://user-images.githubusercontent.com/81910342/128842663-d322d964-a2f4-46a4-81cf-ea16c90136e7.PNG)
    |테이블정의서|![1](https://user-images.githubusercontent.com/81910342/128814142-b6e959a7-6759-4c79-89c1-91559edaf6d5.PNG)  

    </details>
* 개발
  * JavaScript
    * 회원가입시 조건을 상황에 맞게 CSS처리 했습니다.
        [코드보기👀](https://github.com/financeTeamProject/CardCaptain/blob/e0ec856e17c14c7f938b45b3799f83c9797b644a/CDCP/src/main/webapp/WEB-INF/views/user/join.jsp#L265)
        <details>
        <summary>이미지보기👀</summary>

        |feature|Description|
        |:--:|:--:|
        |회원가입|![회원가입 2](https://user-images.githubusercontent.com/81910342/128839805-7bb7abce-0e3e-49e3-a538-f5642e4643f4.png)
        |ID/PW 찾기|![IDPW 찾기](https://user-images.githubusercontent.com/81910342/128840482-ea6e997a-81ab-4247-b276-c9b10c922cfc.PNG)

        
        </details>
  * Ajax를 활용한 동적Web 구현
    * 로딩된 페이지 상에서 동적으로 웹을 구현함으로써 대메뉴 이동을 제외하고는 화면의 리로드 없이 사용할 수 있도록 구현했습니다.
        <details>
        <summary>이미지보기👀</summary>

        |feature|Description|
        |:--:|:--:|
        |1|![카드사별 랭킹](https://user-images.githubusercontent.com/81910342/128833893-0f9d0215-1413-4aed-97ac-8b0b2799e0dd.png)
        |2|![스크린샷(135)](https://user-images.githubusercontent.com/81910342/128833924-35922c5e-639f-4b52-84a0-cac34b106f80.png)
        
        </details>
        
* 담당업무
  * 메인레이아웃
    <details>
 
     * 대표색상을 이용하여 Header/Footer 구조와 메인의 슬라이드를 이용하여 각종 메뉴바의 가이드를 구성했습니다.
       ![메인레이아웃](https://user-images.githubusercontent.com/81910342/128856764-a0bd32db-5870-47b5-a0bf-1e261758a75b.PNG)
 
    </details>
  * 로그인
    <details>
 
     * Header의 우측 로그인이미지를 클릭시 로그인창을 생성합니다.
        [JSP code👀](https://github.com/financeTeamProject/CardCaptain/blob/8f52920ec304a59033318ea789e8009e1f28483b/CDCP/src/main/webapp/WEB-INF/views/home.jsp#L790)
          ![로그인 1](https://user-images.githubusercontent.com/81910342/128860847-a8be7e75-7782-46fa-bd6f-f32a208fa175.PNG)
     * 입력한 ID/PW의 데이터를 form으로 DB까지 넘겨줍니다.    
        [Controller code👀](https://github.com/financeTeamProject/CardCaptain/blob/8f52920ec304a59033318ea789e8009e1f28483b/CDCP/src/main/java/com/gdj35/cdcp/WEB/user/UserContoller/UserContoller.java#L28)
        [Sql code👀](https://github.com/financeTeamProject/CardCaptain/blob/f63c2bd84256cc1d0087d98a90818f08ad3ce42e/CDCP/src/main/resources/mapper/User_SQL.xml#L4)
     * 로그인 성공, 실패
 
       |성공|실패|
       |:--:|:--:|
       |![로그인_성공](https://user-images.githubusercontent.com/81910342/128866029-30bf2359-ef1c-484e-8c9e-48a8cdcafcb2.PNG)||![로그인_실패](https://user-images.githubusercontent.com/81910342/128866685-08e37841-b417-4b75-bf33-92db50148e09.PNG)|
    </details>
  * 회원가입
  * ID/PW 찾기
  * Mypage
  * 관리자페이지-회원
  
  
* 테스트
***

