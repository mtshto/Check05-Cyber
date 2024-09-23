# Check05-Cyber

## Comandos
```http
sudo apt-get install openssh-server
```
```http
/etc/ssh/sshd_config
```
![image](https://github.com/user-attachments/assets/eda30b77-ccb2-4e67-bf9d-651d574d01dc)

![image](https://github.com/user-attachments/assets/ae99765d-0ec6-402c-99cd-93d09180bf4a)
![image](https://github.com/user-attachments/assets/483b98e0-bbcc-473c-9754-438f949b98a6)

## Visualização transferência de arquivos
![image](https://github.com/user-attachments/assets/bef39fbb-9589-4791-b3fc-33d35f04212e)
![image](https://github.com/user-attachments/assets/65ce943f-cd49-4167-af4a-706cd83e1d83)
![image](https://github.com/user-attachments/assets/34671b64-0ae1-44de-9db5-494272a25457)

## Práticas recomendadas para proteger o acesso SSH

![image](https://github.com/user-attachments/assets/340aaad1-468c-421a-b5c0-5e6c00326cc0)
![image](https://github.com/user-attachments/assets/0067661a-f5b8-444a-a7c2-cbdced5e0c6f)
![image](https://github.com/user-attachments/assets/02d9f533-0d31-4e20-bc57-3d209a3a4ddf)
![image](https://github.com/user-attachments/assets/d344b823-c9df-46cd-8862-a379b33a5e80)
![image](https://github.com/user-attachments/assets/7703d712-2704-45f5-8e8b-c05c9eeedd01)
![image](https://github.com/user-attachments/assets/47b56417-2b0c-4486-8509-6ba4bd120b34)
![image](https://github.com/user-attachments/assets/db0c9a75-35cd-4a79-963d-4e5ad6e0f772)
![image](https://github.com/user-attachments/assets/b62cbe8a-bae5-4af7-a083-4fdd87d33732)

# Metodo_GET_POST

## /var/www/html (ls ou cat xxxx.html)

#### Verificar a Versão do PHP Instalado
```http
php -v
```

####  Instalar o PHP (se não estiver instalado)
```http
sudo apt update
sudo apt install php7.4 libapache2-mod-php7.4
```

#### Reiniciar o Apache
```http
sudo systemctl restart apache2
```

#### form_get.html
```http
<!-- form_get.html -->
<html>
<body>
<h2>Formulário GET</h2>
<form action="process_get.php" method="GET">
Nome: <input type="text" name="nome"><br><br>
Email: <input type="email" name="email"><br><br>
<input type="submit" value="Enviar">
</form>
</body>
</html>
```

#### process_get.php
```http
<!-- process_get.php -->
<?php
?>
$nome = $_GET['nome'];
$email = $_GET['email'];
echo "<h2>Dados Recebidos via GET</h2>";
echo "Nome: ". htmlspecialchars(Snome). "<br>";
echo "Email: " htmlspecialchars(Semail). "<br>";
```

#### form_post.html
```http
<!-- form_post.html -->
<html>
<body>
<h2>Formulário POST</h2>
<form action="process_post.php" method="POST">
Usuário: <input type="text" name="usuario"><br><br>
Senha: <input type="password" name="senha"><br><br>
<input type="submit" value="Registrar">
</form>
</body>
</html>
```

#### process_post.php
```http
<!-- process_post.php -->
<?php
??
Susuario = $_POST['usuario'];
Ssenha = $_POST['senha'];
echo "<h2>Dados Recebidos via POST</h2>";
echo "Usuário: ". htmlspecialchars(Susuario). "<br>";
echo "Senha: ". htmlspecialchars($senha). "<br>";
```

## Ataque de força bruta
- BURP SUITE (Kali) e Foxproxy (Mozila)
