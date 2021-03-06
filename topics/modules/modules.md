layout: true
class: center, middle, inverse

---

# Modules (PEP 302)
with [examples](modules.ipynb)
## [GeeksHub](http://www.geekshub.in)
### [info@geekshub.in](mailto:info@geekshub.in)

---

name: inverse
layout: false

# Modules
* Modules are objects of type "ModuleType"
* Modules have namespaces
* Usually loaded from file
* Modules have execution environment

---

# Import and Namespaces
* Modules can be imported
* Modules are loaded in System Cache
* References gets added
* locals() and globals()
* Attributes can be added to module's namespace
* Examples
    ```python
    import math
    print(math.__name__)
    print(id(math))
    print(math.__dict__)
    print(sys.modules)
    ``` 
---

# How Importing Works
* Checks sys.modules
* Creates a new module type
* Loads source code from the file (if not found in sys.modules cache)
* Add entries to the cache
* Compiles and executes the source code
* Finders, Loaders, Importers

---

# Importing (Cntd)
* Finders - finds the module (file, network, database etc)
    * sys.meta_path
* Loaders - loads and executes the module using ModuleSpec
* Importers - names given to Finders/Loaders
* Varieties of finders/loaders available in Python
    * \_\_spec\_\_
* sys.path or package's \_\_path\_\_
* import
    * imports the modules (more on this later)
* importlib
    * importlib.import_module('math')- loads sys.modules cache using module name
    * importlib.util.find_spec to get the spec file of the module
* [Examples](import_importlib.ipynb)

---

# Module Properties
* type(math)
* math.\_\_spec\_\_
* math.\_\_name\_\_
* math.\_\_package\_\_
* math.\_\_file\_\_ (not available for built-in modules)
* built-in
    * math
* standard library
    * fractions
* custom module
    * module1

---

# Import Variants
* import __module__
* import __module__ as __alias__
* from __module__ import __symbol__
* from __module__ import __symbol__ as __alias__
* from math import *
* All imports leads to loading of entire modules in sys.cache
* The only difference is what symbols imported to globals() or locals()
* [Examples](import_variants.ipynb)

---

# Reloading Modules
* Danger ahead
    * deleting sys.modules entry
    * importlib.reload(module_name)
* Can be done but dangerous
* Some other part of the code may still referring to outdated
* Do not do it in production
* [Examples](reloading_modules.ipynb)

---

# \_\_main\_\_
* \_\_name\_\_ set to \_\_main\_\_ if the module is run as script
* \_\_name\_\_ points to module name if imported as module
* \_\_main\_\_.py - Python executes this file when it is present as starting point of the application
* Let us see some examples

---

# Exercises


---

layout: true
class: center, middle, inverse

# Thank you :-)

# [GeeksHub](http://www.geekshub.in)
_**Co-Creating Tomorrow **_
### [info@geekshub.in](mailto:info@geekshub.in)

---
