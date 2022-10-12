# Magento Yield Management
Module to connect with the homemade Yield Management App . 
This module deal with the calendar pricing logic , that the Wobz industry implement.
It working with Magento 2.3.*


- Step 1: Composer installation
- Step 2: Enable the module



### Step 1. Composer installation

In this module, we will use composer to install it on different e-commerce .

~~~
composer require wobz-tech/magento-yield-management
~~~



### Step 2. Enable the module

By finish above step, you have created an empty module. Now we will enable it in Magento environment.
Before enable the module, we must check to make sure Magento has recognize our module or not by enter the following at the command line:

~~~
php bin/magento module:status
~~~

If you follow above step, you will see this in the result:

~~~
List of disabled modules:
WobzTech_MagentoYieldManagement
~~~

This means the module has recognized by the system but it is still disabled. Run this command to enable it:

~~~
php bin/magento module:enable WobzTech_MagentoYieldManagement
~~~

The module has enabled successfully if you saw this result:

~~~
The following modules has been enabled:
- WobzTech_MagentoYieldManagement
~~~

This’s the first time you enable this module so Magento require to check and upgrade module database. We need to run this comment:

~~~
php bin/magento setup:upgrade
~~~
Then use the compilation tool and the static deployment command line : 
~~~
php bin/magento setup:di:compile
php bin/magento setup:static-content:deploy [langages]

~~~

Now you can check under Product page if  the module is present.

TODO example of implementation
