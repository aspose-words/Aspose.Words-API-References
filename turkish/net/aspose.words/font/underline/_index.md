---
title: Font.Underline
linktitle: Underline
articleTitle: Underline
second_title: .NET için Aspose.Words
description: Metin stillerini özelleştirmek için Font Underline özelliğini keşfedin. Tasarımlarınızda gelişmiş tipografi için alt çizgi türlerini kolayca ayarlayın ve değiştirin.
type: docs
weight: 540
url: /tr/net/aspose.words/font/underline/
---
## Font.Underline property

Yazı tipine uygulanan alt çizginin türünü alır veya ayarlar.

```csharp
public Underline Underline { get; set; }
```

## Örnekler

Bir metnin altını çizmenin stilini ve rengini nasıl yapılandıracağınızı gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Underline = Underline.Dotted;
builder.Font.UnderlineColor = Color.Red;

builder.Writeln("Underlined text.");

doc.Save(ArtifactsDir + "Font.Underlines.docx");
```

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

* enum [Underline](../../underline/)
* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
