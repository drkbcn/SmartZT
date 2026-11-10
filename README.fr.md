🌐 [English](README.md) · [Español](README.es.md) · [Italiano](README.it.md) · [Português](README.pt.md) · **Français** · [Deutsch](README.de.md) · [Ελληνικά](README.el.md) · [Български](README.bg.md) · [Українська](README.uk.md)

# 🏍️ SmartZT, application non officielle pour motos Zontes

[![Dernière version](https://img.shields.io/github/v/release/drkbcn/SmartZT)](https://github.com/drkbcn/SmartZT/releases/latest)
[![Téléchargements](https://img.shields.io/github/downloads/drkbcn/SmartZT/total)](https://github.com/drkbcn/SmartZT/releases)

Une application non officielle pour les motos Zontes, conçue pour remplacer
celle du constructeur par quelque chose de plus rapide et plus fiable. Elle
communique avec la caméra embarquée (DVR) de la moto en Wi-Fi et avec son
module keyless PKE en Bluetooth Low Energy. Elle fonctionne sur Android et,
depuis la 2.1, sur iPhone et iPad avec une première **version iOS en test**
(voir [iOS (en test)](#ios-en-test)).

| Moto | Caméra | Carburant | Écran | Réglages | À propos |
|:-:|:-:|:-:|:-:|:-:|:-:|
| <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/dark-moto.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/dark-camera.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/dark-fuel.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/dark-screen.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/dark-settings.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/dark-about.png" width="130"> |
| <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/light-moto.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/light-camera.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/light-fuel.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/light-screen.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/light-settings.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/light-about.png" width="130"> |

Le thème clair, sombre ou système se choisit dans **Réglages › Thème**.

## Ce qu'elle fait

- **Moto** : d'abord votre moto et son état de connexion, avec un seul bouton
  **Se connecter à la moto**. Les commandes de verrouillage, déverrouillage,
  bouchon du réservoir et selle affichent leur progression pendant l'envoi, et
  l'éclairage d'ambiance se pilote via le module PKE, avec le même schéma de
  défi-réponse AES que l'application d'origine.
- **Caméra** : liste et télécharge les vidéos et photos des caméras avant et
  arrière du DVR, et les lit dans l'application.
- **Carburant** : un journal des pleins avec des statistiques de consommation
  et des graphiques dans le temps.
- **Écran** : l'état du tableau de bord (TFT) et deux façons de l'utiliser :
  - **Duplication d'écran** : diffuse l'écran du téléphone sur le tableau de
    bord de la moto en Wi-Fi Direct, avec fréquence d'images et débit
    réglables.
  - **Android Auto** *(expérimental)* : affiche Android Auto sur le tableau de
    bord, pour des applications de cartes et de musique comme Waze ou Spotify.
    Détails plus bas.
- **Réglages du véhicule** : lit et modifie les paramètres enregistrés dans le
  MCU de la moto (mode de clé, délai de verrouillage automatique, alarme ESS,
  alarme de frein à main, etc.).
- **Garage** : gérez plusieurs motos et passez de l'une à l'autre.
- **Configuration par QR** : l'appairage et les identifiants Wi-Fi se
  configurent en scannant un code QR, comme pour la configuration de la moto ou
  chez le concessionnaire.
- **Export/import de la configuration** : sauvegarde et restauration de la
  configuration de l'application via un code QR chiffré.
- **Mises à jour** : l'application consulte cette page pour trouver les
  nouvelles versions (au plus une fois par jour) et vous permet de télécharger,
  reporter ou ignorer une version. **Réglages › À propos** affiche aussi les
  notes de chaque version. Les versions Android n'expirent jamais.

## Android Auto (expérimental)

Le téléphone joue le rôle de l'autoradio de la voiture : l'image d'Android Auto
est réencodée pour le tableau de bord et les appuis sur le tableau de bord lui
sont renvoyés. Le son des instructions de navigation et la musique continuent
de passer par le téléphone (par exemple vers un intercom Bluetooth dans le
casque).

- Android Auto doit être installé, et son *head unit server* développeur doit
  être lancé à la main : ouvrez les paramètres d'Android Auto, appuyez une
  dizaine de fois sur **Version**, puis utilisez le menu ⋮ › **Start head unit
  server**. L'application propose un raccourci vers ces paramètres. Android ne
  permet pas à une autre application de le lancer à votre place.
- L'écran d'Android Auto s'ouvre aussi sur le téléphone, où vous pouvez le
  toucher pour ouvrir des applications et des menus. Un bouton ✕ vous ramène à
  SmartZT sans arrêter la projection.
- **Essayer Android Auto sur ce téléphone** le lance sans aucune moto
  connectée.
- La taille de l'image (800×480, 1280×720 ou 1920×1080) se choisit dans
  l'onglet Écran. Les grandes tailles consomment plus de CPU et de batterie.
- Les boutons du guidon ne sont pas pris en charge : ces motos ne les envoient
  pas.

Il n'a pas été validé sur tous les téléphones ni sur toutes les versions
d'Android Auto, attendez-vous donc à quelques imperfections.

## iOS (en test)

SmartZT 2.1 est la première version pour iPhone et iPad. Elle est **en
test** : attendez-vous à des imperfections, et merci de signaler ce qui ne
fonctionne pas.

- **La duplication d'écran sur iOS en est à un stade très précoce.** Sur
  certains téléphones et tableaux de bord, elle peut ne pas démarrer ou ne pas
  afficher d'image. En cas d'échec, partagez le journal de duplication (bouton
  de partage sur la carte du tableau de bord, dans l'onglet Écran) et
  joignez-le à un [ticket](https://github.com/drkbcn/SmartZT/issues).
- **Fonctionne sur iOS :** Moto (verrouillage, déverrouillage, selle, bouchon
  du réservoir, éclairage d'ambiance, tension de la batterie), Caméra (vidéos
  et photos du DVR), Carburant, Garage, Réglages du véhicule, configuration
  par QR et export/import de la configuration.
- **Non disponible sur iOS :** Android Auto, le HUD de navigation, la couche
  de protection d'écran et les widgets de l'écran d'accueil. Le Wi-Fi Direct
  n'existe pas sur iOS : vous rejoignez donc le Wi-Fi du DVR à la main dans
  l'app Réglages d'iOS ; SmartZT vous indique son nom et son mot de passe.
- **Prérequis :** iOS 15 ou ultérieur (la duplication d'écran nécessite
  iOS 16 ou ultérieur), un identifiant Apple (un compte gratuit suffit) et un
  ordinateur sous Windows, macOS ou Linux pour installer l'application.

### Installation sur iPhone ou iPad (sideloading)

SmartZT n'est pas sur l'App Store. Le fichier `.ipa` de la page
[Releases](https://github.com/drkbcn/SmartZT/releases) s'installe avec votre
propre identifiant Apple grâce à
**[Impactor](https://github.com/claration/Impactor)**, un outil de
sideloading gratuit et open source :

1. Téléchargez `SmartZT-<version>.ipa` depuis la dernière version.
2. Installez Impactor depuis sa
   [page de releases](https://github.com/claration/Impactor/releases) :
   - **Windows :** installez d'abord [iTunes](https://support.apple.com/en-us/106372) ;
     Impactor utilise ses pilotes pour communiquer avec l'iPhone.
   - **macOS :** `brew install --cask impactor`, ou téléchargez-le.
   - **Linux :**
     [Flathub](https://flathub.org/apps/dev.khcrysalis.PlumeImpactor). Il a
     besoin de `usbmuxd`, déjà inclus dans la plupart des distributions.
3. Branchez l'iPhone en USB, déverrouillez-le et acceptez de faire confiance à
   l'ordinateur quand il le demande.
4. Ouvrez Impactor, connectez-vous avec votre identifiant Apple, choisissez le
   fichier `.ipa` de SmartZT et installez-le.
5. Sur iOS 16 ou ultérieur, activez **Réglages › Confidentialité et sécurité ›
   Mode développeur** (*Settings › Privacy & Security › Developer Mode*) et
   redémarrez le téléphone quand il le demande.
6. Si iOS indique que le développeur n'est pas approuvé, ouvrez **Réglages ›
   Général › VPN et gestion de l'appareil** (*Settings › General › VPN &
   Device Management*), touchez votre identifiant Apple et faites-lui
   confiance.

**Avec un identifiant Apple gratuit :**

- Apple fait cesser l'ouverture de l'application au bout de **7 jours**.
  Réinstallez-la avec Impactor (Impactor peut aussi la renouveler pour vous) ;
  votre garage, vos réglages et votre journal des pleins sont conservés.
- Vous pouvez avoir au plus 3 applications installées en sideloading en même
  temps, et enregistrer seulement 10 identifiants d'app par semaine. SmartZT en
  utilise 2 : l'application et son extension de diffusion de l'écran.

**Si Impactor affiche** `An Application Group with Identifier
'group.com.vitapps.smartzt.…' is not available`, réinstallez-la : cela peut
arriver lors de la première installation, et à la deuxième tentative le groupe
est déjà créé.

AltStore, SideStore et Sideloadly devraient aussi fonctionner, mais seul
Impactor a été essayé pour l'instant.

**Pour mettre à jour**, téléchargez le nouveau `.ipa` et installez-le
par-dessus l'actuel de la même façon.

### Duplication d'écran sur iOS

1. Rejoignez le Wi-Fi de la moto dans l'app Réglages d'iOS (SmartZT vous
   indique son nom et son mot de passe), puis revenez dans SmartZT.
2. Dans l'onglet **Écran**, lancez la duplication.
3. Dans la feuille de diffusion d'écran d'iOS, choisissez **SmartZT** et
   touchez le bouton pour démarrer la diffusion.
4. Gardez le téléphone déverrouillé. Tant qu'il est verrouillé, le tableau de
   bord affiche une image « téléphone verrouillé ». **Keep running when
   locked** (l'option est encore en anglais dans l'application) joue un son
   inaudible pour qu'iOS garde la duplication active ; cela consomme plus de
   batterie.

## Avant de commencer

Le contrôle BLE (verrouillage/déverrouillage, selle, bouchon du réservoir,
éclairage d'ambiance) nécessite une clé de chiffrement Zontes de 16 caractères
pour s'authentifier auprès du module PKE. Cette clé **n'est pas fournie avec
l'application** : sans elle, le contrôle BLE ne fonctionne pas.

## État

C'est un client obtenu par rétro-ingénierie : les trames BLE, le chiffrement et
l'API HTTP du DVR ont été déduits de l'application d'origine, et non d'une
documentation officielle. Attendez-vous à quelques imperfections avec des
combinaisons de moto et de firmware moins courantes.

## Installation

Ce dépôt n'héberge pas le code source, seulement des versions signées.

- **Android :** téléchargez le dernier APK depuis la page
  [Releases](https://github.com/drkbcn/SmartZT/releases) et installez-le
  par-dessus votre version actuelle ; votre garage, vos réglages et votre
  journal des pleins sont conservés. Les versions marquées *Pre-release* sont
  des bêtas et la vérification des mises à jour de l'application ne les
  propose pas.
- **iPhone et iPad :** voir
  [Installation sur iPhone ou iPad](#installation-sur-iphone-ou-ipad-sideloading).

## Langues

Anglais, espagnol, italien, portugais, français, allemand, grec, bulgare et
ukrainien. (Le grec, l'ukrainien et le bulgare utilisent la police du
système.)

## Avertissement

Ce projet n'est ni affilié à Zontes, ni approuvé ni soutenu par Zontes.
Utilisez-le à vos propres risques.
