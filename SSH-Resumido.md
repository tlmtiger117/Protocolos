# 29/04/26
# SSH(Secure shell)

- ssh: serviço de acesso remoto comumente utilizado em sistemas unix/Linux
   - Porta padrão: porta 22

   - Shell: tradutor de comandos, traduz o que o user digitou pro processador entender e executar o comando.
      - Fluxo: comando -> RAM(armazena o comando e repassar para CPU) -> CPU(processa/entende o que foi pedido, executa e
         retorna o resultado para o cliente)

   - Utiliza um programa para processar e cifras os dados enviados do src e dst.


- Sintaxe: ssh usuario@host
   - -p: especifica uma porta(se necessário)
   - -i: especifica uma chave privada(permite acessar sem precisar digitar senha).
      - isso só é possível se o host alvo permitir. ele pode adcionar uma passfrase ou
        simplemente pedir chave + senha + passfrase(depende doq ue o host quer).


- o que testar:
   - testar credenciais coletadas
   - testar users comuns (wordlist)
   - testar keys privadas (ficam em .ssh) no diretório "/home/<user>"
   - modos diferentes de cifra(as vezes é necessério trocar). "-o"


