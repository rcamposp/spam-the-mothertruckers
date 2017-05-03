# spam-the-mothertruckers
Script para spamear sitios de phising

```
  $client = new \GuzzleHttp\Client();
  $i = 0;
  while($i<10){
      $client->post(
          'http://www.mediationtraininggroup.com/Support/wwww.santander.cl/transa/segmentos/Menu/view.asp',
          array(
              'form_params' => array(
                  "bcplogin" => "login",
                  "rut" => rand(1000000,99999999)."-".rand(0,9),
                  "pin" => rand(1000,9999),
                  "Entrar.x" => rand(10,107),
                  "Entrar.y" => rand(10,107)
              )
          )
      );
      Log::debug("Vete: " . $i);
      $i++;
  }
  echo "<script>
      window.location.href = 'http://localhost/vete';
  </script>";
  ```
