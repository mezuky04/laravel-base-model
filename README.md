laravel-base-model
==================

BaseModel.php implements in all laravel models that extends it basic database operations like select, update, insert, delete

# Usage
Put BaseModel.php in your models direcotry and extend it in all your other models.

```php
class UsersModel extends BaseModel {

    /**
     * @var string
     */
    protected $_tableName = 'Users';

    /**
     * @var array
     */
    protected $_tableFields = array('UserId', 'Email', 'Name', 'Password');
}

```
Then, you can use functions like getOne, getAll, update, insert with your model.
```php
$usersModel = new UsersModel();

$result = $usersModel->getOne(array('UserId' => 1), array('Email'));

echo $result->Email;
