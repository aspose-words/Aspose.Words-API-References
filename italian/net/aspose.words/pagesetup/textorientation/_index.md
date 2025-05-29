---
title: PageSetup.TextOrientation
linktitle: TextOrientation
articleTitle: TextOrientation
second_title: Aspose.Words per .NET
description: Scopri la proprietà TextOrientation di PageSetup per impostare facilmente l'orientamento del testo sulla pagina. Personalizza il tuo layout con opzioni che vanno oltre l'impostazione predefinita "Orizzontale".
type: docs
weight: 430
url: /it/net/aspose.words/pagesetup/textorientation/
---
## PageSetup.TextOrientation property

Permette di specificare`TextOrientation` per l'intera pagina. Il valore predefinito èHorizontal

```csharp
public TextOrientation TextOrientation { get; set; }
```

## Osservazioni

Questa proprietà è supportata solo per i formati nativi di MS Word DOCX, WML, RTF e DOC.

## Esempi

Mostra come impostare l'orientamento del testo.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Imposta la proprietà "TextOrientation" su "TextOrientation.Upward" per ruotare tutto il testo di 90 gradi
// verso destra in modo che tutto il testo da sinistra a destra vada dall'alto verso il basso.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TextOrientation = TextOrientation.Upward;

doc.Save(ArtifactsDir + "PageSetup.SetTextOrientation.docx");
```

### Guarda anche

* enum [TextOrientation](../../textorientation/)
* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
