# NPM Project - istruzioni di set-up

## Installazione di Node e Npm

Devo prima di tutto installare Node e Npm sul mio sistema. È sufficiente installarli una volta per tutte, non serve che siano installati su ogni progetto.

Procedura:

1. Installo Node e Npm, versione stabile (LTS), scaricandolo da qua https://nodejs.org/en/

2. Controllo se è installato aprendo un terminale `bash` e i comandi `npm -v` e `node -v`
    * Per aprire un terminale in Visual Studio Code: `Terminale > Nuovo Terminale` nel menu in alto - **controllare che il terminale sia `bash`**
3. Se i comandi stampano la versione installata, il set-up è andato a buon fine - **controllare di avere Node versione 16 e Npm versione 8**

Esempio di output del terminale con installazione corretta di Node e Npm:

```bash
$ node -v
v16.16.0

$ npm -v
8.11.0
```

## Set-up di un nuovo progetto

1. Creo un nuovo progetto come siamo stati abituati a farlo fino ad ora: nuova cartella, set-up di `git` con GitHub Desktop, ecc

2. Apro con Visual Studio Code la cartella di progett

3. Apro un nuovo terminale `bash`

4. Lancio `npm init` per creare il file `package.json`
    * Se mi vanno bene le impostazioni di default che mi mostra tra parentesi, premo Invio finché non ha creato il file

5. Uso `npm install` per installare un pacchetto, e lo dovrei vedere apparire nel file `package.json` sotto le `dependencies` (vedi file `package.json` in questo progetto)
    * ad esempio, `npm install bootstrap` per installare l'ultima versione di Bootstrap. I pacchetti verranno installati all'interno della cartella `node_modules`
    * In caso di Bootstrap, posso poi andare a linkarli nel file HTML come in questo esempio, vedi `index.html`

6. Creo un file `.gitignore` nella cartella di progetto e aggiungo la riga `node_modules` all'interno di questo file, così da non fare commit su GitHub della cartella `node_modules` ma solo dei file di codice che andiamo a scrivere noi

## Set-up di SASS

1. Installo SASS sul mio sistema, globalmente, lanciando `npm install -g sass` - questo non lo va ad installare nel mio progetto o ad aggiungere nel mio `package.json`, ma lo rende disponibile come un comando del mio terminale, ovunque io mi trovi nel sistema

2. Lancio `sass -v` nel terminale per testare che sia installato correttamente

3. Creo cartelle CSS e SASS sotto assets come in questo progetto, aggiungo lo script per compilare SASS al `package.json` (vedi file di esempio in questo progetto)

4. Eseguo lo script con `npm run` - in questo caso, eseguo `npm run sass:watch`

5. Aggiungo un Link al file `assets/css/styles.css` nell'HTML

6. Se il set-up è andato a buon fine, scrivendo SASS nel mio `assets/scss/styles.scss` dovrei vedere la compilazione da SASS a CSS funzionare correttamente, e dovrei vedere lo stile applicato al mio HTML
