## Changing the Login Screen in Kibana 7.4
Main elements of login screen are following

1. ".euiTitle.euiTitle--large.loginWelcome__title" --> Title 
2. ".euiText.euiText--small.loginWelcome__subtitle" --> SubTitle
3. ".loginWelcome__logo" --> Logo
4. ".euiCallOutHeader" --> Logged out message


### Method 1: Using the Plugin hack

Similar to changing the logo, we use hack.js to replace the above defined classes with out custom implementations

```s
var welcomeText = `<h1 class="euiTitle euiTitle--large loginWelcome__title">Welcome Xeardoth!!!</h1>`
var welcomeSubText = '<div class="euiText euiText--small loginWelcome__subtitle"><div class="euiTextColor euiTextColor--subdued"><p>Login</p></div></div>'
var logo1 = `<div ><img src="./xeardoth.png" id="xeardothlogo"></div>`

 $(".euiTitle.euiTitle--large.loginWelcome__title").replaceWith(welcomeText);
 $(".euiText.euiText--small.loginWelcome__subtitle").replaceWith(welcomeSubText);
 $(".loginWelcome__logo").replaceWith(logo1);
 $("#verizonlogo").css('display', 'inline-block').css('height','40').css('margin-bottom', '40px');

```
