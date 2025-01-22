# 🎯 SEToolkit para Phishing de Senhas do Facebook

---

## 📝 Descrição do Projeto
Este projeto demonstra como usar o **Social-Engineer Toolkit (SEToolkit)** para criar uma página de phishing que simula o login do Facebook.  
⚠️ **Este projeto deve ser utilizado apenas para fins educacionais, éticos e em ambientes controlados, com autorização explícita.**

---

## ✅ Pré-requisitos

Antes de começar, certifique-se de ter o seguinte:

### 🛠️ Softwares Necessários
- **[VirtualBox](https://www.virtualbox.org/):** Para criar a máquina virtual.  
- **[Kali Linux ISO](https://www.kali.org/get-kali/):** Sistema operacional para realizar os testes.  
- **SEToolkit:** Ferramenta pré-instalada no Kali Linux para engenharia social.  

### 🖥️ Requisitos de Hardware
- **CPU:** Com suporte à virtualização (ativar no BIOS, se necessário).  
- **RAM:** 4 GB (mínimo) ou mais recomendado.  
- **Disco:** 20 GB de espaço disponível.  

---

## 🛠️ Ferramentas Utilizadas

| Ferramenta         | Função                                                         |
|---------------------|----------------------------------------------------------------|
| **VirtualBox**      | Gerenciar a máquina virtual.                                   |
| **Kali Linux**      | Sistema operacional para testes de penetração.                |
| **SEToolkit**       | Criar e gerenciar páginas de phishing.                        |
| **Apache**          | Servidor web para hospedar a página clonada.                  |

---

## 🚀 Configuração do Ambiente

### 1️⃣ Instale e configure o Kali Linux no VirtualBox
1. Baixe e instale o **VirtualBox**.
2. Baixe a imagem ISO do **Kali Linux** no [site oficial](https://www.kali.org/get-kali/).
3. No VirtualBox, crie uma nova máquina virtual:
   - **Nome:** Kali Linux  
   - **Sistema Operacional:** Linux (Debian 64-bit).  
   - **RAM:** 4 GB.  
   - **Disco:** 20 GB (dinamicamente alocado).  
4. Inicie a máquina virtual com a ISO do Kali Linux e siga o processo de instalação.

---

### 2️⃣ Atualize o Kali Linux
Após instalar o Kali Linux, atualize o sistema:
```bash
sudo apt update && sudo apt upgrade -y
