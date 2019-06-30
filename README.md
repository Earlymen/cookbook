# Elephant cookbook

```php 
      public function connect($dbname, $username, $password, $host='127.0.0.1')
        {
            try
            {
                $this->handler = new PDO('mysql:host = '.$host.'; dbname='.$dbname, $username, $password);
                $this->handler->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
            } catch (PDOException $e)
            {
                die('Unable to connect to the database');
            };
            return $this->handler;
        }
 ```
