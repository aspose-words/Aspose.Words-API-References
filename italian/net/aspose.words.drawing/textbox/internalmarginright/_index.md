---
title: TextBox.InternalMarginRight
second_title: Aspose.Words per .NET API Reference
description: TextBox proprietà. Specifica il margine interno destro in punti per una forma.
type: docs
weight: 40
url: /it/net/aspose.words.drawing/textbox/internalmarginright/
---
## TextBox.InternalMarginRight property

Specifica il margine interno destro in punti per una forma.

```csharp
public double InternalMarginRight { get; set; }
```

### Osservazioni

Il valore predefinito è 1/10 di pollice.

### Esempi

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
* spazio dei nomi [Aspose.Words.Drawing](../../textbox/)
* assemblea [Aspose.Words](../../../)


