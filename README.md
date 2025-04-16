# Conteúdo do Script `iacl.sh`

O script `iacl.sh` contém o seguinte código:

```bash
#!/bin/bash

# Criando diretórios...
echo "Criando diretórios..."
mkdir /scripts/publico
mkdir /scripts/adm
mkdir /scripts/ven
mkdir /scripts/sec

# Criando grupos de usuários...
echo "Criando grupos de usuários..."
groupadd GRP_ADM
groupadd GRP_VEN
groupadd GRP_SEC

# Criando usuários...
echo "Criando usuários..."

# Grupo ADM
useradd carlos -m -s /bin/bash -p $(openssl passwd -6 Senha123) -G GRP_ADM
useradd maria -m -s /bin/bash -p $(openssl passwd -6 Senha123) -G GRP_ADM
useradd joao -m -s /bin/bash -p $(openssl passwd -6 Senha123) -G GRP_ADM

# Grupo VEN
useradd debora -m -s /bin/bash -p $(openssl passwd -6 Senha123) -G GRP_VEN
useradd sebastiana -m -s /bin/bash -p $(openssl passwd -6 Senha123) -G GRP_VEN
useradd roberto -m -s /bin/bash -p $(openssl passwd -6 Senha123) -G GRP_VEN

# Grupo SEC
useradd josefina -m -s /bin/bash -p $(openssl passwd -6 Senha123) -G GRP_SEC
useradd amanda -m -s /bin/bash -p $(openssl passwd -6 Senha123) -G GRP_SEC
useradd rogerio -m -s /bin/bash -p $(openssl passwd -6 Senha123) -G GRP_SEC

# Especificando as permissões do diretório...
echo "Especificando as permissões do diretório..."
chown carlos:GRP_ADM /scripts/adm
chown debora:GRP_VEN /scripts/ven
chown josefina:GRP_SEC /scripts/sec

chmod 770 /scripts/adm
chmod 770 /scripts/ven
chmod 770 /scripts/sec
chmod 755 /scripts/publico

# Mensagem final
echo "Fim."
