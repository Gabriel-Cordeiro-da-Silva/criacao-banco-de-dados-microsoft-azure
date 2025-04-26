# Criando uma Instância de Banco de Dados SQL no Azure 🚀

## 📚 Sobre o Projeto
Este repositório documenta o processo de criação e configuração de uma instância de Banco de Dados SQL no **Microsoft Azure**. 
Aqui você encontrará resumos, anotações práticas, dicas de configuração e boas práticas para futuras implementações.

## 🎯 Objetivos
- Documentar de forma clara e estruturada o processo de criação de um Banco de Dados SQL no Azure.
- Utilizar o GitHub como ferramenta de compartilhamento de conhecimento técnico.

## 🛠️ Passo a Passo

### 1. Acesso ao Portal Azure
- Acesse [portal.azure.com](https://portal.azure.com) com sua assinatura, no meu caso: Azure for Students.

### 2. Criação de Banco de Dados SQL
- No menu lateral, clique em **"Criar um recurso"** > **"Banco de Dados"** > **"Banco de dados SQL"**.
- Preencha as informações principais:
  - **Assinatura:** Azure for Students
  - **Grupo de Recursos:** (crie novo ou selecione existente)
  - **Nome do Banco de Dados:** Ex: `teste`
  - **Servidor:** Criar novo servidor lógico (Ex: `mc`)
  - **Localização:** Brazil South
  - **Camada de Preço:** (escolha a mais básica para reduzir custos)
- Configure a autenticação de acesso:
  - Usuário de administrador e senha fortes.
- (Opcional) Ajuste configurações adicionais de rede, segurança e backups.

### 3. Revisar + Criar
- Após configurar tudo, clique em **"Revisar + Criar"**.
- Verifique o custo estimado e clique em **"Criar"**.

### 4. Acesso e Gerenciamento
- Acesse o banco de dados via **Azure Cloud Shell**:
  - Escolha **Bash** e configure se for a primeira vez.
- Conecte-se ao banco via `sqlcmd` ou ferramentas externas usando a **cadeia de conexão** gerada.

### 5. Comandos Úteis no Azure Cloud Shell
```bash
# Mostrar a cadeia de conexão para sqlcmd
az sql db show-connection-string --name teste --client sqlcmd --server mc.database.windows.net
```

```bash
# Consultar detalhes do banco de dados
az sql db show --name teste --server mc --resource-group MC
```

## 📚 Recursos de Estudo
- [Início rápido: Criar uma Instância Gerenciada de SQL do Azure](https://learn.microsoft.com/pt-br/azure/azure-sql/managed-instance/instance-create-quickstart?view=azuresql&tabs=azure-portal)
- [Criar seu banco de dados SQL no Azure](https://learn.microsoft.com/pt-br/training/modules/provision-azure-sql-db/3-create-your-database)

---

## 🧠 Glossário
Em caso de dúvidas sobre os termos técnicos utilizados, consulte o [glossário de termos](./glossario.md).

---

## 💡 Dicas para Economizar no Azure
- Escolha o menor tamanho de instância possível no início.
- Utilize camadas de preço mais econômicas (ex: camada básica).
- Configure desligamento automático se possível.
- Exclua recursos que não estiver utilizando (servidores, bancos, IPs públicos).
- Monitore o custo em **Cost Management + Billing** no portal Azure.

---

> **Autor:** Gabriel Cordeiro
