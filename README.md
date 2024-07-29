# Repositório APT Não-Oficial Matugen

Repositório APT Não-Oficial do [Matugen](https://github.com/InioX/matugen).

Use este repositório para instalar e atualizar o pacote Matugen com facilidade usando o APT.

Antes de confiar neste repositório, verifique a integridade dos arquivos e considere sua segurança primeiro. Crie seu próprio repositório APT usando este como base ou utilize o meu que buscará atualizações diariamente.

## Requisitos

* Debian/Ubunto ou qualquer distro derivado destes.

## Como instalar o repositório APT

Para que o APT identifique este repositório e seja capaz de instalar e atualizar o Matugen você deve executar os códigos abaixo.

```shell
wget -qO- https://maeglithier.github.io/matugen-apt/pubkey.asc | sudo gpg --dearmor -o /usr/share/keyrings/matugen-archive-keyring.gpg
echo "deb [arch=amd64 signed-by=/usr/share/keyrings/matugen-archive-keyring.gpg] https://maeglithier.github.io/matugen-apt stable main" | sudo tee /etc/apt/sources.list.d/matugen.list >/dev/null
sudo apt update
sudo apt install matugen -y # Agora você está pronto para instalar e atualizar sempre que uma nova versão lançar.
```

## Como faço para desinstalar este repositório?

Para remover este repositório e sua chave pública você deve executar os códigos abaixo.

```shell
sudo apt remove matugen # Apenas se você ainda não desinstalou o matugen. Neste caso, desinstale primeiro.
sudo rm /usr/share/keyrings/matugen-archive-keyring.gpg
sudo rm /etc/apt/sources.list.d/matugen.list
```

## Checksum

e7c72b1168403bad71b4ca3851ded85c36c8b319f46a2b530886b1c2199e3041  pool/main/m/matugen/matugen_2.3.0_amd64.deb

## Copyright

O instalador do Matugen (arquivos deb) é compilado usando os binários oficiais, e em respeito a licença oficial são distribuidos sob a licença GPL-2.0.
