# 🐹 MONEY MENTOR
### 금융 상품 비교 어플리케이션

<!-- 주석처리 -->
<!-- ### 삼성 SW 아카데미 팀 프로젝트
#### 금융 상품 비교 어플리케이션
 ![로고](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbfQboG%2FbtsHw5Mluk1%2F0HfdpaLmjP8igs0TbvvoBk%2Fimg.png) -->

| Notion Page | 프로젝트 팀 |
| --- | --- |
| [💡 아이디어 회의](https://www.notion.so/e2a75d5db39c432e95c096f2bf558460?pvs=21) <br> [🍎 기획 (전체적인 구조)](https://www.notion.so/fa33869faa9643719dfca196efa3a2e9?pvs=21) <br> [👩‍💻 구체적인 활동](https://www.notion.so/f167ad912d29416581839b5bef1c9717?pvs=21) <br> [📆 스케줄표 ](https://www.notion.so/fd50942fabb84e7e83a8be362de9f70b?pvs=21) <br> [👨‍🔧 필수 구현기능 ](https://www.notion.so/622185bd971042ea943d3159368d7ee3?pvs=21) <br> [📝 자료조사](https://www.notion.so/577d4a3bbcff4c1c9ccfefb92d5fec13?pvs=21) | 👨‍💼 신재건 <br> 👨🏼‍💻 나경준 <br> 🙋‍♀️ 정소영 <br> <br> <br> <br> |

---
## 목차

### 🙋 I. 팀원 정보 및 업무 분담 내역

### 📊 II. 설계 내용 (아키텍처 등) 및 실제 구현 정도

### 📑 III. 데이터베이스 모델링(ERD)

### 💻 IV. 금융 상품 추천 알고리즘에 대한 기술적 설명

### 💁 V. 서비스 대표 기능들에 대한 설명

### 🙇 VI. 느낀 점, 후기 등


---

## 🙋 I. 팀원 정보 및 업무 분담 내역

- 프로젝트 기간 : 2024.4.25(목) ~ 2024.5.23(목)

| 이름 | 역할 및 구현 기능 |
| --- | --- |
| 신재건 | [ Full Stack ]<br>커뮤니티 게시판 만들기, Django 유저 정보 구현<br>라우터 URL 연결 작업, Vue와 Djnago 연결작업<br>회원 관리 ,가입상품, 더미데이터 제작 |
| 나경준 | [ Full Stack ]<br>은행 찾기 구조 구현(카카오맵 API)<br>환율 계산기, 예적금 금리 비교, 추천 알고리즘<br>금융 정보 수정 시 이메일 전송 및 금융 상품 Option DB 담당 |
| 정소영 | [ Front End ]<br>전체 레이아웃 구성, CSS 페이지 디자인<br>JavaScript를 활용한 메인페이지 애니메이션 구현, 고양이 키우기 게임<br>반응형 웹 제작 (Media Query 이용) , Notion 기록, PPT 제작 |


---

## 📊 설계 내용 (아키텍처 등) 및 실제 구현 정도

- **기술 스택 🔧**

|  | Front | Back |
| --- | --- | --- |
| Language | JavaScript | Python |
| Framework | Vue3<br>Pinia (+Pinia-plugin-persistedstate)<br>vuetify<br>axios<br>chart.js | django<br>django-rest-framework<br>django-rest-auth<br>drf-spectacular |

- 협업 도구

Git, VS Code Live , Mattermost

## 프런트엔드 화면 디자인 설계
### 🎨 Figma 
[📎 Figma Link  ](https://www.figma.com/design/4uLEnFeFRbHxRX1YmcIreS/%EA%B8%88%EC%9C%B5%ED%94%84%EB%A1%9C%EC%A0%9D%ED%8A%B8-%ED%94%BC%EA%B7%B8%EB%A7%88?node-id=0%3A1&t=GneVOKSpgqVgMRE9-1)

![Figma](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FcJHos8%2FbtsHxRVqchl%2F9oelXsL1MMGClfLaCnqrQ0%2Fimg.jpg)

메인 페이지, 로그인, 회원가입, 로그아웃, 프로필페이지(마이펫 포함), 금리 비교 (데이터 저장, 전체 조회, 상세 조회), 환율계산기, 은행검색, 커뮤니티, 금융 상품 추천 알고리즘 등 계획했던 기능을 모두 구현하였습니다.  

## 백엔드 데이터 설계
### 📑데이터베이스 모델링 (ERD)
[📎 ERD Drawing Link ](https://www.erdcloud.com/d/exwbK7Fhyy2a3QKqZ)

![ERD 이미지](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FK1DDh%2FbtsHx9aBazq%2FkeGuWg5ACF50dpzPrQgDbk%2Fimg.png)


### 🗂️ API 명세서

사용한 API : 카카오맵, 한국수출입은행 환율정보, 금융감독원, GPT OPEN AI 

명세서 작성해야 함@!!

---
## 💻금융 상품 추천 알고리즘에 대한 기술적 설명
### 추천 알고리즘 1️⃣
동일하게 1만명의 유저 더미데이터를 생성합니다. 이 후에  나이, 자산, 연봉이 비슷한 유저가 많이 가입한 금융 상품을 추천해줍니다. 먼저는 코사인 유사도(cosine similarity)를 사용하여 비슷한 유사도를 가진 금융상품을 분석합니다. 이 후에 추천하는 상품을 1등부터 6등까지 보여줍니다. 

### 추천 알고리즘 2️⃣
동일하게 1만명의 유저 더미데이터를 생성합니다. 사용자가 선호하는 은행을 고려하여 해당 은행의 상품을 우선적으로 고려합니다. 사용자의 저축 성향을 분석하여 상, 중, 하로 나눕니다. (상 : 24개월 이상 저축, 중: 12개월~24개월 저축, 하: 12개월 이하) 이렇게 나눠진 그룹 그 중에서 가장 금리가 높은 상품을 추천합니다. 추가로 연봉과 자산을 고려하여 예금과 적금을 구별하고, 사용자에게 맞는 상품을 추천하게 설계가 되어있습니다. 이렇게 세심한 고려와 다양한 요소를 고려한 추천 알고리즘은 사용자에게 현명한 금융 결정을 돕는 데 큰 도움이 될 것입니다.

---

## 💁 서비스 대표 기능들에 대한 설명
### 1️⃣ 메인페이지
![메인페이지](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fl9nt6%2FbtsHy6Yq8Ym%2FbmJ3ewJbs1F2vIMFCXjQq1%2Fimg.jpg)

### 2️⃣ 로그인, 회원가입 페이지 
![로그인 페이지](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FPBBOW%2FbtsHyT53Ika%2FF8DoPYwrK31ARsZqSYZxz1%2Fimg.png)
![회원가입 페이지](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2Fz9wQb%2FbtsHzHKDMlA%2FnioZDPveQioATwIrpDn6h0%2Fimg.png)

### 3️⃣ 프로필 페이지
![프로필 페이지](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FlCFPN%2FbtsHyDPYJDx%2FJxvZGltHMoWmV9NDOIWzp1%2Fimg.png)
![마이펫](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbmPiZc%2FbtsHxJi6fAV%2FDkLWkXQWaoeiD7gt5xiIu1%2Fimg.png)

### 4️⃣ 금리비교 
![금리비교](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FDFI5H%2FbtsHyDvGm6l%2FNIZailKWbNAOvsuL8NbMXK%2Fimg.png)

### 5️⃣ 환율계산기
![환율계산기](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FkOoyP%2FbtsHzsAaEoT%2FcGMb7ydtzVTGUrJT0AKunk%2Fimg.png)

### 6️⃣ 은행검색
![은행검색](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FcEk7Ef%2FbtsHynzPWf3%2Fke9FK7mp8J5HiTeKASYlR0%2Fimg.jpg)

### 7️⃣ 커뮤니티 
![커뮤니티](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbFIZb4%2FbtsHxJi4GHK%2F42HiPzHlnoGOtJcfW1OwV0%2Fimg.png)


## 🙇 느낀점, 후기 등

| 이름  | 내용  |
| --- | --- |
| 신재건 | 프로젝트를 진행하면서  힘든 과정을 겪었지만, 그만큼 개발자로서 성장할 수 있었습니다. 문제를 해결하며 새로운 기술을 익히고, 팀과의 협업을 통해 많은 것을 배웠습니다. 앞으로도 이런 도전들을 통해 계속 성장해 나가고 싶습니다. |
| 나경준 | 좀 더 많이 준비하고 싶었는데 시간이 짧아서 아쉬운 마음이 듭니다. Python에서는 제대로 잘 작동하는 코드들이 많은데, Django와 Vue에서 이식하지 못한 코드들이 있었습니다. 예를 들어서, 유저 간의 채팅이 되는 코드를 사용하고 싶었는데 이것이 Python에서는 잘 작동되었지만 DB에 넣고 Vue에서 렌더링을 하려고 하자 에러가 나서 어려움을 겪었습니다. 또, 토스 홈페이지에 들어가보면, 기사들이 나와있습니다. 이 부분에 네이버 뉴스 탭에 있는 금융 기사나 로이터(Reuters), 블룸버스(Bloomberg) 등 금융에 관한 세계적인 뉴스를 크롤링 해서 담는 아이디어를 생각했지만 구현하지 못해서 아쉬웠습니다. <br>이번 프로젝트를 하면서 좋았던 점은 협업의 경험을 쌓게 된 것입니다. 이전에는 팀으로 하는 프로젝트 경험이 많지 않았는데, 이렇게 프로젝트를 진행하면서 팀원들에게 도움이 될 수 있어서 기뻤습니다. 미션을 하나씩 수행할 때마다 생각지도 못했던 에러와 문제점들이 발생했는데 이것을 해결해나가는 과정이 즐거웠고 프로그래머로서 정말 좋은 경험이 되었던 것 같습니다. |
| 정소영 | 프로젝트를 진행하면서 Vue3와 Django를 혼합하여 작업하다보니 파일의 변수명과 파일명 등이 많아져서 합칠 때 어려움이 있었습니다. 이 때 팀원 중 한 분이 각각의 폴더 안에 자신의 작업물을 정리할 수 있는 새로운 폴더를 만들어 작업하는 아이디어를 제안해 주셨고, 이를 통해 파일들을 보다 체계적으로 정리할 수 있었습니다. 팀원들 덕분에 프로젝트 진행 속도가 빨라졌으며, 협업하는 법을 배울 수 있었습니다. <br>가장 중요한 것은 서로가 모르는 것이 있을 때 언제든지 질문하고 도움을 주고 받을 수 있었다는 점입니다. 특히 Vue3 렌더링 작업이 처음에는 어려웠는데, 팀원들이 함께 공부하고 서로 도와주면서 점점 이해할 수 있게 되었습니다.  팀 미션이 저의 실력 향상에 큰 도움이 되었고, Vue3에 대한 이해도가 높아지면서 프로젝트에 더욱 효율적으로 기여할 수 있게 되었습니다. 함께 노력하고 배울 수 있는 값진 경험이었습니다. |

<!-- ![로고](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FbfQboG%2FbtsHw5Mluk1%2F0HfdpaLmjP8igs0TbvvoBk%2Fimg.png) -->
