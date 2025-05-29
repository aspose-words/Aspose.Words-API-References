---
title: PdfSaveOptions.OpenHyperlinksInNewWindow
linktitle: OpenHyperlinksInNewWindow
articleTitle: OpenHyperlinksInNewWindow
second_title: Aspose.Words per .NET
description: Controlla il comportamento dei collegamenti ipertestuali nel tuo PDF con PdfSaveOptions. Imposta facilmente i link in modo che si aprano in una nuova finestra o scheda per un'esperienza utente migliorata.
type: docs
weight: 230
url: /it/net/aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow/
---
## PdfSaveOptions.OpenHyperlinksInNewWindow property

Ottiene o imposta un valore che determina se i collegamenti ipertestuali nel documento Pdf di output devono essere forzati ad essere aperti in una nuova finestra (o scheda) di un browser.

```csharp
public bool OpenHyperlinksInNewWindow { get; set; }
```

## Osservazioni

Il valore predefinito è`falso` Quando questo valore è impostato su`VERO` i collegamenti ipertestuali vengono salvati utilizzando il codice JavaScript. il codice JavaScript è`app.launchURL("URL", true);` , dove`URL` è un collegamento ipertestuale.

Nota che se questa opzione è impostata su`VERO` i collegamenti ipertestuali non funzionano in alcuni lettori PDF, ad esempio Chrome, Firefox.

Le azioni JavaScript sono vietate dalla conformità PDF/A-1 e PDF/A-2.`falso`verrà utilizzato automaticamente quando si salva in formato PDF/A-1 e PDF/A-2.

## Esempi

Mostra come salvare i collegamenti ipertestuali in un documento che convertiamo in PDF, in modo che aprano nuove pagine quando clicchiamo su di essi.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertHyperlink("Testlink", @"https://www.google.com/search?q=%20aspose", false);

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Imposta la proprietà "OpenHyperlinksInNewWindow" su "true" per salvare tutti i collegamenti ipertestuali utilizzando il codice Javascript
// che obbliga i lettori ad aprire questi link in nuove finestre/schede del browser.
// Impostare la proprietà "OpenHyperlinksInNewWindow" su "false" per salvare normalmente tutti i collegamenti ipertestuali.
options.OpenHyperlinksInNewWindow = openHyperlinksInNewWindow;

doc.Save(ArtifactsDir + "PdfSaveOptions.OpenHyperlinksInNewWindow.pdf", options);
```

### Guarda anche

* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
