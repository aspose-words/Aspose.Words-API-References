---
title: TextBox.FitShapeToText
linktitle: FitShapeToText
articleTitle: FitShapeToText
second_title: Aspose.Words per .NET
description: Scopri come la proprietà FitShapeToText di Microsoft Word adatta automaticamente le forme per adattarle perfettamente al testo, migliorando la presentazione del documento.
type: docs
weight: 10
url: /it/net/aspose.words.drawing/textbox/fitshapetotext/
---
## TextBox.FitShapeToText property

Determina se Microsoft Word ingrandirà la forma per adattarla al testo.

```csharp
public bool FitShapeToText { get; set; }
```

## Osservazioni

Il valore predefinito è`falso`.

## Esempi

Mostra come ridimensionare una casella di testo per adattarla perfettamente al suo contenuto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Applica questi valori a entrambi i membri per adattare la forma padre
// strettamente attorno al contenuto del testo, ignorando le dimensioni che abbiamo impostato.
textBox.FitShapeToText = true;
textBox.TextBoxWrapMode = TextBoxWrapMode.None;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text fit tightly inside textbox.");

doc.Save(ArtifactsDir + "Shape.TextBoxFitShapeToText.docx");
```

### Guarda anche

* class [TextBox](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
