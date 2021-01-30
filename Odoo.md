# Building a sample module

## Error: Unable to import odoo 

Context: In file {module_name}/models/models.py

Solution:

1. Install Pylint Odoo Plugin 
  ```pip3 install --upgrade --pre pylint-odoo```

2. Create a file named **.pylintrc** in the module 

3. Add the plugin in **.pylitrc**
  ```load-plugins=pylint_odoo```

## Problem: Updating odoo default listening port

Solution:

In odoo.conf file add a line, ```xmlrpc_port = {port-number}```.
