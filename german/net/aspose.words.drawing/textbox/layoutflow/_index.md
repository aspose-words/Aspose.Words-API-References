---
title: TextBox.LayoutFlow
linktitle: LayoutFlow
articleTitle: LayoutFlow
second_title: Aspose.Words für .NET
description: TextBox LayoutFlow eigendom. Bestimmt den Fluss des Textlayouts in einer Form in C#.
type: docs
weight: 60
url: /de/net/aspose.words.drawing/textbox/layoutflow/
---
## TextBox.LayoutFlow property

Bestimmt den Fluss des Textlayouts in einer Form.

```csharp
public LayoutFlow LayoutFlow { get; set; }
```

## Bemerkungen

Der Standardwert istHorizontal.

## Beispiele

Zeigt, wie die Ausrichtung von Text in einem Textfeld festgelegt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Verschieben Sie den Dokument-Builder in die TextBox und fügen Sie Text hinzu.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// Legen Sie die Eigenschaft „LayoutFlow“ fest, um eine Ausrichtung für den Textinhalt dieses Textfelds festzulegen.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

### Siehe auch

* enum [LayoutFlow](../../layoutflow/)
* class [TextBox](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
