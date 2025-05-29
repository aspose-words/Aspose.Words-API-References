---
title: Shape.LastParagraph
linktitle: LastParagraph
articleTitle: LastParagraph
second_title: Aspose.Words für .NET
description: Greifen Sie auf die Eigenschaft „LastParagraph“ zu, um einfach den letzten Absatz in Ihrer Form abzurufen und so das Layout und die Lesbarkeit Ihres Dokuments zu verbessern.
type: docs
weight: 130
url: /de/net/aspose.words.drawing/shape/lastparagraph/
---
## Shape.LastParagraph property

Ruft den letzten Absatz in der Form ab.

```csharp
public Paragraph LastParagraph { get; }
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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Shape](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
