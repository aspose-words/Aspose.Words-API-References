---
title: Font.Color
second_title: Aspose.Words per .NET API Reference
description: Font proprietà. Ottiene o imposta il colore del carattere.
type: docs
weight: 70
url: /it/net/aspose.words/font/color/
---
## Font.Color property

Ottiene o imposta il colore del carattere.

```csharp
public Color Color { get; set; }
```

### Esempi

Mostra come inserire testo formattato utilizzando DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Specifica la formattazione del carattere, quindi aggiunge il testo.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

Mostra come inserire un campo di collegamento ipertestuale.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Inserisci un collegamento ipertestuale ed enfatizzalo con una formattazione personalizzata.
// Il collegamento ipertestuale sarà un pezzo di testo cliccabile che ci porterà alla posizione specificata nell'URL.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", falso);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Ctrl + clic con il pulsante sinistro del mouse sul collegamento nel testo in Microsoft Word ci porterà all'URL tramite una nuova finestra del browser web.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

### Guarda anche

* class [Font](../)
* spazio dei nomi [Aspose.Words](../../font/)
* assemblea [Aspose.Words](../../../)


