---
title: Enum DropCapPosition
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.DropCapPosition Sıralama. Gömme metninin konumunu belirtir.
type: docs
weight: 1410
url: /tr/net/aspose.words/dropcapposition/
---
## DropCapPosition enumeration

Gömme metninin konumunu belirtir.

```csharp
public enum DropCapPosition
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Paragrafta büyük harf yoktur. |
| Normal | `1` | Gömme, bağlantı paragrafındaki metin kenar boşluğunun içine yerleştirilir. |
| Margin | `2` | Gömme, bağlantı paragrafındaki metin kenar boşluğunun dışına yerleştirilir. |

### Örnekler

Gömme işleminin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// İkinci ve üçüncü paragraflardaki metnin başlayacağı büyük harfli bir paragraf ekleyin.
builder.Font.Size = 54;
builder.Writeln("L");

builder.Font.Size = 18;
builder.Writeln("orem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
builder.Writeln("Ut enim ad minim veniam, quis nostrud exercitation " +
                "ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Şu anda ikinci ve üçüncü paragraflar birincinin altında görünecek.
// "ParagraphFormat" nesnesi aracılığıyla ilk paragrafı diğer paragraflar için büyük harf olarak dönüştürebiliriz.
// Gömmeyi yerleştirmek için "DropCapPosition" özelliğini "DropCapPosition.Margin" olarak ayarlayın
// metnimiz soldan sağa ise sol taraftaki sayfa kenar boşluğunun dışında.
// Gömmeyi sayfa kenar boşluklarına yerleştirmek için "DropCapPosition" özelliğini "DropCapPosition.Normal" olarak ayarlayın
// ve metnin geri kalanını onun etrafına sarmak için.
// "DropCapPosition.None" tüm paragraflar için varsayılan durumdur.
ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;
format.DropCapPosition = dropCapPosition;

doc.Save(ArtifactsDir + "ParagraphFormat.DropCap.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


