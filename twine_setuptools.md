## CreatePyPiPackages

<p>
  
### Step1
* Create a folders under name mypackages and move inside of it
```ruby
mkdir mypackages
cd mypackages
```
  
### Step2
* Create a folders under mathpackage and move inside
```ruby
mkdir mathpackage
cd mathpackage
```
  
### Step3
* Create a folders below files under mathpackage
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
* go back to mypackages
```ruby
cd .. 
```
  
  ### Step6
* create check.py(paste below code in it) to test if we can import modules
```ruby
nano check.py
_______
from mathpackage import calculations
calculations.add(10,10)
```
  
 ### Step7
* run check.py and see if its printing 20, if printed 20 then delete check.py
```ruby
python3 check.py
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
* create a setup.py and LICENSE by copying code from [here]  
```ruby
nano setup.py
nano LICENSE
```
### Step10
* run below 2 commands and enter your username and password of pypi.
```ruby
python3 setup.py sdist bdist_wheel
python3 -m twine upload dist/*
```
### Step10
* Now you can install your package using pip and check if its working by creating check.py same as in step 6 and 7
```ruby
pip install mathpackage

```
</p>
