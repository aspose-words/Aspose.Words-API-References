---
title: TextBoxWrapMode Enum
linktitle: TextBoxWrapMode
articleTitle: TextBoxWrapMode
second_title: .NET için Aspose.Words
description: Şekillerdeki metin kaydırmayı kontrol etmek, belge düzenlerini ve tasarım esnekliğini geliştirmek için Aspose.Words.Drawing.TextBoxWrapMode enum'unu keşfedin.
type: docs
weight: 1750
url: /tr/net/aspose.words.drawing/textboxwrapmode/
---
## TextBoxWrapMode enumeration

Metnin bir şeklin içinde nasıl sarılacağını belirtir.

```csharp
public enum TextBoxWrapMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Square | `0` | Metin bir şeklin içine sarılır. |
| None | `2` | Metin bir şeklin içine sarılmıyor. |

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

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
