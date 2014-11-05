# Scripts para instalação do Fedora num MacBook

## Resumo

Os procedimentos que eu descrevo aqui são para me lembrar como faço a instalação do Fedora em meu próprio MacBook Pro (atualmente em `triple boot` junto com o OS X e o Windows 8.1). Para isso eu utilizo um pen drive com o instalador do Fedora e também um HD externo que contem um mirror de seus pacotes. Assim eu consigo realizar grande parte da instalação que preciso com velocidade e sem necessidade de estar conectado a Internet. Também já fiz, utilizando os scripts desse projeto, a instalação do Fedora em máquinas de amigos. Se você resolver utilizar esses scripts para montar um Fedora em teu Mac, sugiro que faça um fork desse projeto para manter tuas atualizações e/configurações para eles.

## Procedimentos

### Checar os pré-requisitos

1. O pen drive com o instalador do Fedora 20 está disponível?
2. A particão `/data` está configurada?
  1. Ela usa [HFS+](http://pt.wikipedia.org/wiki/HFS%2B) e o [journal está desabilitado](http://support.apple.com/kb/TA21053?viewlocale=en_US)?
  2. Ela tem o espaço que você precisa? (em meu caso, ela é a de número 5 na saída a seguir):
```
$ diskutil list
/dev/disk0
   #:                       TYPE NAME                    SIZE       IDENTIFIER
   0:      GUID_partition_scheme                        *180.0 GB   disk0
   1:                        EFI EFI                     209.7 MB   disk0s1
   2:                  Apple_HFS osx                     39.5 GB    disk0s2
   3:                 Apple_Boot Recovery HD             650.0 MB   disk0s3
   4:                  Apple_HFS                         35.0 GB    disk0s4
   5:                  Apple_HFS data                    80.0 GB    disk0s5
   6: 0FC63DAF-8483-4772-8E79-3D69D8477DE4               17.0 GB    disk0s6
   7:                 Linux Swap                         7.2 GB     disk0s7
```
3. O projeto `dotfiles` está em `/data/pj/Projetos/github.com/paulojeronimo/dotfiles`? Esse projeto contem o script `criar-links-data` que será utilizado pelo script `do3` deste projeto.

### Instalar o Fedora a partir do Pen Drive (ou DVD) de instalação

1. Dar boot pelo pen drive (ou DVD) de instalação do Fedora.
2. ... 

###  

<!---
vim: set ts=2 sw=2 expandtab:
-->
