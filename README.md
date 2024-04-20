# setting-up-sphinx

### steps

create a python venv using python 3
```
python -m venv venv
```

activate venv: 
```
source venv/bin/activate
```

install relevant libraries using pip 
```
pip install sphinx #and other dependencies
```

create a docs directory to seperately handle documentation: 
```
mkdir docs && cd docs
```

setup sphinx project using quick start
```
sphinx-quickstart
```

### Set up gh pages: 
goto repository settings >> pages. select `/docs` as the build directory. 

### compile changes and copy to /docs
inside /docs, run:
```
make html
```
Then copy all build html files to /docs so that they're visible to gh pages.
```
cp -r build/html .
```
