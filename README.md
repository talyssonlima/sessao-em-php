### Classe para manipulação de sessões em php, fácil e muito útil no desenvolvimento de uma aplicação.

```php
<?php  
  
require __DIR__ . "/Session.php";  
  
$session = new Session();  
  
//Criar sessão  
$session->set("user", ["email" => "example@mail.com", "password" => "12345678"]);  
$session->set("user1", ["email" => "example@mail.com", "password" => "12345678"]);  
$session->set("admin", ["email" => "exampleadmin@mail.com", "password" => "87654321"]);  
  
//Verifica a existência da sessão e exclui  
if($session->has("user1")){  
    $session->unset("user1");  
}  
  
//Regenera o id da sessão, excluindo o antigo id e criando um novo  
$session->regenerate();  
  
//Mostra todos os índices da sessão  
var_dump($session->all());  
  
//Destrói a sessão  
$session->destroy();
``
