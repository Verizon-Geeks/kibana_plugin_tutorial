* Custom Loader for Kibana 7.4

The throbber is the animation that appears on the Kibana page while it does not load all its components. The throbber logo is embedded in .kibanaWelcomeLogo

If you have kibana already installed, This can be found in 

```sh
/usr/share/kibana/src/legacy/ui/ui_render/views/ui_app.pug
```
Point to the right svg file you would like to have in it place.

You can also convert the svg file to base 64 format by

```sh
base64 yourimage.svg
```


* reference
- https://medium.com/gradiant-talks/customizing-kibana-web-application-f74c1b48ec73
