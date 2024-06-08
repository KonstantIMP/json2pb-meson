# json2pb messon wrapper

Use this repo to seamlessly import json2pb library from [original repo](https://github.com/shramov/json2pb) in your meson project

First off all add wrap file `subprojects/json2pb.wrap` with content
```
[wrap-git]
url = https://github.com/KonstantIMP/json2pb-meson.git
revision = master
```

Then inside your meson build script you can get json2pb dependecy and use it for any target
```
json2pb = subproject('json2pb').get_variable('json2pb')
```
