---
title: Shape.LastParagraph
second_title: Aspose.Words for .NET API Referansı
description: Shape mülk. Şekildeki son paragrafı alır.
type: docs
weight: 120
url: /tr/net/aspose.words.drawing/shape/lastparagraph/
---
## Shape.LastParagraph property

Şekildeki son paragrafı alır.

```csharp
public Paragraph LastParagraph { get; }
```

### Örnekler

Bir metin kutusu içindeki metnin yönünün nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Belge oluşturucuyu TextBox'ın içine taşıyın ve metin ekleyin.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// Bu metin kutusunun metin içeriği için bir yönlendirme ayarlamak için "LayoutFlow" özelliğini ayarlayın.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

### Ayrıca bakınız

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Shape](../)
* ad alanı [Aspose.Words.Drawing](../../shape/)
* toplantı [Aspose.Words](../../../)


