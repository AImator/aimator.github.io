## [markdown 高级用法](./markdown_advanced_usage)

##### *Made by* [AImator.com]()

### Customize Image Properties

<p align="center">
 <a href="http://asses.aimator.com">
  <img height="150px" width="150px" src="https://code.aliyun.com/aimator/assets/raw/master/images/aimator300.jpg?raw=true">
 </a>
</p>
<h3 align="center">AImator</h3>
<p align="center">Everyone can find valuable contents here....
</p>
<p align="center">
 <a href="http://asses.aimator.com">
  <strong>Visit AImator &raquo;</strong>
 </a>
</p>

The following code can let you get the above output:

```
<p align="center">
 <a href="image_click_url">
  <img height="150px" width="150px" src="image_url.jpg?raw=true">
 </a>
</p>
<h3 align="center">tittle</h3>
<p align="center">description...
</p>
<p align="center">
 <a href="text_click_url">
  <strong>Visit AImator &raquo;</strong>
 </a>
</p>
```

<img height="72px" width="72px" align="right" src="https://code.aliyun.com/aimator/assets/raw/master/images/aimator150.jpg?raw=true">

There is another way to customized image properties, especially when you need to mix graphics and text.

The following code can let you get the right output:

```
<img height="72px" width="72px" align="right" src="image_url.jpg?raw=true">
```

If your site directory structure like this:

```
directory/
│
├── markdown.md
│
├── images/
│   ├── image.png
│   ├── image.jpg
│   └── image.svg
│
└── others/
    ├── filename.css
    └── filename.js
```

Then you can use `"./images/image.png?raw=true"` instead of `"http://external_url"` to show the image.

### Insert Shields

What are shields? Maybe you've been found these cute images if you love to visit GitHub.com:

[![Travis](https://img.shields.io/travis/rust-lang/rust.svg)](http://development.aimator.com/notebook)
[![Magnum CI](https://img.shields.io/magnumci/ci/96ffb83fa700f069024921b0702e76ff.svg)](http://development.aimator.com/notebook)
[![Coveralls](https://img.shields.io/coveralls/jekyll/jekyll.svg)](http://development.aimator.com/notebook)
[![Coverity Code Advisor On Demand Job Badge](https://img.shields.io/coverity/ondemand/jobs/JOB.svg)](http://development.aimator.com/notebook)

You can browse all catagories shields from [Shields.io](http://shields.io), even customized your badge.