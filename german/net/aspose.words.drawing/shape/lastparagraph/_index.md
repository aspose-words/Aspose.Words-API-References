---
title: LastParagraph
second_title: Aspose.Words für .NET-API-Referenz
description: Ruft den letzten Absatz in der Form ab.
type: docs
weight: 120
url: /de/net/aspose.words.drawing/shape/lastparagraph/
---
## Shape.LastParagraph property

Ruft den letzten Absatz in der Form ab.

```csharp
public Paragraph LastParagraph { get; }
```

### Beispiele

Zeigt, wie die Ausrichtung von Text in einem Textfeld festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Verschieben Sie den Document Builder in die TextBox und fügen Sie Text hinzu.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// Legen Sie die Eigenschaft "LayoutFlow" fest, um eine Ausrichtung für den Textinhalt dieses Textfelds festzulegen.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

### Siehe auch

* class [Paragraph](../../../aspose.words/paragraph)
* class [Shape](../../shape)
* namensraum [Aspose.Words.Drawing](../../shape)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->