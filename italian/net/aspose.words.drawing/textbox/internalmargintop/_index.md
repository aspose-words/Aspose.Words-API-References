---
title: TextBox.InternalMarginTop
linktitle: InternalMarginTop
articleTitle: InternalMarginTop
second_title: Aspose.Words per .NET
description: TextBox InternalMarginTop proprietà. Specifica il margine superiore interno in punti per una forma in C#.
type: docs
weight: 50
url: /it/net/aspose.words.drawing/textbox/internalmargintop/
---
## TextBox.InternalMarginTop property

Specifica il margine superiore interno in punti per una forma.

```csharp
public double InternalMarginTop { get; set; }
```

## Osservazioni

Il valore predefinito è 1/20 di pollice.

## Esempi

Mostra come impostare i margini interni per una casella di testo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci un'altra casella di testo con margini specifici.
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
