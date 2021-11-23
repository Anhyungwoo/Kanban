# 칸반보드
## 개요 
### 1. 서비스 내용 
```

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