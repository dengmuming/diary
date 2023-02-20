# Read the Docs And Sphinx

## 启动项目
```
方式1：cd dairy && make html，在浏览器打开build/html/index.html文件
方式2：cd dairy && make html，在根目录cmd执行 `sphinx-autobuild source build/html`
```
`参考文档：https://blog.csdn.net/lu_embedded/article/details/109006380`

## 部署Read the Docs
### 官方文档
```
https://docs.readthedocs.io/en/stable/intro/getting-started-with-sphinx.html
```
### Could not import extension sphinx_markdown_tables (exception: No module name
原因是ReadTheDocs的python环境没有对应的第三方库文件，需要在项目根目录执行如下命令生成requirements.txt，这样ReadTheDocs会自动安装对应的插件依赖。
```
$python3 -m pip freeze > requirements.txt
```