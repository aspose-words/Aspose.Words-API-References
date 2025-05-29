---
title: DropCapPosition Enum
linktitle: DropCapPosition
articleTitle: DropCapPosition
second_title: .NET için Aspose.Words
description: Etkili görsel çekicilik için benzersiz büyük harf metin konumları tanımlayarak belge tasarımınızı geliştirmek için Aspose.Words.DropCapPosition enum'unu keşfedin.
type: docs
weight: 1820
url: /tr/net/aspose.words/dropcapposition/
---
## DropCapPosition enumeration

Büyük harfli bir metnin konumunu belirtir.

```csharp
public enum DropCapPosition
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Paragrafta büyük harf kullanılmamıştır. |
| Normal | `1` | Büyük harf, bağlantı paragrafındaki metin kenar boşluğunun içine yerleştirilir. |
| Margin | `2` | Büyük harf, bağlantı paragrafındaki metin kenar boşluğunun dışında konumlandırılır. |

## Örnekler

Büyük harfle başlamanın nasıl yapılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// İkinci ve üçüncü paragraflardaki metnin büyük harfle başladığı bir paragraf ekleyin.
builder.Font.Size = 54;
builder.Writeln("L");

builder.Font.Size = 18;
builder.Writeln("orem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
builder.Writeln("Ut enim ad minim veniam, quis nostrud exercitation " +
                "ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Şimdilik ikinci ve üçüncü paragraflar birinci paragrafın altında görünecek.
// "ParagraphFormat" nesnesi aracılığıyla ilk paragrafı diğer paragraflar için büyük harfle baş harfe dönüştürebiliriz.
// "DropCapPosition" özelliğini "DropCapPosition.Margin" olarak ayarlayın ve büyük harf yerleştirmeyi deneyin
// Metnimiz soldan sağa ise sol sayfa kenar boşluğunun dışında.
// "DropCapPosition" özelliğini "DropCapPosition.Normal" olarak ayarlayın ve büyük harfin sayfa kenar boşluklarına yerleştirilmesini sağlayın
// ve metnin geri kalanını bunun etrafına sarmak için.
// "DropCapPosition.None" tüm paragraflar için varsayılan durumdur.
ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;
format.DropCapPosition = dropCapPosition;

doc.Save(ArtifactsDir + "ParagraphFormat.DropCap.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
