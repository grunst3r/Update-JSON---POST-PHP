# Update JSON POST PHP
Update json using post in php

```
$json = file_get_contents('config.json');
$data = json_decode($json, true);
foreach ($_POST as $key => $value) {
	if( $data[$key] == $_POST[$key] ) $data[$key] = $_POST[$key];
	else $data[$key] = $value;
}

file_put_contents('config.json', json_encode($data));

```

```
<form method="post">
TIENDA
	<input type="text" name="tienda[]">
	<input type="text" name="tienda[]">
	<input type="text" name="tienda[]">
	<input type="text" name="tienda[]">
	<input type="submit" value="Guardar">
</form>
```
```
<form method="post">
LIBRO
	<input type="text" name="libro[]">
	<input type="text" name="libro[]">
	<input type="text" name="libro[]">
	<input type="text" name="libro[]">
	<input type="submit" value="Guardar">
</form>
```
