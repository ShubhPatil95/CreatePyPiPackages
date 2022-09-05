## CreatePyPiPackages

<p>
  
### Step1
* Create a folders under name mypackages and move inside of it
```ruby
mkdir CreatePyPiPackages
cd CreatePyPiPackages
```
  
### Step2
* Create a folders under mypackagearrithmatics and move inside(NOTE: package name should be unique, hence make sure you are giving your unqiue name to this package. I am giving mypackagearrithmatics, hence in further steps kind ensure to replace mypackagearrithmatics with your package name)
```ruby
mkdir mypackagearrithmatics
cd mypackagearrithmatics
```
  
### Step3
* Create a folders below files under mypackagearrithmatics
```ruby
touch calculations.py __init__.py
```
  
### Step4
* Write below code inside calculations.py
```ruby
def add(a,b):
  print("This is addition=>",a+b)
  
def sub(a,b):
  print("This is substraction=>",a-b)
```
  
 ### Step5
* go back to CreatePyPiPackages
```ruby
cd .. 
```
  
  ### Step6
* create [check.py](https://github.com/ShubhPatil95/CreatePyPiPackages/blob/main/mypackagemath/check.py) to test if we can import modules
```ruby
nano check.py
```
  
```ruby
from mypackagearrithmatics import calculations
calculations.add(10,10)
```
  
 ### Step7
* run check.py and see if its printing "This is addition=> 20",then delete check.py
```ruby
python3 check.py
```
 ```ruby
rm check.py
```
 <strong> This is how we can create a module and package. Further we will see how to publish these packages</strong> <br>

  
 ### Step8
* install dependencies
```ruby
pip install wheel
pip install twine
python3 -m pip install --upgrade twine setuptools
```
  
### Step9
* create a setup.py and LICENSE by copying code from [setup.py](https://github.com/ShubhPatil95/CreatePyPiPackages/blob/main/mypackagemath/setup.py) and [LICENSE](https://github.com/ShubhPatil95/CreatePyPiPackages/blob/main/mypackagemath/LICENSE). Make sure you are replacing details in setup.py with your details, also update your name replacing mine in LICENSE.
```ruby
nano setup.py
```
```ruby
nano LICENSE
```  
### Step10
* run below 2 commands and enter your username and password of pypi.
```ruby
python3 setup.py sdist bdist_wheel
python3 -m twine upload dist/*
```
### Step10
* Now you can install your package using pip
```ruby
pip install mypackagearrithmatics
```
### Step11
 * Type below line in python and see if you its printing "This is addition=> 40"
```ruby
from mypackagearrithmatics calculations
calculations.add(20,20)
```
</p>
