# 14/04/26
# Como funciona o portocolo DNS

- DNS: Domain Name System, utilizado para resolver nomes domínios (A,AAAA,NS,CNAME) do endereço do site para acessa-lo.
   - Isso  inclui nome so site (ex: site.com) ou o endereço ip, o que te permite acessa-lo na internet (Ex: 224.234.321.12)

- Tipos de consultas DNS:
  
  - Recursiva → “resolve pra mim e me entrega pronto”
  - Iterativa → “não sei tudo, mas te indico o próximo passo na hierarquia de servidores DNS(.com,.br.org...)”
     - Root(repassa se seuber o TLD) → TLD(repassa pra quem sabe a resposta) → Autoritativo (→ resolve o domínio/IP)

  
   - 1° DNS (recursivo):
     
   - Ex: Google Public DNS
      - Recebe a requisição do cliente (seu PC)
      - Resolve tudo pra você
      - Faz consultas iterativas (dados enviados por você, pegos pelo DNS e enviados devolta para você).
      - É o “intermediário inteligente”   

    - 2° Root Servers(aponta para quem sabe uma parte da pergunta do user):
      
      - Topo da hierarquia(.com,.br.org...)
      - Não sabem o IP final do domínio
      - Diz: “vai pro TLD(camada superior(DNS correto)) do .com, .org…"

        
    - 3° TLD Servers(retorna os server DNS autoritativos exietentes do ".algo")
      
       - Ex: "domínio.br"
       - Apontam para o servidor autoritativo
       - Também não dão a resposta final (na maioria dos casos)


    - 4° Servidor Autoritativo:
      
      - O “dono da verdade”
      - Contém os registros reais (A, MX, TXT…)
      - Dá a resposta final
     

    - Fluxo completo (juntando tudo):
      
      - Seu PC → DNS (recursivo)
      - DNS → Root → TLD → Autoritativo
      - DNS → devolve resposta pro PC

         
