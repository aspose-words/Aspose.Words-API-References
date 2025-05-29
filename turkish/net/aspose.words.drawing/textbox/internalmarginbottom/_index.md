---
title: TextBox.InternalMarginBottom
linktitle: InternalMarginBottom
articleTitle: InternalMarginBottom
second_title: .NET için Aspose.Words
description: Gelişmiş tasarım hassasiyeti için şeklinizin iç alt kenar boşluğunu noktalarla özelleştirmek üzere TextBox InternalMarginBottom özelliğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.drawing/textbox/internalmarginbottom/
---
## TextBox.InternalMarginBottom property

Bir şekil için iç alt kenar boşluğunu noktalarla belirtir.

```csharp
public double InternalMarginBottom { get; set; }
```

## Notlar

Varsayılan değer 1/20 inçtir.

## Örnekler

Bir metin kutusu için iç kenar boşluklarının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belirli kenar boşluklarına sahip başka bir metin kutusu ekle.
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

### Ayrıca bakınız

* class [TextBox](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
