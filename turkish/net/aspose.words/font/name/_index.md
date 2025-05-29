---
title: Font.Name
linktitle: Name
articleTitle: Name
second_title: .NET için Aspose.Words
description: Tasarımınızın çekiciliğini ve okunabilirliğini artırmak için yazı tipi stillerini kolayca özelleştirmek ve ayarlamak üzere Yazı Tipi Adı özelliğini keşfedin.
type: docs
weight: 230
url: /tr/net/aspose.words/font/name/
---
## Font.Name property

Yazı tipinin adını alır veya ayarlar.

```csharp
public string Name { get; set; }
```

## Notlar

Alırken, iade ederken[`NameAscii`](../nameascii/).

Ayarlarken, ayarlar[`NameAscii`](../nameascii/) ,[`NameBi`](../namebi/) ,[`NameFarEast`](../namefareast/) ve[`NameOther`](../nameother/) belirtilen değere.

## Örnekler

Bir metin dizisinin font özelliğini kullanarak nasıl biçimlendirileceğini gösterir.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
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

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
