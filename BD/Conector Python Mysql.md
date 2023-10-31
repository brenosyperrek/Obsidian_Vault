
```python
# Importar o módulo mysql.connector
import mysql.connector

# Definir uma função que recebe o nome do banco de dados, o usuário, a senha e o host como parâmetros
def conectar_mysql(db, user, password, host):
  # Tentar estabelecer uma conexão com o banco de dados usando os parâmetros fornecidos
  try:
    # Criar um objeto de conexão usando o método connect do módulo mysql.connector
    conexao = mysql.connector.connect(database=db, user=user, password=password, host=host)
    # Retornar o objeto de conexão
    return conexao
  # Se ocorrer algum erro, capturar a exceção e imprimir a mensagem de erro
  except mysql.connector.Error as e:
    print(f"Erro ao conectar ao banco de dados: {e}")
    # Retornar None
    return None
```
