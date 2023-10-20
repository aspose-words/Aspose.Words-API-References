---
title: Shape.LastParagraph
linktitle: LastParagraph
articleTitle: LastParagraph
second_title: Aspose.Words for .NET
description: Shape LastParagraph mülk. Şeklin son paragrafını alır C#'da.
type: docs
weight: 120
url: /tr/net/aspose.words.drawing/shape/lastparagraph/
---
## Shape.LastParagraph property

Şeklin son paragrafını alır.

```csharp
public Paragraph LastParagraph { get; }
```

## Örnekler

Bir metin kutusu içindeki metnin yönünün nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Belge oluşturucuyu TextBox'un içine taşıyın ve metin ekleyin.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// Bu metin kutusunun metin içeriğinin yönünü ayarlamak için "LayoutFlow" özelliğini ayarlayın.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

### Ayrıca bakınız

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Shape](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
