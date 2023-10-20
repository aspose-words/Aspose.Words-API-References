---
title: ShapeBase.Target
linktitle: Target
articleTitle: Target
second_title: Aspose.Words per .NET
description: ShapeBase Target proprietà. Ottiene o imposta il frame di destinazione per il collegamento ipertestuale della forma in C#.
type: docs
weight: 520
url: /it/net/aspose.words.drawing/shapebase/target/
---
## ShapeBase.Target property

Ottiene o imposta il frame di destinazione per il collegamento ipertestuale della forma.

```csharp
public string Target { get; set; }
```

## Osservazioni

Il valore predefinito è una stringa vuota.

## Esempi

Mostra come inserire una forma che contiene un'immagine ed è anche un collegamento ipertestuale.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.HRef = "https://forum.aspose.com/";
shape.Target = "New Window";
shape.ScreenTip = "Aspose.Words Support Forums";

// Ctrl + facendo clic con il pulsante sinistro del mouse sulla forma in Microsoft Word si aprirà una nuova finestra del browser Web
// e portaci al collegamento ipertestuale nella proprietà "HRef".
doc.Save(ArtifactsDir + "Image.InsertImageWithHyperlink.docx");
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
