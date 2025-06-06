---
title: Font.Position
linktitle: Position
articleTitle: Position
second_title: .NET için Aspose.Words
description: Font Position özelliğini keşfedin, tipografiniz üzerinde hassas kontrol için noktalardaki metin hizalamasını kolayca ayarlayın. Esnek konumlandırma ile tasarımınızı yükseltin!
type: docs
weight: 310
url: /tr/net/aspose.words/font/position/
---
## Font.Position property

Metnin taban çizgisine göre konumunu (nokta cinsinden) alır veya ayarlar. Pozitif bir sayı metni yükseltir ve negatif bir sayı düşürür.

```csharp
public double Position { get; set; }
```

## Örnekler

Metnin konumunu kaydıracak şekilde nasıl biçimlendirileceğini gösterir.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Bu metin dizisini taban çizgisinin 5 puan üzerine yükseltin.
Run run = new Run(doc, "Raised text. ");
run.Font.Position = 5;
para.AppendChild(run);

// Bu metin dizisini başlangıç çizgisinin 10 puan altına indirin.
run = new Run(doc, "Lowered text. ");
run.Font.Position = -10;
para.AppendChild(run);

// Normal metinden oluşan bir bölüm ekle.
run = new Run(doc, "Text in its default position. ");
para.AppendChild(run);

// Alt simge olarak görünen bir metin dizisi ekleyin.
run = new Run(doc, "Subscript. ");
run.Font.Subscript = true;
para.AppendChild(run);

// Üst simge olarak görünen bir metin parçası ekleyin.
run = new Run(doc, "Superscript.");
run.Font.Superscript = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.PositionSubscript.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
