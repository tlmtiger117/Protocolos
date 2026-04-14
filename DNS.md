# 14/04/26
# Como funciona o portocolo DNS

- DNS: Domain Name System, utilizado para consultar(perguntar) servidores externos(sites/domínios) seu endereço para acessa-los.
   - Isso  inclui nome so site (ex: site.com) ou o endereço, o que te permite acessa-lo na internet (ex: 224.234.321.12)
     

- Tipos de servidores DNS:
  
   - 1° Resolver (recursivo):
   - Ex: Google Public DNS
      - Recebe a requisição do cliente (seu PC)
      - Resolve tudo pra você
      - Faz consultas iterativas (dados enviados por você, pegos pelo DNS e enviados devolta para você).
      - É o “intermediário inteligente”
        

    - 2° Root Servers(repassa os dados para quem sabe):
      - Topo da hierarquia(.com,.br.org...)
      - Não sabem o IP final
      - Dizem: “vai pro TLD(camada superior) correta (.com, .org…)”

        
    - 3° TLD Servers(te manda os server autoritativos do domínio) domínios = ".com", ".br", etc...
       - Ex: "domínio.br"
       - Apontam para o servidor autoritativo
       - Também não dão a resposta final (na maioria dos casos)


    - 4° Servidor Autoritativo:
      - O “dono da verdade”
      - Contém os registros reais (A, MX, TXT…)
      - Dá a resposta final
     

    - Fluxo completo (juntando tudo):
       - Seu PC → DNS (recursivo)
       - Resolver → Root
       - Root → TLD 
       - TLD → Autoritativo
       - Autoritativo → resposta final
     

         
