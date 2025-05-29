---
title: Font.Size
linktitle: Size
articleTitle: Size
second_title: .NET için Aspose.Words
description: Yazı Tipi Boyutu özelliğiyle yazı tipi boyutunu zahmetsizce ayarlayın. Gelişmiş okunabilirlik ve tasarım çekiciliği için metninizi noktalar halinde özelleştirin.
type: docs
weight: 350
url: /tr/net/aspose.words/font/size/
---
## Font.Size property

Yazı tipi boyutunu nokta cinsinden alır veya ayarlar.

```csharp
public double Size { get; set; }
```

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
