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

```

### 3. 각 페이지별 소개
* 메인페이지
![메인페이지](https://www.google.com/images/branding/googlelogo/2x/googlelogo_color_272x92dp.png)



## 핵심기술
### 1. 회원가입
#### 동작 방식에 대한 설명 .....
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
