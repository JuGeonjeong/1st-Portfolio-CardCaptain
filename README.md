# __Portfolio__
## [ _Card Captain_ ] - 카드의 모든 혜택
![메인](https://user-images.githubusercontent.com/81910342/128857814-db0351c5-4e07-4032-9793-282e99b680f2.png)
***
## ⁍ Project Info ⁌
* 프로젝트 명 : Card Captain
* 개발 기간 :  2021.06.01 ~ 2021.08.03
* 참여 인원 : 5명
* 담당 업무 : 디자인레이아웃, 로그인, 회원가입, ID/PW 찾기, My page, 관리자페이지-회원

## ⁍ Use Technology ⁌
* 개발 환경 : <img src="https://img.shields.io/badge/Windows 10-0078D6?style=flat-square&logo=Windows&logoColor=white"/>  
* 사용 도구 : <img src="https://img.shields.io/badge/Eclipse-2C2255?style=flat-square&logo=Eclipse&logoColor=white"/> <img src="https://img.shields.io/badge/SQL Developer-F80000?style=flat-square&logo=ORACLE&logoColor=white"/>    
* 사용 기술 : <img src="https://img.shields.io/badge/JAVA-007396?style=flat-square&logo=JAVA&logoColor=white"/> <img src="https://img.shields.io/badge/JAVASCRIPT-F7DF1E?style=flat-square&logo=JAVASCRIPT&logoColor=black"/> <img src="https://img.shields.io/badge/CSS-1572B6?style=flat-square&logo=css3&logoColor=white"/> <img src="https://img.shields.io/badge/HTML-E34F26?style=flat-square&logo=HTML5&logoColor=white"/> <img src="https://img.shields.io/badge/SPRING-6DB33F?style=flat-square&logo=SPRING&logoColor=white"/> <img src="https://img.shields.io/badge/ORACLE-F80000?style=flat-square&logo=ORACLE&logoColor=white"/> <img src="https://img.shields.io/badge/JQUERY-0769AD?style=flat-square&logo=JQUERY&logoColor=white"/>

## ⁍ Introduction ⁌
* ### 기획
  * 카드의 사용량이 증가하는 이유?
    * 편리함
    * 소비에 따른 다양한 혜택
    * 인터넷과 온라인 쇼핑몰 등 사업영역 발전
    * 페이의 사용량 증가
  * 하지만 !
    * 신용카드와 체크카드 종류는 수백가지가 존재, 그에 따른 혜택 또한 수백가지가 존재
    * 카드를 보유한 대부분의 사용자들은 혜택을 누리지 못함
    * 소비습관에 맞지않는 카드를 사용하는 사용자가 대다수

* ### 디자인
  * 청결하고 안정적인 <img src="https://img.shields.io/badge/코발트블루-0047AB?style=for-the-badge&logo"/>(#0047AB)를 사용, 여러카드의 다양한 디자인들을 안정감을 더불어 돋보이게 해줍니다.
    <details>
      <summary>이미지보기👀</summary>

    |feature|Description|
    |:--:|:--:|
    |메인페이지|![스크린샷(129)](https://user-images.githubusercontent.com/81910342/128695317-ec154d4f-f5f1-4c38-84d7-8e361b9dc896.png)
    |카드사별 순위|![스크린샷(132)](https://user-images.githubusercontent.com/81910342/128695374-9338785c-10f3-464a-8a98-619d89c1ddf4.png)
    |카드 비교|![스크린샷(133)](https://user-images.githubusercontent.com/81910342/128811160-3212877a-ce00-4c7e-bd75-3aee11c24208.png)
    |전체카드순위|![스크린샷(131)](https://user-images.githubusercontent.com/81910342/128811220-5b7e736b-0ef0-432d-94a4-df3594a92118.png) ![스크린샷(137)](https://user-images.githubusercontent.com/81910342/128813314-38d65f0a-59f2-43db-9a37-11b0eb6de965.png)

  </details>

## ⁍ Develop Detail ⁌


<!-- 
  * 관리자페이지-회원
 
* 테스트
-->

#### 📝 el 태그 및 jstl을 활용한 정적 web 구현
Controller → jsp 이동 시 view resolver가 view 경로 추가 및 화면 구현

>   <details>
>    
>   ![지도](https://user-images.githubusercontent.com/81910342/129653848-6e922c3e-6176-45b5-90f3-b9357faf0f57.PNG)
>   ```html
>	
>   <!-- Map html Start -->
>	<div class="slide1">
>		<div class="map_area" style="width:1600px; border-width:7px;padding:40px;margin:0 auto;">
>			<h1><span id="cardName">[${randomCard.CARD_NAME}]</span>&nbsp;<span id="cardSummary">${randomCard.CARD_SUMMARY}</span></h1><br/>
>			<c:set var="size" value="${fn:length(arr)}" />
>			<c:forEach var ="i" begin="0" end ="${size-1}">
>				<input type="button" value="${arr[i]}" onclick="sendPlace(this);" style="width:auto;padding-left:5px;padding-right:5px;" />
>			</c:forEach>
>			<input type="hidden" value="${randomCard.CARD_NO}">
>			
>			<div class="map_wrap">
>				<div id="menu_wrap" class="bg_white">
>				<div class="option">
>				<div>
>					<form onsubmit="searchPlaces(); return false;">
>						<input type="text" value="버튼을 클릭해 주세요" id="keyword" size="40" readonly="readonly" style="border-style:none;border-radius:5px;height:25px;width:350px;"> 
>						<button type="submit" id="serachButton" style="visibility: hidden;">검색하기</button>
>					</form>
>				</div>
>				</div>
>				
>				<ul id="placesList"></ul>
>				<div id="pagination"></div>
>				</div>
>				<div id="map" style="width:70%;height:100%;position:relataive;overflow:hidden;"></div>
>			</div>
>		</div><br/>
>	</div>
>	<!-- Map html End -->
>	
>   ```	
> 
>   </details>

---
#### 📝 Post 전송 방식의 Ajax를 활용한 동적 Web 구현
로딩된 페이지 상에서 동적으로 웹을 구현함으로써 화면의 리로드 없이 사용할 수 있도록 구현

>   <details>
>	
>   ![Mypage 3](https://user-images.githubusercontent.com/81910342/129684408-0d2e4748-4e65-4e31-a15b-24be27a2c99b.PNG)
>   ```java
>    
>   //회원정보 수정
>	function update() {
>		var params = $("#updateForm").serialize();
>		
>		$.ajax({
>			url: "memUpdates",
>			type: "post",
>			dataType: "json",
>			data: params,
>			success: function (res) {
>				if(res.resMsg == "success") {
>					alert("정보가 수정 되었습니다.");
>					alert("다시 로그인 해주세요.")
>					location.href = "testALogout";
>				}
>			},
>			error: function (request, status, error) {
>				console.log(error);
>			}
>		});
>	}
>	
>	//회원 탈퇴
>	function leave() {
>		var params = $("#updateForm").serialize();
>		
>		$.ajax({
>			url: "memLeave",
>			type: "post",
>			dataType: "json",
>			data: params,
>			success: function (res) {
>				if(res.resMsg == "success") {
>					alert("회원탈퇴 되었습니다.");
>					location.href = "testALogout3";
>				}
>			},
>			error: function (request, status, error) {
>				console.log(error);
>			}
>		});
>	}
>	
>	// 카드추가
>	function addcard() {
>		var params = $("#addcardlist").serialize();
>		
>		$.ajax({
>			url: "addcards",
>			type: "post",
>			dataType: "json",
>			data: params,
>			success: function (res) {
>				addLists();
>			},
>			error: function (request, status, error) {
>				console.log(error);
>			}
>		});
>	}
>	
>	// 카드리스트
>	function reloadList() {
>		var params = $("#joinCard").serialize();
>		
>		$.ajax({
>			url: "joincards",
>			type: "post",
>			dataType: "json",
>			data: params,
>			success: function (res) {
>				drawList(res.list);
>				drawPaging(res.pb);
>			},
>			error: function (request, status, error) {
>				console.log(error);
>			}
>		});
>	}
>	
>	// 목록 그리기
>	function drawList(list) {
>		var html = "";
>		// 	" +  + " : 만들어놓고 붙여넣어도 됨.
>		for(var d of list) {
>			html += "<tr cNo=\"" + d.CARD_NO + "\">";
>			html += "<td>" + "" + "</td>";
>			html += "<td class=\"a\">" + d.CARD_TYPE + "</td>";
>			html += "<td class=\"b\">" + d.CARD_NAME + "</td>";
>			html += "<td>" + "<button value=\"추가\" class=\"addbtn\" id=addbtn>추가</button>" + "</td>";
>			html += "</tr>";
>			
>		}
>		$(".list_wrap tbody").html(html);
>		
>		var lists = "";
>		
>		$(".list_wrap tr td button").on("click", function() {
>			lists = $(this).parents().parents().attr("cno");
>			console.log(lists);
>			$("#addcardlist #lists").val(lists);
>			
>			addcard();
>		});
>	}
>	
>	// 보유카드리스트
>	function addLists() {
>		var params = $("#joinCard").serialize();
>		
>		$.ajax({
>			url: "addLists",
>			type: "post",
>			dataType: "json",
>			data: params,
>			success: function (res) {
>				drawAddList(res.addlist);
>			},
>			error: function (request, status, error) {
>				console.log(error);
>			}
>		});
>	}
>	
>	// 리스트 삭제
>	function deletelist() {
>		var params = $("#cardDelete").serialize();
>		 $.ajax({
>			url: "cardDeletes",
>			type: "post",
>			dataType: "json",
>			data: params,
>			success: function (res) {
>				addLists();
>			},
>			error: function (request, status, error) {
>				console.log(error);
>			}
>		}); 
>	}
>	
>	addLists();
>	
>	// 보유카드 그리기
>	function drawAddList(addlist) {
>		var add = "";
>		console.log(addlist);
>		
>		for(var i = 0; i < addlist.length; i++){
>			add += "<tr cNo=\"" + addlist[i].CARD_NO + "\">";
>			add += "<td>" + "" + "</td>";
>			add += "<td class=\"a\">" + addlist[i].CARD_TYPE + "</td>";
>			add += "<td class=\"b\">" + addlist[i].CARD_NAME + "</td>";
>			add += "<td>" + "<button value=\"추가\" class=\"deletebtn\" id=\"deletebtn\">삭제</button>" + "</td>";
>			add += "</tr>";
>			
>		}
>		$(".add_wrap tbody").html(add);
>			
>		// 20210725
>		$(".add_wrap tr td button").on("click", function () {
>			var html = "";
>			var lists = $(this).parents().parents().attr("cno");
>			$("#cardDelete #lists").val(lists);
>			
>			deletelist();
>			//addLists();
>		});
>	}
>   
>   ```
>   </details>
	
---
#### 📝 Maven을 이용한 Spring 라이브러리 관리
로딩된 페이지 상에서 동적으로 웹을 구현함으로써 화면의 리로드 없이 사용할 수 있도록 구현

>   <details>
>    
>    ```java
>	
>	<!-- Spring -->
>	<dependency>
>		<groupId>org.springframework</groupId>
>		<artifactId>spring-context</artifactId>
>		<version>${org.springframework-version}</version>
>		<exclusions>
>			<!-- Exclude Commons Logging in favor of SLF4j -->
>			<exclusion>
>				<groupId>commons-logging</groupId>
>				<artifactId>commons-logging</artifactId>
>			</exclusion>
>		</exclusions>
>	</dependency>
>	<dependency>
>		<groupId>org.springframework</groupId>
>		<artifactId>spring-webmvc</artifactId>
>		<version>${org.springframework-version}</version>
>	</dependency>
>	<dependency>
>		<groupId>org.springframework</groupId>
>		<artifactId>spring-test</artifactId>
>		<version>${org.springframework-version}</version>
>	</dependency>
>	
>	<!-- AspectJ -->
>	<dependency>
>		<groupId>org.aspectj</groupId>
>		<artifactId>aspectjrt</artifactId>
>		<version>${org.aspectj-version}</version>
>	</dependency>
>	
>	<dependency>
>		<groupId>org.aspectj</groupId>
>		<artifactId>aspectjweaver</artifactId>
>		<version>${org.aspectj-version}</version>
>	</dependency>
>	
>	<dependency>
>		<groupId>org.aspectj</groupId>
>		<artifactId>aspectjtools</artifactId>
>		<version>${org.aspectj-version}</version>
>	</dependency>
>	
>	...
> 
>   ```
>	
>   </details>

---
#### 📝 Annotation-driven 설정을 통한 Annotation 기능 사용
주석에 의미를 부여하고 재사용성 증가

>   <details>
>    
>   ```java
>	
>   <!-- Enables the Spring MVC @Controller programming model -->
>   <annotation-driven />
> 
>   ```	
>   </details>

---
#### 📝 어노테이션 사용으로 소스 코드에 메타데이터를 보관
컴파일 타임의 체크뿐 아니라 어노테이션 API를 사용해 코드 가독성을 높여줌

>   <details>
> 
>   ```java 
> 
>	@Controller
>	public class UserListContoller {
>		@Autowired UserIListService useriListService;
>	 
>		@Autowired IPagingService iPagingService; 
>	.
>	.
>	.
>	@Service
>	public class UserListService implements UserIListService {
>		@Autowired UserIListDao useriListdao;
>	.
>	.
>	.
>	@Repository
>	public class UserListDao implements UserIListDao {
>		@Autowired 
>		public SqlSession sqlSession;
> 
>   ```
> 
>   </details>

---
#### 📝 Bean을 활용한 Paging 처리
로딩된 페이지 상에서 동적으로 웹을 구현함으로써 화면의 리로드 없이 사용할 수 있도록 구현

>   <details>
>    
>   ![페이징](https://user-images.githubusercontent.com/81910342/129672542-3bf27936-906d-4c94-b435-bdc0bc0ef0da.PNG)
> 
>   Controller ↴
>   ```java 
> 
>   // 회원 목록 리스트
>	  @RequestMapping(value="/mLists",
>	  		method = RequestMethod.POST,
>	  		produces = "text/json;charset=UTF-8")
>	  @ResponseBody
>	  public String mLists(
>	  		@RequestParam HashMap<String, String> params) throws Throwable{
>	  	ObjectMapper mapper = new ObjectMapper();
>	  	Map<String, Object> modelMap = new HashMap<String, Object>();
>	  	int page = Integer.parseInt(params.get("page"));
>	  	
>	  	// 페이징
>	  	int cnt = useriListService.mCnt(params);
>	  	PagingBean pb = iPagingService.getPagingBean(page, cnt);
>	  	
>	  	params.put("startCnt", Integer.toString(pb.getStartCount()));
>	  	params.put("endCnt", Integer.toString(pb.getEndCount()));
>	  	
>	  	// 리스트
>	  	List<HashMap<String, String>> list = useriListService.mList(params);
>	  	modelMap.put("list", list);
>	  	modelMap.put("pb", pb);
>	  	
>	  	return mapper.writeValueAsString(modelMap);
>	  }
> 
>   ```
> 
>   Paging Bean ↴
>   ```java
> 
>	public class PagingBean {
>		//페이지 게시글 시작번호
>		int startCount;
>		//페이지 게시글 종료번호
>		int endCount;
>		//마지막 페이지 번호
>		int maxPcount;
>		//현재 페이지 기준 시작 페이지 번호
>		int startPcount;
>		//현재 페이지 기준 종료 페이지 번호
>		int endPcount;
>	  
>		//Getter & Setter
>	public int getStartCount() {
>		return startCount;
>	}
>	public void setStartCount(int startCount) {
>		this.startCount = startCount;
>	}
>   .
>   .
>   .
> 
>   ```
>   
>   Paging Service ↴
>   ```java
> 
>	@Service
>	public class PagingService implements IPagingService{
>   	
>	//테이블 시작row
>	@Override
>	public int getStartCount(int page, int viewCnt) {
>		int startCount = 0;
>		startCount = (page - 1) * viewCnt + 1;
>	return startCount;
>	}
>   
>	//테이블 종료row
>	@Override
>	public int getEndCount(int page, int viewCnt) {
>		int endCount = 0;
>		endCount = page * viewCnt;
>		return endCount;
>	}
>   .
>   .
>   .
>
>	//빈형식으로 취득
>	@Override
>	public PagingBean getPagingBean(int page, int maxCount, int viewCnt, int pageCnt) {
>		PagingBean pb = new PagingBean();
> 
>		pb.setStartCount(getStartCount(page, viewCnt));
>		pb.setEndCount(getEndCount(page, viewCnt));
>		pb.setMaxPcount(getMaxPcount(maxCount, viewCnt));
>		pb.setStartPcount(getStartPcount(page, pageCnt));
>		pb.setEndPcount(getEndPcount(page, maxCount, viewCnt, pageCnt));
> 
>		return pb;
>		}
>	}
> 
>   ```
> 
>   </details>

---
#### 📝 HttpSession을 활용한 데이터정보 저장
Tomcat 서버를 활용하여 로그인 정보를 Session에 저장하여 사용

>   <details>
>    
>   ```java
>    
>   // 로그인메인
>	  @RequestMapping(value="/logins",
>	  		method = RequestMethod.POST,
>	  		produces = "text/json;charset=UTF-8")
>	  	@ResponseBody
>	  	public String login(
>	  			HttpSession session,
>	  			@RequestParam HashMap<String,String> params) throws Throwable {
>	  			System.out.println(params);
>	  		ObjectMapper mapper = new ObjectMapper();
>	  		
>	  		Map<String, Object> modelMap = new HashMap<String, Object>();
>	  		
>	  		params.put("mPw",Utils.encryptAES128(params.get("mPw")));
>	  		
>	  		HashMap<String,String> data = useriService.getM(params);
>	  		
>	  		if(data != null) {
>	  			session.setAttribute("sMNo", data.get("MEMBER_NO"));
>	  			session.setAttribute("sMId", data.get("MEMBER_ID"));
>	  			session.setAttribute("sMPw", data.get("MEMBER_PW"));
>	  			session.setAttribute("sMPw2",Utils.decryptAES128(data.get("MEMBER_PW")));
>	  			session.setAttribute("sMBi", data.get("MEMBER_BIRTH"));
>	  			session.setAttribute("sMCo", data.get("CONTACT"));
>	  			session.setAttribute("sMNm", data.get("NICKNAME"));
>	  			session.setAttribute("sMNa", data.get("E_NAME"));
>	  			session.setAttribute("sMAd", data.get("E_ADDRESS"));
>	  			
>	  			modelMap.put("resMsg", "success");
>	  			
>	  		} else {
>	  			modelMap.put("resMsg", "failed");
>	  		}
>	  	return mapper.writeValueAsString(modelMap);
>	  }
>   
>   ```
> 
>   </details>

---
#### 📝 AES 알고리즘 방식을 이용한 암호화,복호화 구현
param에 들어 있는 비밀번호 키를 AES 알고리즘 방식으로 암호화 후 재정의
	   
>   <details>
>   
>   Controller ↴
>   ```java
>	   
>   	@RequestMapping(value="/logins",
>			method = RequestMethod.POST,
>			produces = "text/json;charset=UTF-8")
>		@ResponseBody
>		public String login(
>				HttpSession session,
>				@RequestParam HashMap<String,String> params) throws Throwable {
>				System.out.println(params);
>			ObjectMapper mapper = new ObjectMapper();
>			
>			Map<String, Object> modelMap = new HashMap<String, Object>();
>			
>	                // 암호화
>			params.put("mPw",Utils.encryptAES128(params.get("mPw")));
>			
>			HashMap<String,String> data = useriService.getM(params);
>			
>			if(data != null) {
>				session.setAttribute("sMNo", data.get("MEMBER_NO"));
>				session.setAttribute("sMId", data.get("MEMBER_ID"));
>				session.setAttribute("sMPw", data.get("MEMBER_PW"));
>	                        // 복호화
>				session.setAttribute("sMPw2",Utils.decryptAES128(data.get("MEMBER_PW")));
>				session.setAttribute("sMBi", data.get("MEMBER_BIRTH"));
>				session.setAttribute("sMCo", data.get("CONTACT"));
>				session.setAttribute("sMNm", data.get("NICKNAME"));
>				session.setAttribute("sMNa", data.get("E_NAME"));
>				session.setAttribute("sMAd", data.get("E_ADDRESS"));
>				
>				modelMap.put("resMsg", "success");
>				
>			} else {
>				modelMap.put("resMsg", "failed");
>			}
>		return mapper.writeValueAsString(modelMap);
>	}	   
>	   
>   ```
>	
>   Utils ↴
>   ```java
>	
>   public class Utils {
>	
>	public static String getPrimaryKey() {
>		SimpleDateFormat formatter = new SimpleDateFormat("yyyyMMddHHmmss");
>		return formatter.format(new java.util.Date()) + RandomStringUtils.randomNumeric(6);
>	}
>	
>	public static String encryptAES128(String value) throws Throwable {
>		SecretKeySpec keySpec 
>			= new SecretKeySpec(CommonProperties.SECURE_KEY.getBytes("UTF-8"), "AES");
>
>		SecretKeySpec skeySpec = new SecretKeySpec(
>			DatatypeConverter.parseBase64Binary(
>				(String) DatatypeConverter.printBase64Binary(keySpec.getEncoded())), "AES");
>
>		Cipher cipher = Cipher.getInstance("AES");
>		cipher.init(Cipher.ENCRYPT_MODE, skeySpec);
>		byte[] encrypted = cipher.doFinal(value.getBytes());
>
>		String encodeString = DatatypeConverter.printBase64Binary(encrypted);
>
>		return encodeString;
>	}
>
>	public static String decryptAES128(String value) throws Throwable {
>		SecretKeySpec keySpec = new SecretKeySpec(CommonProperties.SECURE_KEY.getBytes("UTF-8"), "AES");
>		SecretKeySpec sKeySpec = new SecretKeySpec(
>				DatatypeConverter.parseBase64Binary(DatatypeConverter.printBase64Binary(keySpec.getEncoded())), "AES");
>
>		Cipher cipher = Cipher.getInstance("AES");
>		cipher.init(Cipher.DECRYPT_MODE, sKeySpec);
>
>		byte[] decodeBytes = DatatypeConverter.parseBase64Binary(value); //문자열 형태의 파라메터를 배열에 바이트 변환 후 삽입
>
>		byte[] decryptBytes = cipher.doFinal(decodeBytes); // 복호화
>
>		return new String(decryptBytes);
>	}
>	
>	public static HashMap<String, String> toLowerMapKey(HashMap<String, String> oldMap) throws Throwable {
>		Set<String> keySet = oldMap.keySet();
>		
>		Iterator<String> keys = keySet.iterator();
>		
>		HashMap<String, String> newMap = new HashMap<String, String>();
>		
>		while(keys.hasNext()) {
>			String key = keys.next();
>			newMap.put(key.toLowerCase(), String.valueOf(oldMap.get(key)));
>		}
>		return newMap;
>	}
>	
>	public static List<HashMap<String, String>> toLowerListMapKey(List<HashMap<String, String>> oldList) {
>		List<HashMap<String, String>> newList = new ArrayList<HashMap<String, String>>();
>		
>		for(HashMap<String, String> oldMap : oldList) {
>			Set<String> keySet = oldMap.keySet();
>			
>			Iterator<String> keys = keySet.iterator();
>			
>			HashMap<String, String> newMap = new HashMap<String, String>();
>			
>			while(keys.hasNext()) {
>				String key = keys.next();
>				newMap.put(key.toLowerCase(), String.valueOf(oldMap.get(key)));
>			}
>			newList.add(newMap);
>		}
>		return newList;
>       }
>   }
>	   
>   ```
> 
>   </details>

---
#### 📝 Ansi SQL 사용으로 쿼리의 가독성 확보
테이블간 관계가 FROM에서 명시 및 WHERE에서 조건 확인

>   <details>
>    
>   ```sql
>	   
>	<select id="getDCredit" parameterType="hashmap" resultType="hashmap">
>		SELECT C.CARD_NO, C.CARD_CMP_NO, C.CARD_CMP_NAME, C.CARD_NAME, C.CARD_SUMMARY, 
>            	       C.CARD_IMG_URL, C.CLICK_CNT, C.RNK
>		FROM(SELECT C.*, CMP.CARD_CMP_NAME,
>		           ROW_NUMBER() OVER(ORDER BY CLICK_CNT DESC) AS RNK 
>		     FROM CARDS C INNER JOIN CARDCOMPANYS CMP
>		                          ON  C.CARD_CMP_NO = CMP.CARD_CMP_NO
>		                          AND CARD_TYPE = 0) C 
>		WHERE C.RNK BETWEEN 1 AND 10
>	</select>
>		
>	<select id="getDCheck" parameterType="hashmap" resultType="hashmap">
>		SELECT C.CARD_NO, C.CARD_CMP_NO, C.CARD_CMP_NAME, C.CARD_NAME, C.CARD_SUMMARY, 
>            	       C.CARD_IMG_URL, C.CLICK_CNT, C.RNK
>		FROM(SELECT C.*, CMP.CARD_CMP_NAME,
>		           ROW_NUMBER() OVER(ORDER BY CLICK_CNT DESC) AS RNK 
>		     FROM CARDS C INNER JOIN CARDCOMPANYS CMP
>		                          ON  C.CARD_CMP_NO = CMP.CARD_CMP_NO
>		                          AND CARD_TYPE = 1) C 
>		WHERE C.RNK BETWEEN 1 AND 10
>	</select>
>	   
>   ```
> 
>   </details>

---
#### 📝 MyBatis에서 Dynamic SQL 사용으로 쿼리의 재사용 및 쿼리 최소화
조건문을 사용해 중복되는 쿼리를 최소화

>   <details>
>    
>   ```sql
>	   
>	<select id="checklistKeyword" parameterType="ArrayList" resultType="hashmap">
>		SELECT CARD_NO, CARD_NAME, CARD_KIND, CARD_TYPE, BENEFIT_TOP, CARD_IMG_URL
>		FROM(SELECT C.CARD_NO,C.CARD_NAME,DECODE(C.CARD_TYPE, 0, '신용카드','체크카드') AS CARD_KIND,
>					CASE WHEN T.CARD_TYPE = 0 THEN '할인'
>						 WHEN T.CARD_TYPE = 1 THEN '적립'
>						 ELSE '마일리지'
>					END AS CARD_TYPE, B.BENEFIT_TOP,C.CARD_IMG_URL
>				FROM CARDS C INNER JOIN CARDBENEFITS B ON C.CARD_NO = B.CARD_NO
>							 INNER JOIN CARDTYPES T ON B.CARD_NO = T.CARD_NO
>							  AND C.DEL_CHECK=1) A
>		<if test="kind == '' and type == '' and benefit == ''">
>			WHERE 1 = 1
>		</if>
>		<if test="kind != '' or type != '' or benefit != ''">
>			WHERE 1!= 1
>		</if>
>		<if test="kind != ''">
>			OR CARD_KIND IN (${kind})
>		</if>
>		<if test="type != ''">
>			OR CARD_KIND IN (${type})
>		</if>
>		<if test="benefit != ''">
>			OR CARD_KIND IN (${benefit})
>		</if>
>		ORDER BY CARD_NO
>	</select>
>	   
>   ```
> 
>   </details>

---
#### 📝 Git을 통한 협업
Git을 활용하여 팀 작업을 진행 및 파트별 개발을 통한 개발 일정 단축

>   <details>
>    
>   ![Mypage](https://user-images.githubusercontent.com/81910342/129649089-c6e3b25a-af83-4c59-bd4a-fcfac2c03bd9.PNG)
>   [JSP code👀](https://github.com/financeTeamProject/CardCaptain/blob/421e8fefd6c32b0b905de34620262caa0778fc48/CDCP/src/main/webapp/WEB-INF/views/user/mypage.jsp#L683)
> 
>   </details>

---
#### 📝 DB설계
	
>   <details>
>
>   |feature|Description|
>   |:--:|:--:|
>   |ERD|![erd11](https://user-images.githubusercontent.com/81910342/128841759-c2abd214-1f6d-4b4d-bc8a-0cd65f7b518e.PNG)
>   |메타데이터|![메타데이터](https://user-images.githubusercontent.com/81910342/128842663-d322d964-a2f4-46a4-81cf-ea16c90136e7.PNG)
>   |테이블정의서|![1](https://user-images.githubusercontent.com/81910342/128814142-b6e959a7-6759-4c79-89c1-91559edaf6d5.PNG)  
> 
>   </details>

---
#### 📝 테스트
각 페이지별 테스트 케이스 설계 및 시나리오 작성 후 테스트 케이스 기반의 통합 테스트 수행	
>   <details>
>   
>   ![테스트](https://user-images.githubusercontent.com/81910342/129709364-a230f0ca-843f-49e3-b458-9e1fc2d14251.PNG)
> 
>   </details>

---
<!--	   
### 담당업무
  <details>
 
  * 메인레이아웃
    <details>
 
     * 대표색상 <img src="https://img.shields.io/badge/코발트블루-0047AB?style=flat-square&logo"/>를 이용하여 Header/Footer 구조와 메인의 슬라이드를 이용하여 각종 메뉴바의 가이드를 구성했습니다.
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
       ![성공,실패](https://user-images.githubusercontent.com/81910342/128869210-97652983-78a5-4a89-aa08-68a431ae2c2f.PNG)
 
    </details>
  * 회원가입
    <details>
 
      * 모든 조건 만족시 '가입완료'버튼이 활성화 됩니다.
      * 이메일 인증 - 입력한 이메일로 랜덤코드 전송, 코드 일치시 가입가능합니다.
        [JSP code👀](https://github.com/financeTeamProject/CardCaptain/blob/f63c2bd84256cc1d0087d98a90818f08ad3ce42e/CDCP/src/main/webapp/WEB-INF/views/user/join.jsp#L268)
        [Controller code👀](https://github.com/financeTeamProject/CardCaptain/blob/421e8fefd6c32b0b905de34620262caa0778fc48/CDCP/src/main/java/com/gdj35/cdcp/WEB/user/UserContoller/UserContoller.java#L98)
 
        ![스크린샷(139)](https://user-images.githubusercontent.com/81910342/129216959-97ab7cea-a04e-471c-aba1-08f0e9c5d861.png)

    </details>
  * ID/PW 찾기
    <details>
 
      * 모든 조건 만족시 아이디와 비밀번호를 알려줍니다.
      * 이메일 인증 - '비밀번호 찾기'는 이메일 인증을 해줍니다.
        [JSP code👀](https://github.com/financeTeamProject/CardCaptain/blob/f63c2bd84256cc1d0087d98a90818f08ad3ce42e/CDCP/src/main/webapp/WEB-INF/views/user/searchmem.jsp#L291)
        [Controller code👀](https://github.com/financeTeamProject/CardCaptain/blob/421e8fefd6c32b0b905de34620262caa0778fc48/CDCP/src/main/java/com/gdj35/cdcp/WEB/user/UserContoller/UserContoller.java#L137)
 
    ![스크린샷(140)](https://user-images.githubusercontent.com/81910342/129218093-5ffcb60b-b989-4e8f-b1cf-af81638e156d.png)

    </details>
  * Mypage
    <details>
 
      * update를 사용하여 회원정보 변경을 할 수 있습니다.
        [JSP code👀](https://github.com/financeTeamProject/CardCaptain/blob/f63c2bd84256cc1d0087d98a90818f08ad3ce42e/CDCP/src/main/webapp/WEB-INF/views/user/mypage.jsp#L683)
        [Controller code👀](https://github.com/financeTeamProject/CardCaptain/blob/421e8fefd6c32b0b905de34620262caa0778fc48/CDCP/src/main/java/com/gdj35/cdcp/WEB/user/UserContoller/UserListContoller.java#L137)
 
      * 카드사별 카드목록 데이터를 불러오고 추가,삭제를 할 수 있습니다.
        [JSP code👀](https://github.com/financeTeamProject/CardCaptain/blob/f63c2bd84256cc1d0087d98a90818f08ad3ce42e/CDCP/src/main/webapp/WEB-INF/views/user/mypage.jsp#L818)
        [Controller code👀](https://github.com/financeTeamProject/CardCaptain/blob/421e8fefd6c32b0b905de34620262caa0778fc48/CDCP/src/main/java/com/gdj35/cdcp/WEB/user/UserContoller/UserListContoller.java#L27)
 
      ![Mypage](https://user-images.githubusercontent.com/81910342/129218150-7ea9f8c3-006b-403d-92c9-8768a3fd3242.PNG)

      </details>
  </details>
-->
