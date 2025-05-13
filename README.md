# 🌐 Criando sua Primeira Máquina Virtual na Azure

Passo a passo para criar uma máquina virtual na Azure

## ⚙️ Resumo

- Navegar pelo portal da Azure
- Criar uma máquina virtual Linux (Ubuntu)
- Acessar a VM via SSH
- Fazer as configurações iniciais
- Entender o básico da segurança e gerenciamento

## 📌 Passo a Passo

### 1. Acesse o portal Azure

Vá para [portal.azure.com](https://portal.azure.com) e entre com sua conta (ou crie uma gratuita). Você verá algo parecido com isso:

![image](https://github.com/user-attachments/assets/7cadce90-6775-4b23-9862-a2076bb62d8c)


### 2. Clique em "Criar um recurso" → "Máquina Virtual"

No menu lateral ou na tela inicial, clique em **"Criar um recurso"**, escolha **"Computação"** e depois **"Máquina Virtual"**.

### 3. Preencha os dados da VM

- **Grupo de recursos**: crie um novo com um nome fácil de lembrar
- **Nome da máquina virtual**: nome a ser utilizado pela máquina virtual
- **Região**: escolha a mais próxima de você
- **Imagem**: Ubuntu Server 22.04 LTS
- **Tamanho**: escolha um gratuito ou o mais barato

Veja um exemplo:

![image](https://github.com/user-attachments/assets/dc8ee616-43ae-45ad-af29-fa25c1595349)

### 4. Configure o acesso (autenticação)

- Tipo de autenticação: **Chave pública SSH**
- Nome de usuário: `azureuser` (ou outro escolhido)
- Cole sua chave pública SSH (ou gere uma no próprio portal)

### 5. Revise e crie

Clique em **"Avançar"** até a aba "Revisar + criar", confirme os dados e clique em **"Criar"**. A implantação começa e logo a VM estrará pronta.

### 6. Acesse sua VM via terminal

Abra o terminal e conecte via SSH com o IP público:

```bash
ssh azureuser@<ip_da_vm>
```

Exemplo da conexão:

![image](https://github.com/user-attachments/assets/736f8ef6-5ebb-489f-860b-f8c4066b3315)

## 💡 Dicas de quem testou

- Sempre desligue a VM quando não estiver usando para evitar cobranças
- Use grupos de recursos para organizar seus testes
- Salve as configurações em um template para reutilizar depois

---

Com isso, você já tem uma base sólida para criar ambientes na nuvem com a Azure. Teste, quebre, recrie. É assim que se aprende. 🚀
