---
title: Font.Underline
linktitle: Underline
articleTitle: Underline
second_title: Aspose.Words for .NET
description: Font Underline mülk. Yazı tipine uygulanan alt çizgi türünü alır veya ayarlar C#'da.
type: docs
weight: 530
url: /tr/net/aspose.words/font/underline/
---
## Font.Underline property

Yazı tipine uygulanan alt çizgi türünü alır veya ayarlar.

```csharp
public Underline Underline { get; set; }
```

## Örnekler

Metnin alt çizgisinin stilinin ve renginin nasıl yapılandırılacağını gösterir.

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

// Yazı tipi formatını belirtin, ardından metin ekleyin.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

Köprü alanının nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("For more information, please visit the ");

// Bir köprü ekleyin ve bunu özel biçimlendirmeyle vurgulayın.
// Köprü, bizi URL'de belirtilen konuma götürecek tıklanabilir bir metin parçası olacaktır.
builder.Font.Color = Color.Blue;
builder.Font.Underline = Underline.Single;
builder.InsertHyperlink("Google website", "https://www.google.com", false);
builder.Font.ClearFormatting();
builder.Writeln(".");

// Microsoft Word'deki metindeki bağlantıya Ctrl + sol tıklamak bizi yeni bir web tarayıcı penceresi aracılığıyla URL'ye götürecektir.
doc.Save(ArtifactsDir + "DocumentBuilder.InsertHyperlink.docx");
```

### Ayrıca bakınız

* enum [Underline](../../underline/)
* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
