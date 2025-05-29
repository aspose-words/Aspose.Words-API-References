---
title: Font.Color
linktitle: Color
articleTitle: Color
second_title: .NET için Aspose.Words
description: Tasarımlarınızdaki metin renklerini kolayca özelleştirmek için Font Color özelliğini keşfedin. Canlı, göz alıcı tonlarla okunabilirliği ve estetiği artırın!
type: docs
weight: 70
url: /tr/net/aspose.words/font/color/
---
## Font.Color property

Yazı tipinin rengini alır veya ayarlar.

```csharp
public Color Color { get; set; }
```

## Örnekler

DocumentBuilder kullanılarak biçimlendirilmiş metnin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Yazı tipi biçimlendirmesini belirtin, ardından metni ekleyin.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

Bir köprü metni alanının nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Bir köprü metni ekleyin ve özel biçimlendirmeyle vurgulayın.
// Köprü metni, URL'de belirtilen yere bizi götürecek tıklanabilir bir metin parçası olacaktır.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", yanlış);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Microsoft Word'de metindeki bağlantıya Ctrl + sol tıklama bizi yeni bir web tarayıcısı penceresi aracılığıyla URL'ye götürecektir.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
