---
title: Font.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words per .NET
description: Ripristina il testo al suo stile originale con il metodo Font ClearFormatting. Goditi una formattazione pulita e coerente per un aspetto impeccabile!
type: docs
weight: 560
url: /it/net/aspose.words/font/clearformatting/
---
## Font.ClearFormatting method

Ripristina la formattazione predefinita del carattere.

```csharp
public void ClearFormatting()
```

## Osservazioni

Rimuove tutta la formattazione del carattere specificata esplicitamente sull'oggetto da which [`Font`](../) è stato ottenuto in modo che la formattazione del carattere venga ereditata dal genitore appropriato .

## Esempi

Mostra come inserire un campo collegamento ipertestuale.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Inserisci un collegamento ipertestuale ed evidenzialo con una formattazione personalizzata.
// Il collegamento ipertestuale sarà un pezzo di testo cliccabile che ci porterà alla posizione specificata nell'URL.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", false);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Facendo clic con il tasto sinistro del mouse sul collegamento nel testo in Microsoft Word verremo indirizzati all'URL tramite una nuova finestra del browser Web.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

### Guarda anche

* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
