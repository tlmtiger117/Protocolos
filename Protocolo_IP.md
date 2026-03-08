# 08/03/26
# Protocolo IP

- O que é: Protocolo ip(Internet Protocol) é uma regra utilizada para encaminhar dados entre redes diferentes(Sub-redes e WANs).
   - IP: IP, ou endereço ip, é basicamente o identificador virtual de um dispositivo numa rede.
     
      - É utilizado para mandar dados para redes diferentes.
      - Ele não processa os dados, apenas os encaminham para o ip de destino nas camadas superiores(tranporte).

- Encaminhamento de dados: Ele carrega os dados das camadas superiores(TCP,UDP...), mas como sua função é encaminhar os dados
  e não ler/processar eles, ele apenas os encaminham para o destino (mas ele sabe que tem algo alí).

   - Quem processar esses dados carregados pelo protocolo ip são os hosts de destino, que recebem os dados e manda de vola
      a quem os enviou(processo inverso, processa os dados e manda devolta a quem mandou).

- Resumo: Protocolo ip é uma regra utilizada para encaminhar dados entre redes diferentes atravez dos endereços virtuais dos hosts
           (Endereço ip).
  
    - Função: Entregador(SÓ MANDA OS DADOS PARA AS CAMADAS ACIMA, NÃO LÊ OS DADOS).


- [PROTOCOLO ARP] -> link para o meu estudo sobre o protocolo ARP (camada 2 e como ela funciona):
    - link: https://github.com/tlmtiger117/Protocolos/blob/main/Protocolo_ARP.md
     
