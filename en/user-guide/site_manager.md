Site Manage
======================

### 1. Select menu

Click the Site Manage Menu in Left Main Navigation.

### 2. Add site

Click the `New Site` button.

<a href="images/site_manage.png" target="_blank"><img src="images/site_manage.png" width="600px;"/></a>

Input the site name and site Url, and then click the `Add Site` button

Site Url must be entered exactly start with `http://`

** It is important to accurately input the URL **

<a href="images/new_site.png" target="_blank"><img src="images/new_site.png" width="600px;"/></a>

### 3. Add script in your site

Pease add the script to the bottom of the page of the site to be applied

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