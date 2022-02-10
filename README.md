<p align="center">  
<h1 align="middle">:moneybag:  자바 콘솔 프로젝트 - SYBANK  :moneybag:</h1>
<p align="center">
<img src="https://user-images.githubusercontent.com/97592294/153452773-453e144c-9abe-4c25-b10e-c1d20a9f0507.png" width="800" />
</p>


</p>
<br>
<p align="middle">저의 첫번째 팀 프로젝트,</p>
<p align="center">계좌관리 등 은행 업무 서비스를 제공하는</p>
<h3 align="center"> 여기는 <b>쌍용은행</b>입니다! </h3>

<br><br><br><br><br><br>

<h2 align="middle"> 🙋‍♀️ 쌍용은행을 만든 사람들 🙋‍♂️</h2>
<p align="center">
  
| [혜림]  |  [기현]  |   [한빈]      |  [규준]  | [혜인]   | [성현]   |
| :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: | 
| <img src="https://user-images.githubusercontent.com/43840561/129164013-2a88c2e7-1a93-4cc7-bbd8-c5818f5152c7.png"/> | <img src="https://user-images.githubusercontent.com/44080404/133540314-639cc580-1aa5-4bf4-8d54-b435bfe5e5f8.png" /> | <img src="https://user-images.githubusercontent.com/44080404/133540309-ae1e774e-4404-4801-bb5c-0037eab41818.PNG" /> | <img src="https://user-images.githubusercontent.com/44080404/133540317-20da5664-aa3d-4afb-809b-a7d4780a5a17.png" /> |  <img src="https://user-images.githubusercontent.com/44080404/133540321-7f8f4215-3e01-4f21-88e3-90d608377aab.png" /> | <img src="https://user-images.githubusercontent.com/44080404/133540503-22c158d4-1042-4e7c-9ee5-79c694bf5841.png" /> |

</p>

<br><br><br><br><br><br>

<p align="center">
<h2 align="middle"> 프로젝트 개요 및 환경 👨‍💻 </h2>
<br>
<h3>1. 프로젝트 개요</h3>
· 은행에 가입하여 예금하고 적금/펀드상품 가입 및 기타 추가업무를 할 수 있는 프로그램<br>
· 본 프로그램을 이용하여 은행 관리자로서 회원관리, 은행상품관리를 수행할 수 있는 프로그램<br>

<h3>2. 프로젝트 환경</h3>
· Windows 10<br>
· Mac OS<br>
· JAVA JDK 11.0.12<br>
· Eclipse IDE for Enterprise Java Developers<br>
<br><br><br><br><br><br>

<h2 align="middle"> 데이터 설계 🎡 </h2>
<br>
<h3>· 데이터 분석 및 자료형</h3>
<img src="https://user-images.githubusercontent.com/97592294/153457314-7b6fa72f-2225-4dbc-a681-d5acf76aeba0.png">
<br><br><br><br><br><br>

<h2 align="middle"> 나의 담당 업무 🎯 </h2>
<br>
<h3>· 쌍용은행 메인 화면</h3><br>
<img src="https://user-images.githubusercontent.com/97592294/153452773-453e144c-9abe-4c25-b10e-c1d20a9f0507.png" width="500" />
<h4>1. 쌍용은행의 메인 화면을 구현했습니다.</h4>
<h4>2. 메인 화면 선택에 따라 다른 결과 페이지를 도출합니다.</h4>
<pre>
<code>
try { if (sel.equals("1")) { clearScreen(); Login.main(args); clearScreen();} 
else if (sel.equals("2")) { clearScreen(); 
System.out.println("쌍용은행을 이용해주셔서 감사합니다.");
System.exit(0);
clearScreen();} 
else { loop = false;}
} catch (Exception e) { e.printStackTrace(); }
</code>
</pre>
<br>
<h3>· 로그인 화면</h3><br>
<img src="https://user-images.githubusercontent.com/97592294/153458680-f51e7d58-c73f-4f37-aa21-ceb4f8889b43.png" width="500" />
<h4>1. 쌍용은행의 로그인 화면을 구현했습니다.</h4>
<h4>2. 로그인 입력 값을 받아 일치하면 로그인이 완료됩니다.</h4>
<pre>
<code>
try {
				if (sel.equals("1")) {
					clearScreen();
					UserLogin.login();
					clearScreen();
				} else if (sel.equals("2")) {
					clearScreen();
					System.out.println();
					ManagerLogin.Login();
					clearScreen();
				} else if (sel.equals("3")) {
					clearScreen();
					Join.userjoin();
					clearScreen();
				} else if (sel.equals("4")) {
					clearScreen();
					FindID.id();
					clearScreen();
				} else if (sel.equals("5")) {
					clearScreen();
					FindPW.pw();
					clearScreen();
				} else if (sel.equals("6")) {
					System.out.println("쌍용은행을 이용해주셔서 감사합니다.");
					System.exit(0);
				} else {
					loop = false;
				}
			} catch (Exception e) {
				e.printStackTrace();
			}
</code>
</pre>
<br>
<h3>· 아이디 찾기 화면</h3><br>
<img src="https://user-images.githubusercontent.com/97592294/153458672-f8f69229-e499-46a3-9a1c-759b179911b5.png" width="500" />
<h4>1. 아이디 찾기 서비스를 구현했습니다.</h4>
<h4>2. 회원의 정보를 입력 받아 해당 아이디를 찾아주는 서비스 입니다.</h4>
<pre>
<code>
		while (check) {
			System.out.print("이름 (2~5자 이내) : ");
			name = scan.nextLine();
			if (usernameCheck(name)) { continue;} break; }
		while (check) {
			System.out.print("주민등록번호 (13자 이내) : ");
			jumin = scan.nextLine();
			if (userjuminCheck(jumin)) { continue;} break; }
		System.out.println();
		BufferedReader reader = new BufferedReader(new FileReader(MyPath.USERDATA));
		String line = null;
		
		boolean flag = false;
		
		while ((line = reader.readLine()) != null) {
			
			String[] temp = line.split(",");
			
			if (name.equals(line.split(",")[3]) && jumin.equals(line.split(",")[4])) {
				flag = true;
				break;
			} 
		}
		
		if (flag) {
			pause("회원님의 아이디는 " + line.split(",")[1] + "입니다.");
			Login.main(null);
			clearScreen();
		} else {
			pause("!아이디 찾기 실패 : 이름과 주민등록번호를 다시 입력해주세요.");
			clearScreen();
		}
</code>
</pre>
<br>
<h3>· 비밀번호 찾기 화면</h3><br>
<img src="https://user-images.githubusercontent.com/97592294/153458683-f2ef4f4f-56bf-4520-9e22-1d333c5f1b83.png" width="500" />
<h4>1. 비밀번호 찾기 서비스를 구현했습니다.</h4>
<h4>2. 아이디 찾기와 마찬가지로 정보를 입력 받아  while문으로 확인 후 찾아주는 서비스입니다.</h4>
<pre>
<code>
while (check) {
			System.out.print("아이디 (4~16자 이내) : ");
			id = scan.nextLine();
			if (userIDCheck(id)) { continue;} break; }
		while (check) {
			System.out.print("주민등록번호 (13자 이내) : ");
			jumin = scan.nextLine();
			if (userjuminCheck(jumin)) { continue;} break; }
		System.out.println();
		BufferedReader reader = new BufferedReader(new FileReader(MyPath.USERDATA));
		String line = null;
		
		boolean flag = false;
		
		while ((line = reader.readLine()) != null) {
			
			String[] temp = line.split(",");
			
			if (id.equals(line.split(",")[1]) && jumin.equals(line.split(",")[4])) {
				flag = true;
				break;
			} 
		}
</code>
</pre>
<br>
<h3>· 회원가입 화면</h3><br>
<img src="https://user-images.githubusercontent.com/97592294/153458676-1d4a8037-679f-4df7-a687-bac18ef96470.png" width="500" />
<h4>1. 회원가입 창을 구현했습니다.</h4>
<h4>2. regex를 이용하여 유효성 검사 코드를 간소화 하였습니다.</h4>
<pre>
<code>
private static boolean usertelCheck(String tel) {
		
		String regex = "^\\d{3}-\\d{3,4}-\\d{4}$";
		Pattern p = Pattern.compile(regex);
		Matcher m = p.matcher(tel);
		
		if (!m.find()) {
			pause("전화번호는 형식에 맞게 입력해주세요.\n ex) 010-1234-5678");
			return true;
		}
</code>
</pre>
<br>

<br><br><br><br><br><br>

<h2 align="middle"> ⚙️ 기술 스택 ⚙️ </h2>
<br>
<div align="middle">
<img src="https://img.shields.io/badge/Java-3178C6?style=flat-square&logo=Java&logoColor=white"/>
<img src="https://img.shields.io/badge/Eclipse IDE-000000?style=flat-square&logo=Next.Eclipse IDE&logoColor=white"/><br/>
</div>

<br><br><br><br><br><br>
