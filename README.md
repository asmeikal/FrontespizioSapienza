# Frontespizio Sapienza

Package LaTeX per frontespizio tesi conforme alle indicazioni della Sapienza, vedi [qui](http://www.uniroma1.it/sites/default/files/allegati/esempio%20frontespizio%20elaborato.pdf) per un esempio e [qui](http://www.uniroma1.it/logotesi) per le indicazioni complete.
Il package &egrave; fornito *as-is*, senza alcuna garanzia di funzionamento.

Il logo (file `.eps`) &egrave; stato ottenuto convertendo (con Inkscape) il file `.ai` disponibile sul sito della Sapienza (vedi [qui](http://www.uniroma1.it/sites/default/files/allegati/ml_alta_risoluzione.zip)).

## Istruzioni

Il package modifica il comando `\maketitle` per creare una pagina di frontespizio conforme alle indicazioni Sapienza.
Per impostare i vari campi previsti nel frontespizio usare i seguenti comandi:
- `\FSSTitolo{[titolo]}` per impostare il titolo della tesi.
  Per inserire un a capo all'interno del titolo si pu&ograve; usare `\protect\newline`
  Il comando imposta anche il valore di `\title{}`;
- `\FSSFacolta{[facolta]}` per impostare la facolt&agrave;.
  Specificare solo la facolt&agrave;, es. "Filosofia, Lettere, Scienze Umanistiche e Studi Orientali", e non il testo *Facolt&agrave; di*;
- `\FSSCorso{[corso di studi]}` per impostare il corso di laurea.
  Specificare solo il corso di laurea, es. "Storia antica", e non il testo *Corso di laurea in*;
- `\FSSCattedra{[cattedra]}` (opzionale) per impostare la cattedra;
- `\FSSCandidato{[nome tesista]}` per impostare il nome del/la candidato/a.
  Il comando imposta anche il valore di `\author{}`;
- `\FSSMatricola{[matricola]}` per impostare il numero di matricola del/a candidato/a;
- `\FSSRelatore{[nome relatore]}` per impostare il nome del relatore o del supervisore;
- `\FSSCorrelatore{[nome correlatore]}` (opzionale) per impostare il nome del correlatore;
- `\FSSAnnoAccademico{[anno]/[anno]}` per impostare l'anno accademico.
  Specificare solo l'anno, ad es. "2015/2016", e non il testo *A/A*.

*Cattedra* e *Correlatore* possono non essere specificati, nel qual caso non compariranno nel frontespizio.
Ogni altro campo deve essere specificato.

Il titolo viene formattato secondo le specifiche fornite dalla Sapienza: colore titolo, facolt&agrave; e corso di laurea `RGB(111,10,25)`, font arial, 20pt per titolo, 10pt per il resto, grassetto per facolt&agrave; e corso di laurea.
Il testo &egrave; allineato a sinistra, sulla *S* del logo Sapienza.

I margini sono impostati (sx,sup,dx,inf) a 4cm, 2.75cm, 2.5cm, 1cm.

I campi vengono stampati nel seguente ordine:
1. Titolo tesi;
2. Facolt&agrave;, corso di laurea, e opzionalmente cattedra;
3. Candidato e matricola;
4. Relatore e opzionalmente correlatore (quest'ultimo spostato verso destra);
5. Anno accademico.

&Egrave; possibile regolare lo spazio verticale fra i diversi campi:
- `\FSSapienzaSpazioTitolo` imposta lo spazio fra logo Sapienza e titolo;
- `\FSSapienzaSpazioFacolta` imposta lo spazio fra titolo e facolt&agrave;
- `\FSSapienzaSpazioCandidato` imposta lo spazio fra facolt&agrave; e candidato;
- `\FSSapienzaSpazioRelatore` imposta lo spazio fra candidato e relatore;
- `\FSSapienzaSpazioAnnoAccademico` imposta lo spazio fra relatore e anno accademico.

Lo spazio fra i campi viene impostato con `\setlength{[nome spazio]}{[valore]}`.

Il file `main.tex` fornisce un esempio di utilizzo del package.

