---
title: XpsSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words per .NET
description: Ottimizza il layout del tuo documento con la proprietà UseBookFoldPrintingSettings di XpsSaveOptions, consentendo una stampa di opuscoli senza interruzioni per una presentazione migliore.
type: docs
weight: 50
url: /it/net/aspose.words.saving/xpssaveoptions/usebookfoldprintingsettings/
---
## XpsSaveOptions.UseBookFoldPrintingSettings property

Ottiene o imposta un valore booleano che indica se il documento deve essere salvato utilizzando un layout di stampa opuscolo, se specificato tramite[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## Osservazioni

Se questa opzione è specificata,[`PageSet`](../../fixedpagesaveoptions/pageset/) viene ignorato durante il salvataggio. Questo comportamento corrisponde a MS Word. Se le impostazioni di stampa con piega a libro non sono specificate nell'impostazione della pagina, questa opzione non avrà effetto.

## Esempi

Mostra come salvare un documento nel formato XPS sotto forma di piega a libro.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Creiamo un oggetto "XpsSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions(SaveFormat.Xps);

// Imposta la proprietà "UseBookFoldPrintingSettings" su "true" per organizzare il contenuto
// nell'output XPS in un modo che ci aiuti a utilizzarlo per creare un opuscolo.
// Impostare la proprietà "UseBookFoldPrintingSettings" su "false" per eseguire il rendering XPS normalmente.
xpsOptions.UseBookFoldPrintingSettings = renderTextAsBookFold;

// Se stiamo rendendo il documento come un opuscolo, dobbiamo impostare "MultiplePages"
// proprietà degli oggetti di impostazione pagina di tutte le sezioni su "MultiplePagesType.BookFoldPrinting".
if (renderTextAsBookFold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// Una volta stampato questo documento, possiamo trasformarlo in un opuscolo impilando le pagine
// per uscire dalla stampante e piegarlo al centro.
doc.Save(ArtifactsDir + "XpsSaveOptions.BookFold.xps", xpsOptions);
```

### Guarda anche

* class [XpsSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
