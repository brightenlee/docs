# ROAS Tutorial

This is the source for ROAS Tutorial.


Building new releases
------------------------------------------

```
git clone https://github.com/brightenlee/roas_docs.git html
```


Publishing sphinx-generated docs on github
------------------------------------------

##### Set up sphinx:
```
pip install sphinx
pip install sphinx_rtd_theme
pip install recommonmark

mkdir docs
cd docs
sphinx-quickstart
```

##### Set up docs repository:
```
rm -rf _build/html
cd _build
git clone https://github.com/brightenlee/roas_docs.git html
cd html
git branch gh-pages
git symbolic-ref HEAD refs/heads/gh-pages
rm .git/index
git clean -fdx
```

##### Initial creation and commit:
```
cd _build/html
git add .
git commit -m "Initial commit"
git push origin gh-pages
```
