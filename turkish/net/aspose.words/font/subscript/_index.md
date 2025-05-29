---
title: Font.Subscript
linktitle: Subscript
articleTitle: Subscript
second_title: .NET için Aspose.Words
description: Font Subscript özelliğini keşfedin. Belgelerinizde gelişmiş okunabilirlik ve stil için metni kolayca subscript olarak biçimlendirin. Tasarımınızı bugün geliştirin!
type: docs
weight: 440
url: /tr/net/aspose.words/font/subscript/
---
## Font.Subscript property

Yazı tipi alt simge olarak biçimlendirilmişse doğrudur.

```csharp
public bool Subscript { get; set; }
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
