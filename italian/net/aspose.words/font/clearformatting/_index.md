---
title: Font.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words per .NET
description: Font ClearFormatting metodo. Ripristina la formattazione predefinita dei caratteri in C#.
type: docs
weight: 550
url: /it/net/aspose.words/font/clearformatting/
---
## Font.ClearFormatting method

Ripristina la formattazione predefinita dei caratteri.

```csharp
public void ClearFormatting()
```

## Osservazioni

Rimuove tutta la formattazione dei caratteri specificata esplicitamente sull'oggetto da cui [`Font`](../) è stato ottenuto in modo che la formattazione del carattere venga ereditata da il genitore appropriato.

## Esempi

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
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
