### Instalação do Terminal Tabby

1. **Baixar o Instalador do Tabby**:
   - Acesse o site oficial do Tabby em [Tabby](https://tabby.sh/).
   - Selecione a versão adequada para o seu sistema operacional (Windows, macOS ou Linux).

2. **Instalar o Tabby**:
   - No Windows, execute o instalador baixado e siga as instruções na tela.
   - No macOS ou Linux, você pode precisar dar permissões de execução ao arquivo baixado antes de executá-lo.

3. **Configurar o Terminal Tabby (Opcional)**:
   - Após a instalação, abra o Tabby.
   - Acesse as configurações para personalizar o terminal de acordo com sua preferência (cores, fontes, atalhos de teclado, etc.).

### Configuração do On My Posh

1. **Instalar o On My Posh**:
   - O On My Posh é um framework de prompt para o PowerShell, mas também pode ser usado em outros shells.
   - Para Windows, você pode instalar o On My Posh via winget com o comando:
     ```cmd
     winget install JanDeDobbeleer.OhMyPosh -s winget
     ```
   - Para MacOS, você pode instalar o On My Posh via brew com o comando:
     ```brew
     brew install jandedobbeleer/oh-my-posh/oh-my-posh
     ```
   - Para Linux, você pode instalar o On My Posh via curl com o comando:
     ```curl
     curl -s https://ohmyposh.dev/install.sh | bash -s
     ```

2. **Configurar o On My Posh**:
   - Após a instalação, você pode configurar o On My Posh editando o perfil do seu terminal.
   - Para o Windows você pode localizar o caminho `C:\Users\SeuUser\AppData\Local\clink`.
   - Adicione um script oh-my-posh.lua no diretório com o seguinte codigo:
     ```lua
     load(io.popen('oh-my-posh init cmd --config "C:\\{Local do seu Tema}\\theme.omp.json"'):read("*a"))()
     ```
   - O `theme.omp.json` deve ser substituído pelo caminho do tema JSON que você deseja usar. Você pode encontrar temas prontos no [GitHub do On My Posh](https://github.com/JanDeDobbeleer/oh-my-posh) ou baixar o que esta o tema que eu personalizei [Tema Personalizado](https://github.com/JanDeDobbeleer/oh-my-posh).

3. **Aplicar as Mudanças**:
   - Reinicie o terminal para aplicar as mudanças.
   - Se tudo estiver configurado corretamente, você verá o novo prompt do On My Posh.

### Notas Adicionais

- **Permissões de Execução**: No macOS e Linux, você pode precisar conceder permissões para executar scripts. Isso pode ser feito com `chmod +x <nome-do-arquivo>`.
- **Customização**: O On My Posh é altamente personalizável. Explore diferentes temas e configurações para adequá-lo ao seu gosto.
