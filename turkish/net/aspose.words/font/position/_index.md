---
title: Font.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words for .NET
description: Font Position mülk. Metnin konumunu nokta cinsinden taban çizgisine göre alır veya ayarlar. Pozitif bir sayı metni yükseltir negatif bir sayı ise alçaltır C#'da.
type: docs
weight: 300
url: /tr/net/aspose.words/font/position/
---
## Font.Position property

Metnin konumunu (nokta cinsinden) taban çizgisine göre alır veya ayarlar. Pozitif bir sayı metni yükseltir, negatif bir sayı ise alçaltır.

```csharp
public double Position { get; set; }
```

## Örnekler

Konumunu dengelemek için metnin nasıl biçimlendirileceğini gösterir.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Bu metin dizisini taban çizgisinin 5 puan üstüne yükseltin.
Run run = new Run(doc, "Raised text. ");
run.Font.Position = 5;
para.AppendChild(run);

// Bu metin dizisini taban çizgisinin 10 puan altına indirin.
run = new Run(doc, "Lowered text. ");
run.Font.Position = -10;
para.AppendChild(run);

// Bir dizi normal metin ekleyin.
run = new Run(doc, "Text in its default position. ");
para.AppendChild(run);

// Alt simge olarak görünen bir metin dizisi ekleyin.
run = new Run(doc, "Subscript. ");
run.Font.Subscript = true;
para.AppendChild(run);

// Üst simge olarak görünen bir metin dizisi ekleyin.
run = new Run(doc, "Superscript.");
run.Font.Superscript = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.PositionSubscript.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
