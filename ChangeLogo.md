## Replacing Kibana Logo
Kibana logo is part of .euiHeaderLogo

easy way to replace the logo is replace the .euiHeaderLogo


### Method 1 - Generate a plugin with Hack and replace

#### Generating a plugin

refer plugin generator https://github.com/elastic/kibana/tree/7.4/packages/kbn-plugin-generator

#### Edit hack.js 

In hack.js, use jquery to replace the .euiHeaderLogo with your own implementation

1. Define a .css file and add the following into it
```s
.logoWhiteBg1 {
  width: 120px;
  height: 24px;
  display: inline-block;
  padding: 10px;
  background-repeat: no-repeat;
  background-size: contain;
  background-position: center;
  background-image: url("./myfile.svg");
  }
```

2. In hack.js, 
```s
import './your.css'

$(document).ready(function(){

$(".euiHeaderLogo").replaceWith(`<div align="center" class=" logoWhiteBg1">`);

}

```
## Reference

- https://medium.com/gradiant-talks/customizing-kibana-web-application-f74c1b48ec73

