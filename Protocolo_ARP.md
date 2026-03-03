# 02/03/26
# Protocolo ARP

  - Camada 2(enlace):Se refece a conexão(elance/amarração) entre 2 dispositivos.
    - Isso permite o envio/recebimento de frames Ethernet(MAC de envio, destino, correção de error e payload).
    - CRC(Check de Redundância Cíclica) reposnsável por anailisar os estados dos pacotes(estado ruim ou não).
        

- O que é: ARP(Address resolution procol) é um protocolo responsável por descobrir o endereço de fábrica de um dispositivo
             atravéz do seu endereço virtual(IP)
  
    
- Como funciona: Quando um Dispositivo utilizando IP não sabe o MAC de um dispositivo da mesma rede ele:
      
   - 1° Manda uma pergunta geral na rede(broadcast), falando "se o ip x estiver nesta rede, manda ele mandar seu MAC pra mim".
        
   - 2° Se o dispositivo estiver na mesma rede, ele reponde de volta(unicast) pra quem perguntou:
        "ei, eu sou o ip 'x', esse é o meu MAC".
        
   - 3° No lado de quem perguntou, o endereço MAC do dispositivo perguntado é adicionado a tabela arp
        (tabela temporária que mostra os hosts que você se comunicou recentemente na rede LAN).
  
        
 - O que são Broadcast,unicast e ethernet:
     
  - 1° Broadcast: Não é um dispositivo, mas sim, um nome dado a um tipo de pergunta que um host faz numa rede local.
    - Broadcast tem a função de perguntar pra rede inteira algo(nesse caso, "qual ip tem MAC 'x'").
             
        
  - 2° Unicast: Não é um dispositivo, é um nome dado a um tipo de resposta única dada por um host (unicast).
    - Resposta enviada a quem perguntou, isso é unicast(resposta direta a quem perguntou).
    - (não é somente em relação a ARP, mas em contextos gerais da rede também).
      

 - 3° Ethernet: É um tipo de pacote utilizado em redes LAN que inclui:
    - MAC de origem
    - MAC de destino
    - payload(conteúdo do pacote)
    - CRC(Check de Redundância Cíclica), é um mecanismo de detecção e errors utilizado em pacotes em redes LAN.
             
    - Assim, permitindo a comunicação e transferência e recebiemento de dados em redes LAN.


- Fluxo dessa comunicação:

     - H1:"quem te ip 'x'? se estiver na minha rede, manda seu MAC aí..."

     - H2:"blz, eu sou o 'ip x', aqui meu MAC"

     - H1:"perfeito, armazenando temporariamente seu MAC na minha tabela de conexões arp(comunicação entre hosts da mesma LAN"

     - H1:"ok, já posso me comunicar internamente com esse host(pacotes ethernet)".

- [!] Sempre use sniffer como "wireshark" para a analise real de pacotes. Isso muda muito sua visão de como as coisas realmente
      funcionam na rede.

        


        
