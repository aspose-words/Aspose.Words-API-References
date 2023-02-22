---
title: Font.Superscript
second_title: Aspose.Words for .NET API Referansı
description: Font mülk. Yazı tipi üst simge olarak biçimlendirilmişse doğrudur.
type: docs
weight: 440
url: /tr/net/aspose.words/font/superscript/
---
## Font.Superscript property

Yazı tipi üst simge olarak biçimlendirilmişse doğrudur.

```csharp
public bool Superscript { get; set; }
```

### Örnekler

Konumunu dengelemek için metnin nasıl biçimlendirileceğini gösterir.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph) doc.GetChild(NodeType.Paragraph, 0, true);

// Bu metin akışını taban çizgisinin 5 puan üzerine yükseltin.
Run run = new Run(doc, "Raised text. ");
run.Font.Position = 5;
para.AppendChild(run);

// Bu metin akışını taban çizgisinin 10 puan altına indirin.
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
* ad alanı [Aspose.Words](../../font/)
* toplantı [Aspose.Words](../../../)


