# Instructions for creating an editable version of a specfic version of a package
```python
mkdir editableproject
cd editableproject
virtualenv menv
source menv/bin/activate
```
Then download the specific version of the code (e.g., mws v0.8.3)
set it up in a directory:
```python
mkdir mwseditable
cd mwseditable    <- paste the downloaded code here (in tar.gz format)
tar xvzf python-amazon-mws-0.8.3.tar.gz   <- this will unzip the downloaded code
pip install -e python-amazon-mws-0.8.3    <- install in editable mode
flask shell
import mws
```
Voila! The package is imported from this folder instead of site-packages. Verify as below:
```python
$ flask shell
>>> import mws
>>> mws.__file__
```
