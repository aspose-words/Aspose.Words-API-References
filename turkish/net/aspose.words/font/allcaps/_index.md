---
title: Font.AllCaps
linktitle: AllCaps
articleTitle: AllCaps
second_title: .NET için Aspose.Words
description: Font AllCaps özelliğini keşfedin. Projelerinizde gelişmiş okunabilirlik ve etkili tasarım için metni kolayca tüm büyük harflerle biçimlendirin.
type: docs
weight: 10
url: /tr/net/aspose.words/font/allcaps/
---
## Font.AllCaps property

Yazı tipi tamamen büyük harf olarak biçimlendirilmişse doğrudur.

```csharp
public bool AllCaps { get; set; }
```

## Örnekler

Bir çalışmanın içeriğini büyük harflerle gösterecek şekilde nasıl biçimlendirileceğini gösterir.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// İçeriği değiştirmeden bir çalışmanın küçük harfli metnini büyük harfle göstermesini sağlamanın iki yolu vardır.
// 1 - Tüm karakterleri normal büyük harflerle görüntülemek için AllCaps bayrağını ayarlayın:
Run run = new Run(doc, "all capitals");
run.Font.AllCaps = true;
para.AppendChild(run);

para = (Paragraph)para.ParentNode.AppendChild(new Paragraph(doc));

// 2 - Tüm karakterleri küçük harflerle görüntülemek için SmallCaps bayrağını ayarlayın:
// Eğer bir karakter küçük harfliyse, büyük harfli haliyle görünecektir
// ancak küçük harfle aynı yüksekliğe sahip olacaktır (yazı tipinin x yüksekliği).
// Başlangıçta büyük harfle yazılmış olan karakterler aynı görünecek.
run = new Run(doc, "Small Capitals");
run.Font.SmallCaps = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.Caps.docx");
```

### Ayrıca bakınız

* class [Font](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
