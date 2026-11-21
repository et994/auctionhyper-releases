# AuctionHyper

*English below.*

AuctionHyper è un addon per la casa d'aste di **World of Warcraft: Forever** più un'app per
Windows che legge i dati salvati dall'addon e mostra prezzi, affari, vendite e upgrade. È un
progetto personale, ancora giovane: se qualcosa non va, scrivimi (sotto c'è cosa mandare).

## 1. Prima di installare: Smart App Control

L'installatore e l'app non sono firmati digitalmente, quindi Windows può bloccarli.

1. Apri **Sicurezza di Windows > Controllo delle app e del browser > Impostazioni di Controllo
   intelligente delle app** (i nomi possono variare leggermente con la versione di Windows).
2. Se è **Attivato**, l'installatore viene bloccato senza possibilità di aprirlo comunque. Per
   installare va messo su **Disattivato**. Attenzione: su molte versioni di Windows, una volta
   spento non si riaccende senza reinstallare Windows. Decidi tu; se preferisci non spegnerlo,
   non installare.
3. Se è **Valutazione** puoi installare, ma Windows può decidere da solo, più avanti, di passarlo
   ad **Attivato**: da quel momento blocca l'app e anche gli installatori delle versioni nuove.
   L'unico rimedio è metterlo su **Disattivato** (con l'avvertenza del punto 2).
4. Se è **Disattivato** puoi proseguire.

## 2. Installazione

1. Scarica `AuctionHyper_<versione>_x64-setup.exe` dall'[ultima release](https://github.com/et994/auctionhyper-releases/releases/latest)
   (sezione **Assets**) e avvialo. Serve solo la prima volta: poi l'app si aggiorna da sola
   (sezione 6).
2. Se compare **"Windows ha protetto il PC"** (SmartScreen), fai clic su **Ulteriori
   informazioni** e poi su **Esegui comunque**.
3. Segui l'installazione e apri AuctionHyper.

## 3. Configurazione guidata (primo avvio)

1. **Cartella di World of Warcraft**: l'app propone le cartelle che trova (di solito
   `C:\Program Files (x86)\World of Warcraft`). Scegli quella giusta o scrivi il percorso: deve
   contenere la cartella `_forever_`. L'app dice subito se va bene e, se no, perché.
2. **Addon in gioco**: fai clic su **Installa addon**. L'app copia l'addon in
   `_forever_\Interface\AddOns\AuctionHyper`. Non tocca nessun altro file del gioco: scrive solo
   nelle cartelle `AuctionHyper` e `AuctionHyperData` dentro `Interface\AddOns`.
3. **Pronto**: scegli se tenere l'app nell'area di notifica quando chiudi la finestra (spuntato
   di base) e se avviarla con Windows (non spuntato), poi fai clic su **Inizia**. Le due opzioni
   sono spiegate nella sezione 5.

Se non hai mai avviato WoW: Forever, la cartella `Interface\AddOns` non esiste ancora e l'addon
non si può installare: avvia il gioco una volta fino alla scelta del personaggio, chiudilo, poi
in AuctionHyper fai **Impostazioni > Installa addon**.

Se non vuoi configurare subito, fai clic su **Configura più tardi**: l'app si apre lo stesso e
puoi riprendere quando vuoi da **Impostazioni > Rifai la configurazione guidata**.

All'avvio, se l'addon nel gioco è più vecchio di quello incluso nell'app (una versione nuova
dell'app porta un addon più recente), l'app lo aggiorna da sola e ti dice cosa fare in gioco:
`/reload` se sono cambiati solo i file esistenti, oppure chiudere **del tutto** il gioco e
riaprirlo se la versione nuova ha file nuovi (lì un `/reload` non basta). Se l'aggiornamento non riesce
(per esempio un file occupato) compare l'errore con il pulsante **Aggiorna addon** per riprovare.
Se l'addon non è installato l'app non lo installa da sola: te lo segnala e lo installi da
**Impostazioni > Installa addon**. Se l'hai tolto tu con **Rimuovi addon**, l'app non lo
reinstalla e non lo aggiorna finché non lo reinstalli tu.

## 4. Prima scansione

1. Apri l'app e avvia World of Warcraft (se era già aperto mentre installavi l'addon, chiudilo
   **del tutto** e riaprilo: un `/reload` non basta per un addon nuovo). Nella schermata dei
   personaggi, in **AddOns**, AuctionHyper deve essere attivo.
2. Apri la casa d'aste da un banditore: la scansione parte da sola (oppure scrivi `/ahh scan`).
   Tieni aperta la casa d'aste finché arriva la lista: può volerci qualche minuto.
3. Aspetta la scritta verde **"Tutto pronto"** nella barra di AuctionHyper sotto la finestra
   della casa d'aste (in chat il messaggio è **"Dati completi: … Puoi fare /reload"**), poi
   scrivi `/reload`: solo così il gioco salva i dati su disco.
4. **Dopo il primo `/reload` chiudi e riapri il gioco una volta.** Importando i dati, l'app crea
   un secondo addon, `AuctionHyperData`, con le stime che vedi in gioco (affari, prezzi
   consigliati, upgrade), e il gioco trova le cartelle nuove degli addon solo all'avvio. Nella
   schermata dei personaggi, in **AddOns**, deve essere attivo anche AuctionHyperData.
5. Tieni aperta l'app mentre giochi: importa da sola i dati a ogni `/reload` o uscita dal gioco.

`/ahh` apre la finestra dell'addon in gioco (impostazioni e azioni).

## 5. L'app in background: area di notifica e avvio con Windows

L'app importa i dati e scrive le stime per l'addon solo mentre è aperta, quindi conviene che
resti aperta mentre giochi. Due opzioni aiutano; le scegli nell'ultimo passo della configurazione
guidata e le cambi quando vuoi in **Impostazioni > Avvio e chiusura**:

- **Resta nell'area di notifica quando chiudi la finestra**: chiudendo la finestra con la X l'app
  non si chiude, ma resta come icona nell'area di notifica, vicino all'orologio (se non la vedi,
  è sotto la freccia **^** delle icone nascoste) e continua a importare. Fai clic sull'icona per
  riaprire la finestra. **Per chiudere davvero l'app**: clic destro sull'icona > **Esci**. Con
  l'opzione spenta, chiudere la finestra chiude l'app come prima.
- **Avvia con Windows**: all'accesso a Windows l'app parte da sola, nascosta nell'area di
  notifica, così è già pronta quando entri in gioco. Si toglie da **Impostazioni > Avvio e
  chiusura** oppure da Impostazioni di Windows > **App > Avvio** (voce AuctionHyper). Gli
  aggiornamenti automatici (sezione 6) lasciano la voce com'è. Se invece installi a mano una
  versione nuova, il programma di installazione toglie la voce di avvio, ma l'app la rimette da
  sola la prima volta che la apri dopo l'installazione (alla fine lascia spuntata la casella che
  avvia AuctionHyper). Disinstallando l'app la voce di avvio viene tolta; se poi la reinstalli
  tenendo la cartella dati, l'opzione torna come l'avevi lasciata.

Se apri AuctionHyper mentre è già nell'area di notifica, si riapre la finestra esistente (non
parte una seconda copia).

## 6. Aggiornamenti

Dalla versione 0.11 l'app si aggiorna da sola, ma solo quando lo decidi tu:

- poco dopo l'avvio e poi ogni 6 ore controlla su GitHub se c'è una versione nuova. Se c'è,
  compare in alto la barra **"AuctionHyper X è disponibile"** con le novità (se l'app è
  nell'area di notifica lo dice il suggerimento dell'icona);
- **Aggiorna ora** scarica la versione nuova (vedi l'avanzamento), poi l'app si chiude, il
  programma di installazione mostra solo una barra di avanzamento e l'app si riapre aggiornata.
  Dati, impostazioni e avvio con Windows restano. **Più tardi** nasconde la barra fino al
  prossimo avvio dell'app;
- l'installatore è firmato con la mia chiave: se il file scaricato non corrisponde alla firma,
  l'app non lo installa;
- dopo l'aggiornamento dell'app, l'addon nel gioco si aggiorna da solo (sezione 3).

In **Impostazioni > Aggiornamenti** trovi la versione installata, l'ultimo controllo con il suo
esito, il pulsante **Controlla ora** e l'interruttore **Controlla automaticamente gli
aggiornamenti** (acceso di base). Spento, l'app non contatta GitHub da sola: controlli tu quando
vuoi con **Controlla ora**.

Cosa viene contattato: solo GitHub (`github.com` e il suo server dei download), per leggere il
file `latest.json` delle release di AuctionHyper e, se scegli di aggiornare, scaricare
l'installatore. GitHub vede il tuo indirizzo IP e quale versione scarichi, come per qualsiasi
download; l'app non manda nient'altro (nessun dato del gioco, dei personaggi o del PC).

## 7. Se qualcosa non va

Mandami:

- **Gli errori del gioco**: una volta sola, scrivi in chat `/console scriptErrors 1`, così il
  gioco mostra gli errori Lua in una finestra. Quando ne compare uno mandami uno screenshot della
  finestra (o copiane il testo) e il file `World of Warcraft\_forever_\Logs\Client.log`.
- **I file di log dell'app**: in **Impostazioni > Apri cartella dati e log** si apre la cartella
  dati (`%APPDATA%\dev.auctionhyper.desktop`). Mandami `logs\auctionhyper.log` e
  `logs\crash.log` (se c'è).
- Cosa stavi facendo e, se puoi, uno screenshot dell'errore.

Non mandarmi la cartella dati intera senza chiedermelo: contiene il database dei tuoi personaggi.

## 8. Disinstallazione

- **App**: se è nell'area di notifica chiudila prima (clic destro sull'icona > **Esci**), poi
  Impostazioni di Windows > **App > App installate** > AuctionHyper > **Disinstalla**. La
  disinstallazione toglie anche l'avvio con Windows. Se il programma di disinstallazione non lo
  propone, la cartella dati `%APPDATA%\dev.auctionhyper.desktop` resta: cancellala a mano se vuoi
  togliere anche i dati.
- **Addon**: prima di disinstallare l'app, **Impostazioni > Rimuovi addon** (toglie
  `AuctionHyper` e `AuctionHyperData`); oppure, a gioco
  chiuso, cancella a mano `_forever_\Interface\AddOns\AuctionHyper` e
  `_forever_\Interface\AddOns\AuctionHyperData`. I dati salvati dall'addon stanno in
  `_forever_\WTF\Account\<account>\SavedVariables\AuctionHyper.lua` (anche questo si può
  cancellare).

## 9. Privacy

- Nessun dato del gioco lascia il tuo PC. L'app legge (senza modificarli) i file del gioco e, per
  trovare dove è installato, il registro di Windows e i file di Battle.net; scrive solo nella sua
  cartella dati e nelle cartelle `AuctionHyper*` in `Interface\AddOns` (più, se attivi l'avvio con
  Windows, la voce di avvio automatico nel registro del tuo utente).
- L'unica richiesta in rete è il controllo degli aggiornamenti su GitHub (sezione 6: GitHub vede
  indirizzo IP e versione scaricata), che puoi spegnere. Non usa le API web di Blizzard e non ti
  chiede credenziali Battle.net.
- Non scarica immagini o dati da siti esterni: le icone le legge dai file del gioco installato.

---

# AuctionHyper (English)

AuctionHyper is an auction house addon for **World of Warcraft: Forever** plus a Windows app that
reads the data saved by the addon and shows prices, deals, sales and upgrades. The app's interface
is in Italian. It is a young personal project: if something breaks, tell me (what to send is below).

## 1. Before installing: Smart App Control

The installer and the app are not digitally signed, so Windows may block them.

1. Open **Windows Security > App & browser control > Smart App Control settings** (names may
   vary slightly with your Windows version).
2. If it is **On**, the installer is blocked and cannot be run anyway. To install, it has to be
   set to **Off**. Warning: on many Windows versions, once turned off it cannot be turned back on
   without reinstalling Windows. Your call; if you would rather keep it on, do not install.
3. If it is **Evaluation**, you can install, but Windows may later switch it to **On** by itself:
   from then on it blocks the app and the installers of new versions too. The only fix is setting
   it to **Off** (with the warning in point 2).
4. If it is **Off**, go ahead.

## 2. Install

1. Download `AuctionHyper_<version>_x64-setup.exe` from the [latest release](https://github.com/et994/auctionhyper-releases/releases/latest)
   (**Assets** section) and run it. Only the first time: after that the app updates itself
   (section 6).
2. If **"Windows protected your PC"** (SmartScreen) appears, click **More info**, then **Run
   anyway**.
3. Complete the setup and open AuctionHyper.

## 3. Setup wizard (first run)

1. **Cartella di World of Warcraft** (WoW folder): the app lists the folders it finds (usually
   `C:\Program Files (x86)\World of Warcraft`). Pick the right one or type the path: it must
   contain the `_forever_` folder. The app tells you right away whether it is valid and, if not,
   why.
2. **Addon in gioco** (in-game addon): click **Installa addon**. The app copies the addon into
   `_forever_\Interface\AddOns\AuctionHyper`. It never touches any other game file: it only
   writes the `AuctionHyper` and `AuctionHyperData` folders inside `Interface\AddOns`.
3. **Pronto** (ready): choose whether to keep the app in the notification area when you close the
   window (checked by default) and whether to start it with Windows (unchecked), then click
   **Inizia**. Both options are explained in section 5.

If you have never started WoW: Forever, the `Interface\AddOns` folder does not exist yet and the
addon cannot be installed: start the game once, up to character select, close it, then in
AuctionHyper use **Impostazioni > Installa addon** (Settings > Install addon).

If you do not want to set it up right away, click **Configura più tardi** (set up later): the app
opens anyway and you can come back to it any time from **Impostazioni > Rifai la configurazione
guidata** (Settings > run the setup wizard again).

At startup, if the in-game addon is older than the one bundled with the app (a new app version
brings a newer addon), the app updates it by itself and tells you what to do in game: `/reload`
if only existing files changed, or close the game **completely** and start it again if the new
version has new files (then `/reload` is not enough). If the update fails (for example a
file in use), an error appears with the **Aggiorna addon** button to try again. If the addon is
not installed, the app does not install it by itself: it tells you, and you install it from
**Impostazioni > Installa addon**. If you removed it yourself with **Rimuovi addon**, the app
neither reinstalls nor updates it until you install it again.

## 4. First scan

1. Open the app and start World of Warcraft (if the game was already running while you installed
   the addon, close it **completely** and start it again: `/reload` is not enough for a new
   addon). On the character screen, under **AddOns**, AuctionHyper must be enabled.
2. Open the auction house at an auctioneer: the scan starts by itself (or type `/ahh scan`). Keep
   the auction house open until the list arrives: it can take a few minutes.
3. Wait for the green **"Tutto pronto"** text in the AuctionHyper bar below the auction house
   window (in chat the message is **"Dati completi: … Puoi fare /reload"**), then type `/reload`:
   only then does the game save the data to disk.
4. **After the first `/reload`, close the game and start it again once.** While importing the
   data the app creates a second addon, `AuctionHyperData`, with the estimates you see in game
   (deals, suggested prices, upgrades), and the game only discovers new addon folders at startup.
   On the character screen, under **AddOns**, AuctionHyperData must be enabled too.
5. Keep the app open while you play: it imports the data by itself at every `/reload` or logout.

`/ahh` opens the addon's window in game (settings and actions).

## 5. The app in the background: notification area and start with Windows

The app imports the data and writes the estimates for the addon only while it is running, so it
should stay open while you play. Two options help; you pick them in the last step of the setup
wizard and can change them any time in **Impostazioni > Avvio e chiusura** (Settings > startup
and closing):

- **Resta nell'area di notifica quando chiudi la finestra** (stay in the notification area when
  you close the window): closing the window with the X does not quit the app, it stays as an icon
  in the notification area near the clock (if you cannot see it, it is under the **^** arrow of
  hidden icons) and keeps importing. Click the icon to bring the window back. **To really quit
  the app**: right-click the icon > **Esci** (quit). With the option off, closing the window quits
  the app as before.
- **Avvia con Windows** (start with Windows): when you sign in to Windows the app starts by
  itself, hidden in the notification area, so it is ready when you start playing. Turn it off in
  **Impostazioni > Avvio e chiusura** or in Windows Settings > **Apps > Startup** (AuctionHyper
  entry). Automatic updates (section 6) leave the entry as it is. If you install a new version by
  hand instead, the setup program removes the startup entry, but the app puts it back by itself
  the first time you open it after the install (at the end, leave the box that launches
  AuctionHyper ticked). Uninstalling the app removes the startup entry; if you then reinstall it
  and keep the data folder, the option comes back as you left it.

If you open AuctionHyper while it is already in the notification area, the existing window comes
back (a second copy does not start).

## 6. Updates

Since version 0.11 the app updates itself, but only when you say so:

- shortly after startup and then every 6 hours it checks GitHub for a new version. If there is
  one, the **"AuctionHyper X è disponibile"** bar appears at the top with what is new (if the app
  is in the notification area, the icon's tooltip says so);
- **Aggiorna ora** (update now) downloads the new version (you see the progress), then the app
  closes, the setup program shows only a progress bar and the app opens again, updated. Data,
  settings and start with Windows are kept. **Più tardi** (later) hides the bar until the app
  starts again;
- the installer is signed with my key: if the downloaded file does not match the signature, the
  app does not install it;
- after the app update, the in-game addon updates itself (section 3).

**Impostazioni > Aggiornamenti** (Settings > updates) shows the installed version, the last
check and its result, the **Controlla ora** (check now) button and the **Controlla
automaticamente gli aggiornamenti** switch (check for updates automatically, on by default). When
it is off the app never contacts GitHub by itself: you check whenever you like with **Controlla
ora**.

What is contacted: only GitHub (`github.com` and its download server), to read the `latest.json`
file of AuctionHyper's releases and, if you choose to update, download the installer. GitHub sees
your IP address and which version you download, as with any download; the app sends nothing else
(no game, character or PC data).

## 7. If something breaks

Send me:

- **The game's errors**: once, type `/console scriptErrors 1` in chat, so the game shows Lua
  errors in a window. When one appears, send me a screenshot of that window (or copy its text) and
  the file `World of Warcraft\_forever_\Logs\Client.log`.
- **The app's logs**: **Impostazioni > Apri cartella dati e log** opens the data folder
  (`%APPDATA%\dev.auctionhyper.desktop`). Send me `logs\auctionhyper.log` and `logs\crash.log`
  (if present).
- What you were doing and, if you can, a screenshot of the error.

Please do not send the whole data folder unless I ask: it holds the database of your characters.

## 8. Uninstall

- **App**: if it is in the notification area, quit it first (right-click the icon > **Esci**),
  then Windows Settings > **Apps > Installed apps** > AuctionHyper > **Uninstall**. Uninstalling
  also removes the start with Windows entry. If the uninstaller does not offer it, the data folder
  `%APPDATA%\dev.auctionhyper.desktop` stays: delete it by hand to remove the data too.
- **Addon**: before uninstalling the app, **Impostazioni > Rimuovi addon** (removes
  `AuctionHyper` and `AuctionHyperData`); or, with the game
  closed, delete `_forever_\Interface\AddOns\AuctionHyper` and
  `_forever_\Interface\AddOns\AuctionHyperData` by hand. The addon's saved data is in
  `_forever_\WTF\Account\<account>\SavedVariables\AuctionHyper.lua` (you can delete it too).

## 9. Privacy

- No game data leaves your PC. The app reads (without changing them) the game's files and, to
  find where the game is installed, the Windows registry and Battle.net's files; it only writes to
  its own data folder and to the `AuctionHyper*` folders in `Interface\AddOns` (plus, if you turn
  on start with Windows, the startup entry in your user's registry).
- Its only network request is the update check on GitHub (section 6: GitHub sees your IP address
  and the version downloaded), which you can turn off. It does not use Blizzard's web API and
  never asks for Battle.net credentials.
- It does not download images or data from websites: icons are read from the installed game files.
