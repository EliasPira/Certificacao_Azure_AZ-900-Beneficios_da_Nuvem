# ☁️ Benefícios da Nuvem — Microsoft Azure AZ-900

![Azure Badge](https://img.shields.io/badge/Microsoft%20Azure-Cloud%20Fundamentals-blue?logo=microsoft-azure)
![DIO Badge](https://img.shields.io/badge/DIO%20Bootcamp-AZ--900%20Fundamentos-purple)
![Status](https://img.shields.io/badge/status-Em%20Desenvolvimento-yellow)
![License](https://img.shields.io/badge/license-MIT-green)

Este repositório reúne os principais conceitos e benefícios da computação em nuvem abordados no curso **AZ-900: Fundamentos do Microsoft Azure**, ministrado na plataforma [DIO](https://www.dio.me/). O conteúdo é ideal para quem está se preparando para a certificação **AZ-900** ou deseja compreender os fundamentos da nuvem e da plataforma Azure.

## 🎯 Objetivos de Aprendizagem

- Entender os principais benefícios da nuvem.
- Criar e gerenciar VMs no Azure.
- Compreender modelos de precificação e redundância.
- Aplicar boas práticas de segurança e governança.

---
## 📚 Benefícios da Computação em Nuvem

| Beneficio         | Descrição |
|-------------------|-----------|
| **Alta disponibilidade** | Garantia de funcionamento contínuo mesmo diante de falhas ou interrupções. |
| **Escalabilidade** | Ajuste dinâmico de recursos conforme a demanda, com controle de custos. |
| **Elasticidade** | Expansão ou redução automática de recursos em resposta a variações súbitas de carga. |
| **Confiabilidade** | Infraestrutura distribuída globalmente, resiliente a falhas regionais. |
| **Previsibilidade** | Consistência em desempenho e custos, apoiada pelo Azure Well-Architected Framework. |
| **Segurança** | Ferramentas robustas de proteção, com responsabilidade compartilhada entre cliente e provedor. |
| **Governança** | Monitoramento e conformidade automatizada com políticas corporativas. |
| **Gerenciabilidade** | Controle dos recursos via portal web, CLI, APIs e PowerShell. |

---

## 🛠️ Ferramentas para Prática

### 🔹 Criar Conta Gratuita no Azure
- Acesse: [azure.microsoft.com/free](https://azure.microsoft.com/pt-br/free)

### 🔹 Instalar Azure CLI

**Windows:**
```bash
winget install Microsoft.AzureCLI
```

**macOS:**
```bash
brew install azure-cli
```

**Linux (Ubuntu/Debian):**
```bash
curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash
```

### 🔹 Verificar Instalação
```bash
az version
```

### 🔹 Autenticar-se
```bash
az login
```
---

## ⚙️ Criando uma Máquina Virtual no Portal do Azure

A seguir, um passo a passo visual para criar uma VM Windows no portal Azure, conforme a [documentação oficial da Microsoft](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/quick-create-portal):

### 1. Acesse o Portal Azure
🔗 [https://portal.azure.com](https://portal.azure.com)

### 2. Clique em “Máquinas Virtuais” e depois em “Criar”
[Passo 2 - Criar VM](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/media/quick-create-portal/select-create.png)

### 3. Preencha os detalhes básicos da VM
- Nome: `myVM`
- Região: escolha a mais próxima
- Imagem: Windows Server 2022 Datacenter
- Usuário: `azureuser` + senha segura

[Passo 3 - Configuração](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/media/quick-create-portal/basic-settings.png)

### 4. Permita portas de entrada
- RDP (3389) para acesso remoto
- HTTP (80) para servidor web

### 5. Clique em “Examinar + Criar” e depois em “Criar”
[Passo 5 - Revisar e Criar](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/media/quick-create-portal/review-create.png)

### 6. Conecte-se via RDP e instale o IIS
```powershell
Install-WindowsFeature -name Web-Server -IncludeManagementTools
```

### 7. Acesse o IP público da VM no navegador
Você verá a página padrão do IIS confirmando que o servidor está ativo.

---

## 🛡️ Modelos de Redundância e Alta Disponibilidade

| Modelo de Redundância         | Descrição | Implicações |
|-------------------------------|-----------|-------------|
| **Zona de Disponibilidade** | Distribui VMs entre datacenters distintos. | Alta tolerância a falhas regionais. |
| **Conjunto de Disponibilidade** | Agrupa VMs em racks diferentes. | Protege contra falhas locais. |
| **Instância Isolada** | Executa em hardware dedicado. | Maior isolamento e segurança. |
| **Sem Redundância** | VM padrão. | Menor custo, maior risco. |

---

## 📌 Referência

- Slides oficiais do curso AZ-900 na DIO.
- [Documentação Microsoft Learn — Criar VM no Portal](https://learn.microsoft.com/pt-br/azure/virtual-machines/windows/quick-create-portal)

---
