# Chatbot com Criptografia Ponta a Ponta (RSA)

## Descrição
Este projeto implementa um chatbot baseado na arquitetura Cliente-Servidor com criptografia ponta a ponta utilizando o algoritmo RSA. O sistema permite que um cliente envie mensagens criptografadas para um servidor, que as recebe, exibe a mensagem criptografada e a mensagem decriptada.

## Tecnologias Utilizadas
- Python
- Sockets
- Criptografia RSA

## Professor e Disciplina
- **Professor:** Ivonildo Neto
- **Disciplina:** Segurança da Informação

## Componentes
- **Marcel Gustavo**
- **Mateus Omar**

---

## Como Executar o Projeto

### 1. Configurar e Executar o Servidor
1. Baixe ou clone o repositório.
2. Navegue até a pasta do projeto.
3. Execute o seguinte comando para iniciar o servidor:
   ```sh
   python server.py
   ```

### 2. Configurar e Executar o Cliente
1. Em outro terminal, navegue até a pasta do projeto.
2. Execute o seguinte comando para iniciar o cliente:
   ```sh
   python client.py
   ```

3. O cliente irá se conectar ao servidor e iniciar a troca de mensagens criptografadas.
4. Para encerrar a conversa, digite `adeus`.

---

## Como Funciona a Criptografia RSA
O sistema utiliza o algoritmo RSA para criptografar e decriptar as mensagens enviadas entre cliente e servidor. Cada lado gera um par de chaves:
- **Chave Pública** (é enviada para o outro lado e usada para criptografar mensagens).
- **Chave Privada** (é mantida secreta e usada para decriptar mensagens recebidas).

Fluxo de comunicação:
1. O servidor gera um par de chaves RSA.
2. O cliente gera um par de chaves RSA.
3. O servidor e o cliente trocam suas chaves públicas.
4. Cada mensagem é criptografada com a chave pública do destinatário antes de ser enviada.
5. O destinatário decripta a mensagem recebida com sua chave privada.

---

## Exemplo de Execução
### No servidor:
```sh
Conexão estabelecida: ('127.0.0.1', 54321)
Sua chave pública: (e, n)
Sua chave privada: (d, n)
Chave pública do cliente: (e, n)

Mensagem do cliente criptada: [299, 500, ...]
Mensagem do cliente decriptada: "Olá, servidor!"
```

### No cliente:
```sh
Para encerrar a conversa digite 'adeus'.

Sua chave pública: (e, n)
Sua chave privada: (d, n)
Chave pública do servidor: (e, n)

 -> Olá, servidor!
Mensagem do servidor criptada: [320, 512, ...]
Mensagem do servidor decriptada: "Olá, cliente!"
```

---

## Licença
Este projeto é de uso educacional e foi desenvolvido para a disciplina de Segurança da Informação.

