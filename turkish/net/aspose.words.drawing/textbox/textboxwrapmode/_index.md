---
title: TextBox.TextBoxWrapMode
linktitle: TextBoxWrapMode
articleTitle: TextBoxWrapMode
second_title: .NET için Aspose.Words
description: Tasarımınızın netliğini ve görsel çekiciliğini artırmak için şekiller içindeki metin kaydırmayı geliştirmek amacıyla TextBox WrapMode özelliğini keşfedin.
type: docs
weight: 110
url: /tr/net/aspose.words.drawing/textbox/textboxwrapmode/
---
## TextBox.TextBoxWrapMode property

Metnin bir şeklin içinde nasıl sarılacağını belirler.

```csharp
public TextBoxWrapMode TextBoxWrapMode { get; set; }
```

## Notlar

Varsayılan değer:Square.

## Örnekler

Bir metin kutusunun içeriği için kaydırma modunun nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 300, 300);
TextBox textBox = textBoxShape.TextBox;

// Metin kutusunun genişliğini artırmak için "TextBoxWrapMode" özelliğini "TextBoxWrapMode.None" olarak ayarlayın
// metni barındıracak kadar büyük olmalıdır.
// "TextBoxWrapMode" özelliğini "TextBoxWrapMode.Square" olarak ayarlayın
// metin kutusunun içindeki tüm metni, boyutlarını koruyarak sar.
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
