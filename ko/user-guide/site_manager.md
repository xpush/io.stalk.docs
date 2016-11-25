사이트 관리
======================

### 1. 메뉴 이동

좌측 Main Navigation에서 Site Manage 메뉴를 클릭합니다.

### 2. 사이트 등록

`신규 등록` 버튼을 클릭합니다.

<a href="images/site_manage.png" target="_blank"><img src="images/site_manage.png" width="600px;"/></a>

사이트 네임과 사이트 Url을 입력하고 `신규 등록` 버튼을 클릭합니다.

사이트 Url은 `http://`로 시작되도록 정확하게 입력해야합니다.

** 사이트를 등록하거나 수정할 때 URL을 정확히 입력하는 것** 이 중요합니다.

<a href="images/new_site.png" target="_blank"><img src="images/new_site.png" width="600px;"/></a>

### 3. 사이트의 스크립트 수정

아래의 스크립트 코드를, 적용할 사이트의 페이지 하단에 추가해주세요.

<a href="images/site_script.png" target="_blank"><img src="images/site_script.png" width="600px;"/></a>

```html
<html>
<body>
...
<script>
window.stalkConfig = {
    "server": "http://admin.stalk.io:9000",
    "id": "305b9880-88dc-11e5-a1ae-8d70139192fd"
};
</script>
<script src="http://static.stalk.io/widget.js"></script>
</body>
</html>
```