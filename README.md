# Automação de Configuração de Diretórios e Grupos de Usuários no Linux

![Bash](https://img.shields.io/badge/Shell_Script-Bash-4EAA25?style=for-the-badge&logo=gnu-bash&logoColor=white)

Script em Bash para automatizar a criação de diretórios, grupos de usuários e usuários com permissões específicas em ambiente Linux.

---

## 📝 Descrição

Este script executa as seguintes ações:
1. Cria 4 diretórios: `/publico`, `/adm`, `/ven` e `/sec`
2. Cria 3 grupos de usuários: `GRP_ADM`, `GRP_VEN` e `GRP_SEC`
3. Cria 9 usuários divididos por grupos:
   - **GRP_ADM**: carlos, maria, joão
   - **GRP_VEN**: debora, sebastiana, roberto
   - **GRP_SEC**: josefina, amanda, rogerio
4. Define permissões:
   - **770** para diretórios de grupos (leitura/escrita/execução para dono e grupo)
   - **777** para `/publico` (acesso total para todos usuários)

---

## 🚀 Funcionalidades

- Criação automatizada da estrutura de diretórios
- Gerenciamento de usuários por grupos
- Configuração segura de senhas usando criptografia OpenSSL
- Definição de permissões para diretórios compartilhados

---

## ⚙️ Pré-requisitos

- Sistema Linux
- Privilégios de root/sudo
- `openssl` instalado (geralmente pré-instalado)

---

## 🛠️ Instalação & Uso

1. **Baixe o script**:
   ```bash
   wget https://raw.githubusercontent.com/seuusuario/repo/main/script.sh
