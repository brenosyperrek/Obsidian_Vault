- Acesse o MySQL pelo Prompt de comando:

```bash
sudo mysql -u root
```

* Em seguida você irá executar o comando para alterar a senha do seu usuário root. Caso você queira deixar o usuário sem senha, não informe nada no campo `password`:
   
```sql
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
```
 
* Em seguida, você irá executar um comando que faz com que o servidor recarregue as tabelas de permissões e coloque suas novas alterações em vigor:

```sql
FLUSH PRIVILEGES;
```
 
* Em seguida reinicie o serviços do MySQL:

```bash
sudo systemctl restart mysql
```
