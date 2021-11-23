# 칸반보드
## 개요
### 1. 서비스 내용
```
게시글을 업로드, 수정, 삭제후 목록에서 확인할 수 있는 게시판을 개발했으며,
게시글의 기능들은 모두 회원가입 후 로그인 상태여야만 사용 가능합니다.
```

* PHP로 구현된 칸반 보드 (http://anstar94.cafe24.com)
* Node.js로 구현된 칸반 보드 (http://ahw94.cafe24app.com)

### 2. 적용 기술

```
 PHP-Kanban : Html / Css / JavaScript / Vue.js / PHP / DB

 Node.js-Kanban : Html / Css / JavaScript / vue.js / Node.js / DB
```

### 3. 각 페이지별 소개
* 메인페이지
![메인페이지](https://www.google.com/images/branding/googlelogo/2x/googlelogo_color_272x92dp.png)
* 로그인
```
프론트엔드(Vue.js)에서 회원데이터를 전송하여 백엔드(PHP)에서 요청받는 데이터가
DB에 등록된 회원의 정보와 일치하는지 검토하여 일치하는 데이터가 있으면 로그인이 됩니다.
로그인 유지를 처리하기 위해서 sessionId 형태로 토큰을 저장하여 로그인 유지 처리를 하고
페이지 새로고침 시 데이터유지가 안되는걸 방지하기 위해 vuex-presistedstate Module을
설치하여 유지하도록 개발했습니다.
```

* 회원가입
```
회원가입은 사용자가 데이터를 입력하면 연결된 DB를 통해 데이터가 저장됩니다.
그리고 회원가입시 사용자가 일치하지 않는 데이터를 입력시, 모두 예외 처리를 했습니다.
사용자가 입력해야 하는 일치하는 데이터는 다음과 같습니다.
1. 아이디 : 6자 이상 알파벳과 숫자로 구성
2. 비밀번호 : 8자 이상 알파벳 + 특수문자 + 숫자로 구성
3. 비밀번호 확인 : 앞서 입력한 비밀번호와 일치해야 합니다.
4. 회원명과 휴대전화번호는 필수 입력사항이 아니므로 작성하지 않아도 가입이 가능합니다.
```

* 회원정보 수정
```
회원정보수정 부분은 토큰값과 회원명을 확인하여 정보를 가져와서 일치하면 수정이 가능합니다.
또한 비밀번호 변경시 입력된 경우만 비밀번호가 변경되도록 처리하고 미입력시 기존 비밀번호가
유지되도록 개발했습니다.
```

* 게시판 작성, 수정, 삭제
```
프론트엔드(Vue.js) 기술을 사용하여 게시판의 기본 프레임을 만들고, 백엔드(PHP, DB)를 연동하여
사용자가 입력하는 데이터가 데이터베이스 테이블에 저장이 되도록 연동시켰습니다.
```



## 핵심기술
### 1. 회원가입
```
회원가입은 사용자가 원하는 데이터를 요청받아 DB를 연동시켜 저장합니다.
이때 비밀번호는 개발자 및 관리자가 알 필요가 없으므로 암호해쉬값으로 입력됩니다.
```

```
	  <template>
		<PageTitle>회원가입</PageTitle>
		<Form :mode="mode" />
	</template>
		<script>
		import PageTitle from "../../components/PageTitle.vue"
		import Form from "../../components/member/Form.vue"
		export default {
			components: {PageTitle, Form},
			created() {
				if (this.$isLogin()) {
					this.$router.push({ path : "/my_info" })
				}
			},
			data() {
				return {
					mode : "join"
				};
			}
		}
		</script>
```
### 2. 로그인

### 3. 작업 목록

111
