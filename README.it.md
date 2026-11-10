🌐 [English](README.md) · [Español](README.es.md) · **Italiano** · [Português](README.pt.md) · [Français](README.fr.md) · [Deutsch](README.de.md) · [Ελληνικά](README.el.md) · [Български](README.bg.md) · [Українська](README.uk.md)

# 🏍️ SmartZT, app non ufficiale per moto Zontes

[![Ultima versione](https://img.shields.io/github/v/release/drkbcn/SmartZT)](https://github.com/drkbcn/SmartZT/releases/latest)
[![Download](https://img.shields.io/github/downloads/drkbcn/SmartZT/total)](https://github.com/drkbcn/SmartZT/releases)

Un'app non ufficiale per le moto Zontes, nata per sostituire quella del
produttore con qualcosa di più veloce e affidabile. Comunica con la telecamera
(DVR) della moto via Wi-Fi e con il suo modulo keyless PKE via Bluetooth Low
Energy. Funziona su Android e, dalla 2.1, su iPhone e iPad con una prima
**versione iOS in prova** (vedi [iOS (in prova)](#ios-in-prova)).

| Moto | Camera | Carburante | Schermo | Impostazioni | Informazioni |
|:-:|:-:|:-:|:-:|:-:|:-:|
| <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/dark-moto.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/dark-camera.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/dark-fuel.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/dark-screen.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/dark-settings.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/dark-about.png" width="130"> |
| <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/light-moto.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/light-camera.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/light-fuel.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/light-screen.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/light-settings.png" width="130"> | <img src="https://raw.githubusercontent.com/drkbcn/SmartZT/main/screenshots/light-about.png" width="130"> |

Il tema chiaro, scuro o di sistema si sceglie in **Impostazioni › Tema**.

## Cosa fa

- **Moto**: prima la tua moto e il suo stato di connessione, con un solo
  pulsante **Connetti alla moto**. I comandi di blocco, sblocco, tappo del
  serbatoio e sella mostrano l'avanzamento mentre il comando viene inviato, e
  la luce ambiente si controlla tramite il modulo PKE, con lo stesso schema
  challenge-response AES dell'app originale.
- **Camera**: elenca e scarica video e foto delle telecamere anteriore e
  posteriore del DVR, e li riproduce nell'app.
- **Carburante**: un registro dei rifornimenti con statistiche sui consumi e
  grafici nel tempo.
- **Schermo**: lo stato del cruscotto (TFT) e due modi per usarlo:
  - **Duplicazione schermo**: trasmette lo schermo del telefono al cruscotto
    della moto via Wi-Fi Direct, con frame rate e bitrate regolabili.
  - **Android Auto** *(sperimentale)*: porta Android Auto sul cruscotto, per
    app di mappe e musica come Waze o Spotify. Dettagli più sotto.
- **Impostazioni veicolo**: legge e modifica i parametri salvati nella MCU
  della moto (metodo della chiave, tempo di blocco automatico, allarme ESS,
  allarme del freno di stazionamento, ecc.).
- **Garage**: gestisci più di una moto e passa dall'una all'altra.
- **Configurazione tramite QR**: l'abbinamento e le credenziali Wi-Fi si
  impostano scansionando un codice QR, come nella configurazione della moto o
  del concessionario.
- **Esporta/importa configurazione**: backup e ripristino della
  configurazione dell'app tramite un codice QR cifrato.
- **Aggiornamenti**: l'app controlla questa pagina per nuove versioni (al
  massimo una volta al giorno) e ti permette di scaricarle, rimandarle o
  saltarle. **Impostazioni › Informazioni** mostra anche le note di ogni
  versione. Le versioni Android non scadono mai.

## Android Auto (sperimentale)

Il telefono fa da unità principale dell'auto: l'immagine di Android Auto viene
ricodificata per il cruscotto e i tocchi sul cruscotto le vengono rimandati.
L'audio delle indicazioni di navigazione e la musica continuano a uscire dal
telefono (per esempio verso un interfono Bluetooth nel casco).

- Android Auto deve essere installato, e il suo *head unit server* per
  sviluppatori va avviato a mano: apri le impostazioni di Android Auto, tocca
  **Versione** una decina di volte, poi usa il menu ⋮ › **Start head unit
  server**. L'app ha una scorciatoia per quelle impostazioni. Android non
  permette a un'altra app di avviarlo al posto tuo.
- La schermata di Android Auto si apre anche sul telefono, dove puoi toccarla
  per aprire app e menu. Un pulsante ✕ ti riporta a SmartZT senza fermare la
  proiezione.
- **Prova Android Auto su questo telefono** lo avvia senza nessuna moto
  collegata.
- La dimensione dell'immagine (800×480, 1280×720 o 1920×1080) si sceglie nella
  scheda Schermo. Le dimensioni più grandi consumano più CPU e batteria.
- I pulsanti sul manubrio non sono supportati: queste moto non li inviano.

Non è stato provato su tutti i telefoni e su tutte le versioni di Android
Auto, quindi possono esserci problemi.

## iOS (in prova)

SmartZT 2.1 è la prima versione per iPhone e iPad. È **in prova**: possono
esserci problemi, e ti ringrazio se segnali cosa non funziona.

- **La duplicazione dello schermo su iOS è in una fase molto iniziale.** Su
  alcuni telefoni e cruscotti potrebbe non avviarsi o non mostrare
  l'immagine. Se non funziona, condividi il log della duplicazione (pulsante
  di condivisione nella scheda del cruscotto, in Schermo) e allegalo a una
  [segnalazione](https://github.com/drkbcn/SmartZT/issues).
- **Funziona su iOS:** Moto (blocco, sblocco, sella, tappo del serbatoio, luce
  ambiente, tensione della batteria), Camera (video e foto del DVR),
  Carburante, Garage, Impostazioni veicolo, configurazione tramite QR ed
  esportazione/importazione della configurazione.
- **Non disponibile su iOS:** Android Auto, l'HUD di navigazione, il livello
  di protezione dello schermo e i widget della schermata Home. Su iOS non
  esiste il Wi-Fi Direct, quindi ti colleghi a mano al Wi-Fi del DVR dall'app
  Impostazioni di iOS; SmartZT ti mostra nome e password della rete.
- **Requisiti:** iOS 15 o successivo (la duplicazione dello schermo richiede
  iOS 16 o successivo), un Apple ID (va bene anche gratuito) e un computer con
  Windows, macOS o Linux per installare l'app.

### Installazione su iPhone o iPad (sideloading)

SmartZT non è sull'App Store. Il file `.ipa` della pagina
[Releases](https://github.com/drkbcn/SmartZT/releases) si installa con il tuo
Apple ID usando **[Impactor](https://github.com/claration/Impactor)**, uno
strumento di sideloading gratuito e open source:

1. Scarica `SmartZT-<versione>.ipa` dall'ultima versione.
2. Installa Impactor dalla sua
   [pagina delle release](https://github.com/claration/Impactor/releases):
   - **Windows:** installa prima [iTunes](https://support.apple.com/en-us/106372);
     Impactor usa i suoi driver per comunicare con l'iPhone.
   - **macOS:** `brew install --cask impactor`, oppure scaricalo.
   - **Linux:**
     [Flathub](https://flathub.org/apps/dev.khcrysalis.PlumeImpactor). Serve
     `usbmuxd`, già incluso nella maggior parte delle distribuzioni.
3. Collega l'iPhone via USB, sbloccalo e tocca **Autorizza** quando chiede se
   fidarsi del computer.
4. Apri Impactor, accedi con il tuo Apple ID, scegli il file `.ipa` di
   SmartZT e installalo.
5. Su iOS 16 o successivo, attiva **Impostazioni › Privacy e sicurezza ›
   Modalità sviluppatore** (*Settings › Privacy & Security › Developer Mode*)
   e riavvia il telefono quando richiesto.
6. Se iOS dice che lo sviluppatore non è attendibile, apri **Impostazioni ›
   Generali › VPN e gestione dispositivi** (*Settings › General › VPN & Device
   Management*), tocca il tuo Apple ID e autorizzalo.

**Con un Apple ID gratuito:**

- Apple fa smettere di aprirsi l'app dopo **7 giorni**. Reinstallala con
  Impactor (Impactor può anche rinnovarla per te); garage, impostazioni e
  registro dei rifornimenti vengono mantenuti.
- Si possono avere al massimo 3 app installate in sideloading
  contemporaneamente, e registrare solo 10 identificativi di app a settimana.
  SmartZT ne usa 2: l'app e la sua estensione di trasmissione dello schermo.

**Se Impactor mostra** `An Application Group with Identifier
'group.com.vitapps.smartzt.…' is not available`, installala di nuovo: può
succedere alla prima installazione, e al secondo tentativo il gruppo è già
stato creato.

Anche AltStore, SideStore e Sideloadly dovrebbero funzionare, ma finora è
stato provato solo Impactor.

**Per aggiornare**, scarica il nuovo `.ipa` e installalo sopra quello attuale
allo stesso modo.

### Duplicazione dello schermo su iOS

1. Collegati al Wi-Fi della moto dall'app Impostazioni di iOS (SmartZT ti
   mostra nome e password della rete), poi torna su SmartZT.
2. Nella scheda **Schermo**, avvia la duplicazione.
3. Nel pannello di trasmissione dello schermo di iOS, scegli **SmartZT** e
   tocca il pulsante per avviare la trasmissione.
4. Tieni il telefono sbloccato. Quando è bloccato, il cruscotto mostra
   un'immagine di "telefono bloccato". **Keep running when locked** (l'opzione
   è ancora in inglese nell'app) riproduce un audio impercettibile perché iOS
   tenga attiva la duplicazione; consuma più batteria.

## Prima di iniziare

Il controllo BLE (blocco/sblocco, sella, tappo del serbatoio, luce ambiente)
richiede una chiave di cifratura Zontes di 16 caratteri per autenticarsi con
il modulo PKE. Questa chiave **non è distribuita con l'app**: senza, il
controllo BLE non funziona.

## Stato

È un client ottenuto con il reverse engineering: i frame BLE, la crittografia
e l'API HTTP del DVR sono stati ricavati dall'app originale, non da
documentazione ufficiale. Possono esserci problemi con combinazioni di moto e
firmware meno comuni.

## Installazione

Questo repository non ospita il codice sorgente, solo versioni firmate.

- **Android:** scarica l'ultimo APK dalla pagina
  [Releases](https://github.com/drkbcn/SmartZT/releases) e installalo sopra la
  versione attuale; garage, impostazioni e registro dei rifornimenti vengono
  mantenuti. Le versioni contrassegnate come *Pre-release* sono beta e il
  controllo aggiornamenti dell'app non le propone.
- **iPhone e iPad:** vedi
  [Installazione su iPhone o iPad](#installazione-su-iphone-o-ipad-sideloading).

## Lingue

Inglese, spagnolo, italiano, portoghese, francese, tedesco, greco, bulgaro e
ucraino. (Greco, ucraino e bulgaro usano il font di sistema.)

## Avvertenza

Questo progetto non è affiliato, approvato né supportato da Zontes. Usalo a
tuo rischio.
