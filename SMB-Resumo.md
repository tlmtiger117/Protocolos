# 29/04/26
# SMB(server mensage block)

- SMB(server mensage block/bloco de mensages do servidor): Protocolo muito utilizado em redes Windows para o compartilhamento de arquivos e pastas na rede.

   - 445 (SMB direto moderno)
   - 139 (SMB antigo via NetBIOS)

- sintaxes:

   - Windows:

      - acessar o server: \\<"ip ou nome do pc">
      - acessar pasta específica: \\192.168.0.10\<pasta>\<subpasta>...

   - via Linux: smbclient -L //IP_DO_PC -U usuário
  
      -L: lista os arquivos e pastas existentes no host alvo(disk)
      -U: usuário de login no SMB
      -m SMB2(protocolo recente, o SMB1 usado naturalmente pelo SMB1 que já é ultrapassado)

- comandos:

    - cd > acessa pasta(funciona se for acessado via smbclient linux) se não, o Windows não tem um cd no SMB(especifica tudo no "\..\")
    - ls > lista arquivos
    - get arquivo > baixa
 
      
    - put arquivo → envia

      
