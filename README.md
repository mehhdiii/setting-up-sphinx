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

### add path to your py scripts for them to be visible to sphinx: 
goto docs >> source >> config.py and add the following line: 

```
import os
import sys
sys.path.insert(0, os.path.abspath('../..')) # or whatever your relative path to the source code is
```

now you can refer to your scripts using the above path as `base`

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
