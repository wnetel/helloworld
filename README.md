# helloworld
It's a simple python package that prints hello world!



## PIP install

1. Test\prerelease
https://test.pypi.org/project/wnhelloworldpackage/
`pip install -i https://test.pypi.org/simple/ wnhelloworldpackage`

2. Production
https://pypi.org/project/wnhelloworldpackage/
`pip install wnhelloworldpackage`


## Test locally from source code

`pip install .`

`python test.py`

## Create local package

1. Make sure you have the latest versions of setuptools, wheel installed:
`pip install --user --upgrade setuptools wheel`

2. `python setup.py sdist bdist_wheel`

3. under `dist` there will be one or many `*.whl` file you can install it locally
`pip install C:/some-dir/some-file.whl` or
`pip install /dist/some-file.whl`


## Steps to upload your package to the Python Package Index under your account:


1. get user account https://test.pypi.org

2. get user account https://pypi.org

3. Make sure you have the latest versions of setuptools, wheel and twine installed:
`pip install --user --upgrade setuptools wheel`
`pip install --user --upgrade twine`

4. Rename azhelloworldpackage, your package name can contains letters, numbers, _ , and -. It also must not already taken on pypi.org
you need to rename `name` in `setup.py` file and rename the folder structure
`

/yourpackagename
    __init__.py

`

5. `python setup.py sdist bdist_wheel`

6. Upload it to test\prerelease environment `twine upload --repository-url https://test.pypi.org/legacy/ dist/*`

7. Test newly uploaded package `pip install -i https://test.pypi.org/simple/ yourpackagename`

8. Upload it to production environment `twine upload dist/*`

9. Test your package `pip install yourpackagename`

Resource
https://packaging.python.org/tutorials/packaging-projects/#uploading-your-project-to-pypi
