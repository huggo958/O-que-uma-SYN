# O que é uma SYN?
SYN (Synchronize) é um flag no protocolo TCP usado para iniciar uma conexão entre dois computadores.

## - O famoso "aperto de mãos" em tcp
    Cliente -> SYN -> Servidor
    Cliente -> SYN-ACK -> Servidor 
    Cliente -> ACK -> Servidor
    
## SYN em segurança
    1SYN -> Início de conexão
    SYN-ACK -> Resposta do servidor 
    ACK -> Confirmação do cliente 

## O flag SYN
    • Bit número 1 nas posições dos flags 
    • Valor = 1 quando estiver ativo, 0 quando inativo
    • Sempre combinado com Sequence Number

## Como ver SYN no Whireshark
- Filtro para ver SYNs
  
    tcp.flags.syn == 1 and tcp.flags.ack == 0 (apenas o pacote SYN)
    tcp.stream eq 0 (mostra toda uma conversa, tree-way handshake completo)

- 
