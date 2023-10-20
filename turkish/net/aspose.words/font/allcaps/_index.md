---
title: Font.AllCaps
linktitle: AllCaps
articleTitle: AllCaps
second_title: Aspose.Words for .NET
description: Font AllCaps mülk. Yazı tipinin tamamı büyük harflerle biçimlendirilmişse doğrudur C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words/font/allcaps/
---
## Font.AllCaps property

Yazı tipinin tamamı büyük harflerle biçimlendirilmişse doğrudur.

```csharp
public bool AllCaps { get; set; }
```

## Örnekler

Bir çalıştırmanın içeriğini büyük harflerle görüntüleyecek şekilde nasıl biçimlendirileceğini gösterir.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// İçeriği değiştirmeden küçük harfli metni büyük harfle gösterecek şekilde çalıştırmanın iki yolu vardır.
// 1 - Tüm karakterleri normal büyük harflerle görüntülemek için AllCaps bayrağını ayarlayın:
Run run = new Run(doc, "all capitals");
run.Font.AllCaps = true;
para.AppendChild(run);

para = (Paragraph)para.ParentNode.AppendChild(new Paragraph(doc));

// 2 - SmallCaps bayrağını tüm karakterleri küçük harflerle gösterecek şekilde ayarlayın:
// Bir karakter küçük harf ise büyük harf biçiminde görünecektir
// ancak küçük harfle aynı yüksekliğe sahip olacaktır (yazı tipinin x yüksekliği).
// Başlangıçta büyük harf olan karakterler aynı görünecektir.
run = new Run(doc, "Small Capitals");
run.Font.SmallCaps = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.Caps.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
