# Como Acessar do Computador do Cliente

Detectamos que o comando automático de firewall falhou (permissão negada). Você precisará permitir o acesso manualmente se ainda não tiver feito.

## 1. Endereço de Acesso

No computador do cliente, abra o navegador (Chrome/Edge) e digite exatamente este endereço:

### 👉 **http://192.168.3.69:3002**

> **Atenção:** Se o navegador alertar sobre "Site não seguro" (por ser HTTP), pode prosseguir. É normal em redes locais.

## 2. Se não carregar (Tela Branca ou "Não foi possível conectar")

É muito provável que o **Firewall do Windows** no SEU computador (onde o servidor está rodando) esteja bloqueando a conexão de fora.

### Como corrigir manualmente:

1. Pressione a tecla `Windows` e digite **"Firewall e Proteção de Rede"**.
2. Clique em **"Permitir um aplicativo pelo Firewall"**.
3. Clique no botão **"Alterar configurações"** (pode pedir senha de admin).
4. Procure na lista por **"Node.js JavaScript Runtime"** (pode ter mais de um).
5. **Marque todas as caixas** (Privado e Público) para todos os "Node.js" que encontrar.
6. Clique em **OK**.

Tente acessar novamente no computador do cliente.

## 3. Teste Rápido

Para saber se o problema é o firewall ou o sistema:
1. Pegue seu celular.
2. Desligue os dados móveis (4G) e conecte no **mesmo Wi-Fi** desse computador.
3. Acesse `http://192.168.3.69:3002` pelo celular.
4. Se funcionar no celular, o problema pode estar na rede do computador do cliente ou firewall dele.
