---
title: TextBox.InternalMarginLeft
linktitle: InternalMarginLeft
articleTitle: InternalMarginLeft
second_title: .NET için Aspose.Words
description: Şeklinizin iç sol kenar boşluğunu noktalar halinde özelleştirerek gelişmiş tasarım esnekliği elde etmek için TextBox InternalMarginLeft özelliğini keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.drawing/textbox/internalmarginleft/
---
## TextBox.InternalMarginLeft property

Bir şekil için iç sol kenar boşluğunu noktalarla belirtir.

```csharp
public double InternalMarginLeft { get; set; }
```

## Notlar

Varsayılan değer 1/10 inçtir.

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
