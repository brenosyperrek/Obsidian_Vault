
- Cria um banco de dados chamado `basquete`

```sql
CREATE DATABASE basquete;
```

- Seleciona o banco de dados `basquete`

```sql
USE basquete;
```

- - Cria uma tabela chamada `jogadores` para armazenar informações de jogadores

```sql
CREATE TABLE jogadores (
id INT AUTO_INCREMENT NOT NULL,
nome VARCHAR(255) NOT NULL,
altura INT NOT NULL,
peso INT NOT NULL,
posicao VARCHAR(255) NOT NULL,
equipe VARCHAR(255) NOT NULL,
PRIMARY KEY (id)
);
```

- - Cria uma tabela chamada `jogos` para armazenar informações de jogos

```sql
CREATE TABLE jogos (
id INT AUTO_INCREMENT NOT NULL,
data DATE NOT NULL,
hora TIME NOT NULL,
local VARCHAR(255) NOT NULL,
equipe_casa VARCHAR(255) NOT NULL,
equipe_visitante VARCHAR(255) NOT NULL,
placar_casa INT NOT NULL,
placar_visitante INT NOT NULL,
PRIMARY KEY (id)
);
```

- - Cria uma tabela chamada `estatisticas` para armazenar estatísticas de jogadores em jogos

```sql
CREATE TABLE estatisticas (
id INT AUTO_INCREMENT NOT NULL,
jogador_id INT NOT NULL,
jogo_id INT NOT NULL,
pontos INT NOT NULL,
rebotes INT NOT NULL,
assistencias INT NOT NULL,
roubos INT NOT NULL,
tocos INT NOT NULL,
faltas INT NOT NULL,
minutos INT NOT NULL,
PRIMARY KEY (id),
FOREIGN KEY (jogador_id) REFERENCES jogadores (id),
FOREIGN KEY (jogo_id) REFERENCES jogos (id)
);
```