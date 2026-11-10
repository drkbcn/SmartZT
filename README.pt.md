🌐 [English](README.md) · [Español](README.es.md) · [Italiano](README.it.md) · **Português** · [Français](README.fr.md) · [Deutsch](README.de.md) · [Ελληνικά](README.el.md) · [Български](README.bg.md) · [Українська](README.uk.md)

# 🏍️ SmartZT, app não oficial para motas Zontes

[![Última versão](https://img.shields.io/github/v/release/drkbcn/SmartZT)](https://github.com/drkbcn/SmartZT/releases/latest)
[![Transferências](https://img.shields.io/github/downloads/drkbcn/SmartZT/total)](https://github.com/drkbcn/SmartZT/releases)

Uma app não oficial para motas Zontes, criada para substituir a app do
fabricante por algo mais rápido e fiável. Comunica com a câmara (DVR) da mota
por Wi-Fi e com o seu módulo keyless PKE por Bluetooth Low Energy. Funciona em
Android e, desde a 2.1, em iPhone e iPad com uma primeira **versão iOS em
testes** (ver [iOS (em testes)](#ios-em-testes)).

| Mota | Câmara | Combustível | Ecrã | Definições | Sobre |
|:-:|:-:|:-:|:-:|:-:|:-:|
| <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/dark-moto.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/dark-camera.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/dark-fuel.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/dark-screen.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/dark-settings.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/dark-about.png" width="130"> |
| <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/light-moto.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/light-camera.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/light-fuel.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/light-screen.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/light-settings.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/light-about.png" width="130"> |

O tema claro, escuro ou do sistema escolhe-se em **Definições › Tema**.

## O que faz

- **Mota**: primeiro a tua mota e o seu estado de ligação, com um único botão
  **Ligar à mota**. Os controlos de trancar, destrancar, tampa do depósito e
  assento mostram o progresso enquanto o comando é enviado, e a luz ambiente é
  controlada através do módulo PKE, com o mesmo esquema de desafio-resposta
  AES da app original.
- **Câmara**: lista e transfere os vídeos e fotos das câmaras dianteira e
  traseira do DVR, e reprodu-los na app.
- **Combustível**: um registo de abastecimentos com estatísticas de consumo e
  gráficos ao longo do tempo.
- **Ecrã**: o estado do painel (TFT) e duas formas de o usar:
  - **Duplicação de ecrã**: envia o ecrã do telemóvel para o painel da mota
    por Wi-Fi Direct, com taxa de fotogramas e bitrate ajustáveis.
  - **Android Auto** *(experimental)*: mostra o Android Auto no painel, para
    apps de mapas e música como o Waze ou o Spotify. Mais detalhes abaixo.
- **Definições da mota**: lê e altera parâmetros guardados na MCU da mota
  (método da chave, tempo de bloqueio automático, alarme ESS, alarme do travão
  de mão, etc.).
- **Garagem**: gere mais do que uma mota e alterna entre elas.
- **Configuração por QR**: o emparelhamento e as credenciais Wi-Fi
  configuram-se lendo um código QR, tal como na configuração da mota ou do
  concessionário.
- **Exportar/importar configuração**: cópia de segurança e restauro da
  configuração da app através de um código QR cifrado.
- **Atualizações**: a app consulta esta página à procura de novas versões (no
  máximo uma vez por dia) e permite transferir, adiar ou ignorar uma versão.
  **Definições › Sobre** também mostra as notas de cada versão. As versões
  Android nunca expiram.

## Android Auto (experimental)

O telemóvel funciona como a unidade principal do carro: a imagem do Android
Auto é recodificada para o painel e os toques no painel são-lhe devolvidos. O
som das indicações de navegação e a música continuam a sair pelo telemóvel
(por exemplo, para um intercomunicador Bluetooth no capacete).

- O Android Auto tem de estar instalado, e o seu *head unit server* de
  programador tem de ser iniciado à mão: abre as definições do Android Auto,
  toca em **Versão** umas dez vezes e depois usa o menu ⋮ › **Start head unit
  server**. A app tem um atalho para essas definições. O Android não deixa
  que outra app o inicie por ti.
- O ecrã do Android Auto também abre no telemóvel, onde lhe podes tocar para
  abrir apps e menus. Um botão ✕ leva-te de volta ao SmartZT sem parar a
  projeção.
- **Experimentar o Android Auto neste telemóvel** executa-o sem nenhuma mota
  ligada.
- O tamanho da imagem (800×480, 1280×720 ou 1920×1080) escolhe-se no
  separador Ecrã. Os tamanhos maiores gastam mais CPU e bateria.
- Os botões do guiador não são suportados: estas motas não os enviam.

Não foi testado em todos os telemóveis nem em todas as versões do Android
Auto, por isso podem existir problemas.

## iOS (em testes)

O SmartZT 2.1 é a primeira versão para iPhone e iPad. Está **em testes**:
podem existir problemas, e agradeço que comuniques o que não funciona.

- **A duplicação de ecrã no iOS está numa fase muito inicial.** Pode não
  arrancar, ou não mostrar imagem, em alguns telemóveis e painéis. Se falhar,
  partilha o registo da duplicação (botão de partilhar no cartão do painel, no
  separador Ecrã) e anexa-o a um
  [problema](https://github.com/drkbcn/SmartZT/issues).
- **Funciona no iOS:** Mota (trancar, destrancar, assento, tampa do depósito,
  luz ambiente, tensão da bateria), Câmara (vídeos e fotos do DVR),
  Combustível, Garagem, Definições da mota, configuração por QR e
  exportar/importar configuração.
- **Não disponível no iOS:** Android Auto, o HUD de navegação, a camada de
  proteção do ecrã e os widgets do ecrã principal. O iOS não tem Wi-Fi Direct,
  por isso ligas-te à mão ao Wi-Fi do DVR na app Definições do iOS; o SmartZT
  mostra-te o nome e a palavra-passe da rede.
- **Requisitos:** iOS 15 ou posterior (a duplicação de ecrã precisa do iOS 16
  ou posterior), um Apple ID (serve um gratuito) e um computador com Windows,
  macOS ou Linux para instalar a app.

### Instalação em iPhone ou iPad (sideloading)

O SmartZT não está na App Store. O `.ipa` da página de
[Releases](https://github.com/drkbcn/SmartZT/releases) instala-se com o teu
próprio Apple ID usando o **[Impactor](https://github.com/claration/Impactor)**,
uma ferramenta de sideloading gratuita e de código aberto:

1. Transfere `SmartZT-<versão>.ipa` da versão mais recente.
2. Instala o Impactor a partir da sua
   [página de releases](https://github.com/claration/Impactor/releases):
   - **Windows:** instala primeiro o [iTunes](https://support.apple.com/en-us/106372);
     o Impactor usa os seus drivers para comunicar com o iPhone.
   - **macOS:** `brew install --cask impactor`, ou transfere-o.
   - **Linux:**
     [Flathub](https://flathub.org/apps/dev.khcrysalis.PlumeImpactor).
     Precisa do `usbmuxd`, que a maioria das distribuições já inclui.
3. Liga o iPhone por USB, desbloqueia-o e toca em **Confiar** quando perguntar
   pelo computador.
4. Abre o Impactor, inicia sessão com o teu Apple ID, escolhe o `.ipa` do
   SmartZT e instala-o.
5. No iOS 16 ou posterior, ativa **Definições › Privacidade e segurança ›
   Modo de programador** (*Settings › Privacy & Security › Developer Mode*) e
   reinicia o telemóvel quando for pedido.
6. Se o iOS disser que o programador não é de confiança, abre **Definições ›
   Geral › VPN e gestão de dispositivos** (*Settings › General › VPN & Device
   Management*), toca no teu Apple ID e em **Confiar**.

**Com um Apple ID gratuito:**

- A Apple faz com que a app deixe de abrir ao fim de **7 dias**. Volta a
  instalá-la com o Impactor (o Impactor também a pode renovar por ti); a
  garagem, as definições e o registo de abastecimentos mantêm-se.
- Podes ter no máximo 3 apps instaladas por sideloading ao mesmo tempo, e só
  se podem registar 10 identificadores de app por semana. O SmartZT usa 2: a
  app e a sua extensão de transmissão do ecrã.

**Se o Impactor mostrar** `An Application Group with Identifier
'group.com.vitapps.smartzt.…' is not available`, volta a instalá-la: pode
acontecer na primeira instalação, e na segunda tentativa o grupo já está
criado.

O AltStore, o SideStore e o Sideloadly também devem funcionar, mas até agora
só o Impactor foi testado.

**Para atualizar**, transfere o novo `.ipa` e instala-o por cima do atual da
mesma forma.

### Duplicação de ecrã no iOS

1. Liga-te ao Wi-Fi da mota na app Definições do iOS (o SmartZT mostra-te o
   nome e a palavra-passe da rede) e volta ao SmartZT.
2. No separador **Ecrã**, inicia a duplicação.
3. No painel de transmissão do ecrã do iOS, escolhe **SmartZT** e toca no
   botão para iniciar a transmissão.
4. Mantém o telemóvel desbloqueado. Enquanto está bloqueado, o painel mostra
   uma imagem de "telemóvel bloqueado". **Keep running when locked** (a opção
   ainda está em inglês na app) reproduz um áudio inaudível para que o iOS
   mantenha a duplicação ativa; gasta mais bateria.

## Antes de começar

O controlo por BLE (trancar/destrancar, assento, tampa do depósito, luz
ambiente) precisa de uma chave de cifra Zontes de 16 caracteres para se
autenticar no módulo PKE. Esta chave **não é distribuída com a app**: sem ela,
o controlo por BLE não funciona.

## Estado

É um cliente feito por engenharia inversa: as tramas BLE, a cifra e a API
HTTP do DVR foram obtidas a partir da app original, não de documentação
oficial. Podem existir problemas com combinações de mota e firmware menos
comuns.

## Instalação

Este repositório não aloja o código-fonte, apenas versões assinadas.

- **Android:** transfere o APK mais recente da página de
  [Releases](https://github.com/drkbcn/SmartZT/releases) e instala-o por cima
  da versão atual; a garagem, as definições e o registo de abastecimentos
  mantêm-se. As versões marcadas como *Pre-release* são betas, e a verificação
  de atualizações da app não as propõe.
- **iPhone e iPad:** consulta
  [Instalação em iPhone ou iPad](#instalação-em-iphone-ou-ipad-sideloading).

## Idiomas

Inglês, espanhol, italiano, português, francês, alemão, grego, búlgaro e
ucraniano. (O grego, o ucraniano e o búlgaro usam o tipo de letra do sistema.)

## Aviso

Este projeto não é afiliado, apoiado nem suportado pela Zontes. Usa-o por tua
conta e risco.
