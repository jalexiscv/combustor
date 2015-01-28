Combustor
=========

Combustor is a code generator console application for [CodeIgniter](https://ellislab.com/codeigniter/) in order to speed up the development of web applications. This library generates a [CRUD](http://en.wikipedia.org/wiki/Create,_read,_update_and_delete) interface (with [Bootstrap](http://www.getbootstrap.com), optional only) with an integration of an [ORM library](http://www.doctrine-project.org/) or with a factory pattern that is based from this [link](http://www.revillweb.com/tutorials/codeigniter-tutorial-learn-codeigniter-in-40-minutes/).

Instructions
============

1. Download the latest version of CodeIgniter then add the package in your require-list in ```composer.json``` and after that, run ```composer install```:

	```
	{
		"require": {
			"rougin/combustor": "dev-master"
		}
	}
	```

2. After installing the required dependencies, run the command below in the PHP CLI:

	**For Unix and Mac:**

	```php vendor/bin/pertain```

	**For Windows or if there are no symbolic links found at ```vendor/bin``` directory:**

	```php vendor/rougin/combustor/bin/pertain```

	**NOTE**: The command above only setups the Combustor and Doctrine for CodeIgniter. To include the integrated pagination and other stuff, I've created a [simple script](https://github.com/rougin/ignite.php) for that.

2. Then, access the application via the PHP CLI and to retrieve the list of commands:
	
	**For Unix and Mac:**

	```php vendor/bin/combustor```

	**For Windows or if there are no symbolic links found at ```vendor/bin``` directory:**

	```php vendor/rougin/combustor/bin/combustor```

Reminders
=========

* If you want to know more about Doctrine ORM and its functionalities, you can always read their documentation [here](doctrine-orm.readthedocs.org/en/latest/tutorials/getting-started.html).
* Before generating the models, views, and controllers, please make sure that you **set up your database** (foreign keys, indexes, relationships, normalizations) properly to minimize modifications after the codes has been generated. Also, generate the models, views, and controllers first to tables that are having **no relationship with other tables** in the database.
* Found a bug? Want to contribute? Feel free to open an issue or create a pull request. :+1: