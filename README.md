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
   - Nome: Kali Linux  
   - Sistema Operacional: Linux (Debian 64-bit).  
   - RAM: 4 GB.  
   - Disco: 20 GB (dinamicamente alocado).  
4. Inicie a máquina virtual com a ISO do Kali Linux e siga o processo de instalação.

---

### 2️⃣ Atualize o Kali Linux
Após instalar o Kali Linux, atualize o sistema com o comando:
sudo apt update && sudo apt upgrade -y

---

### 3️⃣ Configure o Servidor Apache
O Apache será usado para hospedar a página de phishing. Para ativá-lo, use os comandos:
sudo systemctl start apache2
sudo systemctl enable apache2

---

### 4️⃣ Inicie o SEToolkit
Abra o terminal no Kali Linux e inicie o Social-Engineer Toolkit com o comando:
setoolkit

Caso seja a primeira vez que você o utiliza, aceite os termos de uso para prosseguir.

---

## 🎯 Criação de Página de Phishing para o Facebook

### 1️⃣ Configuração no SEToolkit
1. No menu inicial do SEToolkit, selecione a opção:
1) Social-Engineering Attacks

2. Em seguida, escolha:
2) Website Attack Vectors

3. Para capturar credenciais, selecione:
3) Credential Harvester Attack Method

4. Escolha o método de clonagem:
2) Site Cloner

5. Insira o endereço IP da sua máquina virtual Kali Linux. Para descobrir o IP, use o comando:
ifconfig
Exemplo de entrada: 192.168.0.100

6. Insira a URL que deseja clonar. Neste caso, o URL do Facebook:
https://www.facebook.com

O SEToolkit irá criar uma cópia exata da página de login do Facebook e configurará o servidor Apache para hospedar essa página falsa.

---

### 2️⃣ Testando a Página
1. No navegador de outro dispositivo na mesma rede (ou na própria VM), acesse o endereço IP configurado no SEToolkit.  
Exemplo: http://192.168.0.100

2. A página clonada do Facebook será exibida. Ao inserir credenciais de teste, elas serão capturadas pelo SEToolkit.

---

## 🔍 Verificando Credenciais Capturadas

As credenciais capturadas serão armazenadas em um arquivo no servidor Apache. Use o seguinte comando para localizar e visualizar os dados:

1. Acesse o diretório onde as informações são salvas:
cd /var/www/html

2. Veja o conteúdo do arquivo com as credenciais capturadas:
cat harvester_*.txt

O arquivo conterá os dados inseridos, como nomes de usuário e senhas.

---

## ⚠️ Avisos Importantes

- Somente para uso educacional e ético.  
- Qualquer uso indevido desta ferramenta é ilegal e pode resultar em sérias penalidades legais.  
- Utilize este projeto para conscientizar sobre os perigos de ataques de phishing.

---

## 🛠️ Contribuições

Este é um projeto para o curso de Santander Bootcamp Cibersegurança #2 da DIO.


