---
title: TextBox.InternalMarginBottom
linktitle: InternalMarginBottom
articleTitle: InternalMarginBottom
second_title: Aspose.Words per .NET
description: Scopri la proprietà TextBox InternalMarginBottom per personalizzare il margine inferiore interno della tua forma in punti, per una maggiore precisione di progettazione.
type: docs
weight: 20
url: /it/net/aspose.words.drawing/textbox/internalmarginbottom/
---
## TextBox.InternalMarginBottom property

Specifica il margine inferiore interno in punti per una forma.

```csharp
public double InternalMarginBottom { get; set; }
```

## Osservazioni

Il valore predefinito è 1/20 di pollice.

## Esempi

Mostra come impostare i margini interni per una casella di testo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce un'altra casella di testo con margini specifici.
Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 100, 100);
TextBox textBox = textBoxShape.TextBox;
textBox.InternalMarginTop = 15;
textBox.InternalMarginBottom = 15;
textBox.InternalMarginLeft = 15;
textBox.InternalMarginRight = 15;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Write("Text placed according to textbox margins.");

doc.Save(ArtifactsDir + "Shape.TextBoxMargins.docx");
```

### Guarda anche

* class [TextBox](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
