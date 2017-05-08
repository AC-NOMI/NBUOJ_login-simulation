# NBUOJ_login-simulation  
打开Chrome浏览器，输入地址:www.nbuoj.com  
按F12打开网络监听，选中Network工具栏，勾选Presever log，否则页面刷新时会将之前的记录清除。输入id和password，点击登录，可以看到浏览器产生了一系列的操作，其中访问了一个http://www.nbuoj.com/v8.8/Home/LoginDeal.php的页面，这个便是登录页面。  
选中LoginDeal页面，可以看到浏览器发送与接收的数据，我们先设置headers，其中包括了user-agent，referer等内容，具体见代码。  
除了headers之外，发送的内容中的data部分uid字段，password字段，submit字段，我们在代码中设置一个字典data，values = {'uid':'yourid','password':'yourpassword','submit':'登陆'}，在yourid部分填上你自己的id，在yourpassword填上你自己的密码。  
运行这个python脚本，便可以登录NBUOJ，当然，这段代码的功能只能实现模拟登录，运行完之后，你可以在自己账号的资料页面的登录历史中见到刚刚的那次登录记录。 