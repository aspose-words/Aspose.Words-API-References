---
title: TextBox.TextBoxWrapMode
linktitle: TextBoxWrapMode
articleTitle: TextBoxWrapMode
second_title: Aspose.Words for .NET
description: TextBox TextBoxWrapMode mülk. Metnin şeklin içinde nasıl kaydırılacağını belirler C#'da.
type: docs
weight: 110
url: /tr/net/aspose.words.drawing/textbox/textboxwrapmode/
---
## TextBox.TextBoxWrapMode property

Metnin şeklin içinde nasıl kaydırılacağını belirler.

```csharp
public TextBoxWrapMode TextBoxWrapMode { get; set; }
```

## Notlar

Varsayılan değer:Square.

## Örnekler

Metin kutusunun içeriği için sarma modunun nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 300, 300);
TextBox textBox = textBoxShape.TextBox;

// Metin kutusunun genişliğini artırmak için "TextBoxWrapMode" özelliğini "TextBoxWrapMode.None" olarak ayarlayın
// yeterince büyük olması durumunda metni yerleştirmek için.
// "TextBoxWrapMode" özelliğini "TextBoxWrapMode.Square" olarak ayarlayın
// tüm metni boyutlarını koruyarak metin kutusunun içine sarın.
textBox.TextBoxWrapMode = textBoxWrapMode;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Font.Size = 32;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "Shape.TextBoxContentsWrapMode.docx");
```

### Ayrıca bakınız

* enum [TextBoxWrapMode](../../textboxwrapmode/)
* class [TextBox](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
