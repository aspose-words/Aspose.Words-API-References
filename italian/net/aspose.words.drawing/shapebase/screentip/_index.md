---
title: ShapeBase.ScreenTip
linktitle: ScreenTip
articleTitle: ScreenTip
second_title: Aspose.Words per .NET
description: Scopri la proprietà ShapeBase ScreenTip e migliora l'esperienza utente personalizzando il testo della descrizione comandi che appare quando si passa il mouse sulle forme.
type: docs
weight: 510
url: /it/net/aspose.words.drawing/shapebase/screentip/
---
## ShapeBase.ScreenTip property

Definisce il testo visualizzato quando il puntatore del mouse si sposta sulla forma.

```csharp
public string ScreenTip { get; set; }
```

## Osservazioni

Il valore predefinito è una stringa vuota.

## Esempi

Mostra come inserire una forma che contiene un'immagine e che è anche un collegamento ipertestuale.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://forum.aspose.com/";
shape.Target = "New Window";
shape.ScreenTip = "Aspose.Words Support Forums";

// Facendo clic con il tasto sinistro del mouse sulla forma in Microsoft Word si aprirà una nuova finestra del browser Web
// e ci porta al collegamento ipertestuale nella proprietà "HRef".
doc.Save(ArtifactsDir + "Image.InsertImageWithHyperlink.docx");
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
