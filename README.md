# azure-vm-project-study

# Projeto: Criação de Máquina Virtual no Microsoft Azure (Free Tier)

Este projeto documenta passo a passo o processo de criação e configuração de uma máquina virtual (VM) utilizando a camada gratuita (Free Tier) do Microsoft Azure.

---

## 📌 Objetivo

Demonstrar a criação de uma VM B1s utilizando Ubuntu Linux, adequada para práticas, hospedagem leve ou testes com serviços em nuvem, sem custos durante o período da camada gratuita.

---

## 🧰 Requisitos

- Conta Microsoft
- Cadastro na plataforma Azure (https://azure.microsoft.com/free)
- Cartão de crédito (para validação de identidade — não será cobrado)

---

## 🚀 Etapas Realizadas

### 1. Criação da Conta Free Tier

- Acesso à página do Azure Free
- Validação com cartão de crédito

### 2. Criação da Máquina Virtual

- Navegar até **"Máquinas Virtuais"**
- Clicar em **“+ Criar”**
- Preencher as abas:

#### Básico
- **Nome**: `vm-linux-projeto`
- **Imagem**: Windows Server 2022
- **Tamanho**: B1s (750h/mês gratuito)
- **Usuário**: `azureuser`
- **Autenticação**: Senha segura

#### Disco
- Disco SSD padrão

#### Rede
- Habilitar porta SSH (22) para acesso remoto

#### Marcas (opcional)
- Exemplo: `ambiente=dev`, `projeto=vm-azure`

### 3. Revisar e Criar

- Validação automática das configurações
- Implantação e inicialização

---

## 🔐 Acesso à Máquina

Com a VM em execução, o acesso foi feito via SSH:

```bash
ssh azureuser@<ip_público_da_vm>
````

#### Criação do DataBase 

### 2. Informações Básicas

Preenchi os seguintes campos:

- **Assinatura**: Free Tier
- **Grupo de Recursos**: `RG-FreeTier`
- **Nome do Banco de Dados**: `bd-projeto-vm`
- **Servidor SQL**: Criei um novo chamado `sql-server-projeto`
  - Nome único do servidor
  - Região: mesma da máquina virtual
  - Login: `adminuser`
  - Senha: definida com segurança

---

### 3. Camada de Preço

- Selecionei a opção **"Basic"** ou equivalente à camada gratuita.
- Esta opção é suficiente para testes, estudos e pequenos projetos.

---

### 4. Configuração de Rede (Firewall)

Após a criação, acessei o servidor SQL e:

- Cliquei em **"Firewalls e redes virtuais"**
- Adicionei meu IP público com o botão **"Adicionar meu IP atual"**
- Ativei a opção **"Permitir serviços do Azure a acessar o servidor"**
- Salvei as alterações


Logo apos, mostrou o quanto custaria esse serviço...
