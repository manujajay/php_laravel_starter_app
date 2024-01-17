# PHP Laravel Starter Application

This repository contains the PHP Laravel Starter Application. It provides a basic setup for a Laravel web application, including routing, views, controllers, models, and database interactions. Follow the instructions below to set up the project.

## Table of Contents
- [Initial Setup](#initial-setup)
- [Using This Repository](#using-this-repository)
- [Working with Models and Databases](#working-with-models-and-databases-optional)
- [Testing the Application](#testing-the-application)
- [Troubleshooting](#troubleshooting)
- [Further Information](#further-information)

## Initial Setup
If you're setting up a new Laravel project from scratch, follow these steps:

### Step 1: Install Composer

- Download and install Composer from [getcomposer.org](https://getcomposer.org).

### Step 2: Install Laravel

- Open a terminal or command prompt.
- Run `composer global require laravel/installer` to install the Laravel installer.

### Step 3: Create a New Laravel Project

- Run `laravel new php_laravel_starter_app` to create a new project.
- This command creates a new directory named `php_laravel_starter_app` with Laravel installed.

### Step 4: Explore the Project Structure

- Open the `php_laravel_starter_app` directory in your code editor.
- Notice the MVC architecture: models in `app/Models`, views in `resources/views`, and controllers in `app/Http/Controllers`.

### Step 5: Start the Laravel Development Server

- Inside the `php_laravel_starter_app` directory, run `php artisan serve`.
- This starts a development server at `http://localhost:8000`.

## Using This Repository

If you're cloning this repository:

### Step 1: Clone the Repository

- Run `git clone https://github.com/your-username/php_laravel_starter_app.git`.
- Change into the directory using `cd php_laravel_starter_app`.

### Step 2: Install Dependencies

- Run `composer install` to install the required PHP dependencies.

### Step 3: Set Up Environment Variables

- Copy `.env.example` to a new file named `.env` using `cp .env.example .env`.
- Configure your `.env` file as necessary for your local environment.

### Step 4: Generate Application Key

- Run `php artisan key:generate` to generate a new application key. This will automatically update your `.env` file.

### Step 5: Start the Laravel Development Server

- Run `php artisan serve` to start the Laravel development server.

## Working with Models and Databases (Optional)

### Setting Up the Database

- Update your `.env` file with your database credentials:

```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=your_database
DB_USERNAME=your_username
DB_PASSWORD=your_password
```

### Creating a Model

- Use Artisan to create a new model, for example: `php artisan make:model YourModel`.

### Database Migrations

- Create a new migration with `php artisan make:migration create_your_table --create=your_table`.
- Run migrations with `php artisan migrate`.

### Interacting with the Database

- Eloquent is Laravel's built-in Object-Relational Mapping (ORM) tool, which means it is already included as part of the Laravel framework. There's no need to download or install anything extra if you're using Laravel. 
- Eloquent provides a simple, elegant syntax for interacting with your database (via just php code).
- After creating a model, you can use it to query the database in your controllers or other parts of your application.


#### Retrieving Data

- Retrieve all records from a model's associated table: `YourModel::all();`
- Retrieve single record using its primary key: `YourModel::find($id);`

#### Saving Data

- To create a new record, instantiate a new model instance, set attributes, and call `save()`:

  ```php
  $yourModel = new YourModel;
  $yourModel->name = 'Example';
  $yourModel->save();
  ```

#### Saving Data

- To create a new record, instantiate a new model instance, set attributes, and call `save()`:

  ```php
  $yourModel = new YourModel;
  $yourModel->name = 'Example';
  $yourModel->save();
  ```

#### Updating Data

- Retrieve the model, change the attributes, and call `save()`:

  ```php
    $yourModel = YourModel::find($id);
    $yourModel->name = 'New Name';
    $yourModel->save();
  ```

#### Deleting Data

- Retrieve the model and call `delete()`:

  ```php
    $yourModel = YourModel::find($id);
    $yourModel->delete();
  ```

#### Eloquent Relationships

- Define relationships in your Eloquent models (e.g., `hasOne`, `hasMany`, `belongsTo`) to interact with related data across different tables.

  ```php
    $yourModel = YourModel::find($id);
    $yourModel->delete();
  ```

## Testing the Application

- Visit `http://localhost:8000` in your browser to view the application.
- Access other routes as defined in `routes/web.php`.

## Troubleshooting

If you run into issues:

- Run `composer dump-autoload` to regenerate the autoload files.
- Check the Laravel log in `storage/logs` for error details.
- Ensure file permissions are correctly set for the `storage` and `bootstrap/cache` directories.

## Further Information

For more detailed information, refer to the [Laravel documentation](https://laravel.com/docs). This project is a basic introduction to setting up and using Laravel. We recommend exploring the Laravel documentation and building more complex applications for a deeper understanding.


