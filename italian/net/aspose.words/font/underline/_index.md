---
title: Font.Underline
linktitle: Underline
articleTitle: Underline
second_title: Aspose.Words per .NET
description: Scopri la proprietà "Carattere Sottolineato" per personalizzare gli stili di testo. Imposta e modifica facilmente i tipi di sottolineatura per una tipografia migliorata nei tuoi progetti.
type: docs
weight: 540
url: /it/net/aspose.words/font/underline/
---
## Font.Underline property

Ottiene o imposta il tipo di sottolineatura applicato al font.

```csharp
public Underline Underline { get; set; }
```

## Esempi

Mostra come configurare lo stile e il colore della sottolineatura del testo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Underline = Underline.Dotted;
builder.Font.UnderlineColor = Color.Red;

builder.Writeln("Underlined text.");

doc.Save(ArtifactsDir + "Font.Underlines.docx");
```

Mostra come inserire testo formattato utilizzando DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Specificare la formattazione del carattere, quindi aggiungere il testo.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

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

* enum [Underline](../../underline/)
* class [Font](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
