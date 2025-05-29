---
title: Shape.TextBox
linktitle: TextBox
articleTitle: TextBox
second_title: Aspose.Words für .NET
description: Passen Sie die Eigenschaften Ihrer Shape-TextBox an, um die Textanzeige zu verbessern und die visuelle Attraktivität Ihrer Designs zu steigern. Entfesseln Sie noch heute Ihr kreatives Potenzial!
type: docs
weight: 230
url: /de/net/aspose.words.drawing/shape/textbox/
---
## Shape.TextBox property

Definiert Attribute, die angeben, wie Text in einer Form angezeigt wird.

```csharp
public TextBox TextBox { get; }
```

## Beispiele

Zeigt, wie die Ausrichtung von Text in einem Textfeld festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Verschieben Sie den Dokumentgenerator in das Textfeld und fügen Sie Text hinzu.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// Legen Sie die Eigenschaft „LayoutFlow“ fest, um eine Ausrichtung für den Textinhalt dieses Textfelds festzulegen.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

### Siehe auch

* class [TextBox](../../textbox/)
* class [Shape](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
