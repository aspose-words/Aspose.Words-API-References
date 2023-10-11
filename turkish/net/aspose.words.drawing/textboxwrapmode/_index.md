---
title: Enum TextBoxWrapMode
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Drawing.TextBoxWrapMode Sıralama. Metnin şeklin içinde nasıl kaydırılacağını belirtir.
type: docs
weight: 1340
url: /tr/net/aspose.words.drawing/textboxwrapmode/
---
## TextBoxWrapMode enumeration

Metnin şeklin içinde nasıl kaydırılacağını belirtir.

```csharp
public enum TextBoxWrapMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Square | `0` | Metin bir şeklin içine sarılır. |
| None | `2` | Metin şeklin içine sarılmıyor. |

### Örnekler

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

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)


