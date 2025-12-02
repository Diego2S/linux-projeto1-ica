# 📁 Script de Configuração de Ambiente — Linux (IAC)

Este repositório contém o script **`iacl.sh`**, responsável por automatizar a criação de diretórios, grupos, usuários e permissões em um ambiente Linux.  
O objetivo é facilitar a implementação de uma infraestrutura como código (IaC) simples para treinamentos e ambientes de estudo.

---

## 🚀 Sobre o Script

O script `iacl.sh` realiza:

### 🗂️ Criação de Diretórios

- `/publico`
- `/adm`
- `/ven`
- `/sec`

---

### 👥 Criação de Grupos

- `GRP_ADM`
- `GRP_VEN`
- `GRP_SEC`

---

### 👤 Criação de Usuários

Usuários criados com:

- Diretório home (`-m`)
- Shell Bash (`/bin/bash`)
- Senha criptografada com SHA-512
- Inclusão no grupo correspondente

#### Lista de usuários

**GRP_ADM**
- carlos  
- maria  
- joao  

**GRP_VEN**
- debora  
- sebastiao  
- roberto  

**GRP_SEC**
- josefina  
- amanda  
- rogerio  

---

### 🔒 Permissões Aplicadas

- `/adm` → proprietário `root:GRP_ADM` | permissão `770`
- `/ven` → proprietário `root:GRP_VEN` | permissão `770`
- `/sec` → proprietário `root:GRP_SEC` | permissão `770`
- `/publico` → permissão `777` (acesso total)

---

## 📄 Como Executar

1. Salve o script como `iacl.sh`
2. Conceda permissão de execução:

```bash
chmod +x iacl.sh
