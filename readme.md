## configurações do termux
```bash
pkg install curl zsh git -y
```

instalando ohmyzsh

```bash
sh -c "$(curl -fsSL <https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh>)"
```

colocando o zsh como padrão
```bash
chsh
```

usando o editor vim, abra o arquivo e adicione(na linha 12/13).
```bash
vim .zshrc
```
```bash
ZSH_THEME="imajes"
```

salve, saia, feche o termux e abra novamente.

---
## lixeira linux

crie uma pasta oculta chamada .lixeira na pasta raiz.
```bash
mkdir ~/.lixeira
```

crie um arquivo e digite:
```bash
vim ~/.srm
```
```bash
#!/bin/bash 
# Lixeira Segura 
mv $1 ~/.lixeira/
```

salve e saia do arquivo. dê as permissões para execução.
```bash
chmod +x ~/.srm
```

abra o .bashrc ou .zshrc e digite:
```bash
# LIXEIRA SEGURA 
alias rm='~/.srm'
```

salve, saia e feche o terminal.

pronto, agora ao invez de excluir os arquivos, ele vai ser movido para uma pasta oculta.

assim, evitando a exclusão de arquivos importantes.
