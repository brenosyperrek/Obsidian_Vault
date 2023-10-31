
MOSTRAR DATA DE VALIDADE DO CERTIFICADO DE LICENÇA

Logar no SAPROUTER como root

```bash
su - sncadm
./sapgenpse get_my_name -n validity
```

PARAR O SAPROUTER

```bash
./saprouter -s
```

DESCOBRIR "your distinguish name"

```bash
./sapgenpse get_my_name
```

Obs: No caso da CASAN o "your distinguish name" é : CN=saprouter, OU=0001381974, OU=SAProuter, O=SAP, C=DE

RENOMEAR OS ARQUIVOS

```bash
mv certreq certreq.old
mv cred_v2 cred_v2.old
mv local.pse local.pse.old
mv srcert srcert.old
```

GERAR A REQUISIÇÃO DO CERTIFICADO

```bash
./sapgenpse get_pse –v –r certreq –p local.pse CN=saprouter, OU=0001381974, OU=SAProuter, O=SAP, C=DE
```

Obs: Durante a execução do comando será solicitado um PIN de 4 números. Este PIN deve ser lembrado para os passos seguintes.

Obs: Um arquivo chamado "certreq" será criado.

APLICAR A REQUISIÇÃO E GERAR O CERTIFICADO

- Acessar a url [https://support.sap.com/en/tools/connectivity-tools/saprouter.html](https://support.sap.com/en/tools/connectivity-tools/saprouter.html)
- Localizar e clicar no botão "Apply for a SAProuter certificate"
- Clicar no botão "Submit CSR"
- Copiar o conteúdo do arquivo "certreq" e colar no campo disponível na página.
- Clicar no botão "Request certificate"
- Copiar o conteúdo gerado e colar em um novo arquivo texto chamado "srcert"

IMPORTAR O NOVO CERTIFICADO

```bash
./sapgenpse import_own_cert -c srcert -p local.pse
./sapgenpse seclogin -p local.pse
./saprouter.sh
```