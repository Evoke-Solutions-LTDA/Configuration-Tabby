### Instalação do Terminal Tabby

![image](https://github.com/Evoke-Solutions-LTDA/Configuration-Tabby/assets/47836230/76e0fe5c-4ea4-4ba4-a4c2-85e63c736f33)


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
   - Para Windows, você pode instalar o On My Posh via winget com o comando: [Referência](https://ohmyposh.dev/docs/installation/windows)
     ```cmd
     winget install JanDeDobbeleer.OhMyPosh -s winget
     ```
   - Para MacOS, você pode instalar o On My Posh via brew com o comando: [Referência](https://ohmyposh.dev/docs/installation/macos)
     ```brew
     brew install jandedobbeleer/oh-my-posh/oh-my-posh
     ```
   - Para Linux, você pode instalar o On My Posh via curl com o comando: [Referência](https://ohmyposh.dev/docs/installation/linux)
     ```curl
     curl -s https://ohmyposh.dev/install.sh | bash -s
     ```

2. **Configurar o On My Posh no Windows**:
   - Após a instalação, você pode configurar o On My Posh editando o perfil do seu terminal.
   - Para o Windows você pode localizar o caminho `C:\Users\{Seu User}\AppData\Local\clink`.
   - Adicione um script oh-my-posh.lua no diretório com o seguinte codigo:
     ```lua
     load(io.popen('oh-my-posh init cmd --config "C:\\{Local do seu Tema}\\theme.omp.json"'):read("*a"))()
     ```
   - O `theme.omp.json` deve ser substituído pelo caminho do tema JSON que você deseja usar. Você pode encontrar temas prontos no [GitHub do On My Posh](https://github.com/JanDeDobbeleer/oh-my-posh) ou baixar o que esta o tema que eu personalizei [Tema Personalizado](https://github.com/Evoke-Solutions-LTDA/Configuration-Tabby/blob/main/evoke.omp.json).
  
   ### Mudando o Tema do Oh My Posh no macOS e Linux

   1. **Localizar o Arquivo de Perfil do Shell**: 
      - Identifique qual shell você está utilizando (Bash, Zsh, ou Fish). 
      - Para o Bash, o arquivo de perfil é geralmente `~/.bashrc` ou `~/.bash_profile`.
      - Para o Zsh, é `~/.zshrc`.
      - Para o Fish, é `~/.config/fish/config.fish`.

   2. **Editar o Arquivo de Perfil**:
      - Abra o arquivo de perfil em um editor de texto. Por exemplo, `nano ~/.bashrc` para editar o `.bashrc` no Bash.
      - Localize a linha que inicializa o Oh My Posh, algo como:
      ```bash
      eval "$(oh-my-posh init bash --config /path/to/your/theme.omp.json)"
      ```
      Substitua `/path/to/your/theme.omp.json` pelo caminho do tema desejado.
   

3. **Aplicar as Mudanças**:
   - Reinicie o terminal para aplicar as mudanças.
   - Se tudo estiver configurado corretamente, você verá o novo prompt do On My Posh.

### Notas Adicionais

- **Permissões de Execução**: No macOS e Linux, você pode precisar conceder permissões para executar scripts. Isso pode ser feito com `chmod +x <nome-do-arquivo>`.
- **Customização**: O On My Posh é altamente personalizável. Explore diferentes temas e configurações para adequá-lo ao seu gosto.
