---
title: Shape.TextBox
linktitle: TextBox
articleTitle: TextBox
second_title: .NET için Aspose.Words
description: Tasarımlarınızda metin gösterimini geliştirmek ve görsel çekiciliği artırmak için Shape TextBox özelliklerinizi özelleştirin. Bugün yaratıcı potansiyeli açığa çıkarın!
type: docs
weight: 230
url: /tr/net/aspose.words.drawing/shape/textbox/
---
## Shape.TextBox property

Metnin bir şekil içinde nasıl görüntüleneceğini belirten nitelikleri tanımlar.

```csharp
public TextBox TextBox { get; }
```

## Örnekler

Bir metin kutusunun içindeki metnin yönünün nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Belge oluşturucuyu TextBox'ın içine taşıyın ve metin ekleyin.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// Bu metin kutusunun metin içeriği için bir yönlendirme belirlemek üzere "LayoutFlow" özelliğini ayarlayın.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

### Ayrıca bakınız

* class [TextBox](../../textbox/)
* class [Shape](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
