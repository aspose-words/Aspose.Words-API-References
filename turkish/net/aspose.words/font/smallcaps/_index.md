---
title: Font.SmallCaps
linktitle: SmallCaps
articleTitle: SmallCaps
second_title: .NET için Aspose.Words
description: Font SmallCaps özelliğini keşfedin. Tasarımlarınızda gelişmiş okunabilirlik ve şık bir görünüm için metni kolayca küçük büyük harflerle biçimlendirin.
type: docs
weight: 370
url: /tr/net/aspose.words/font/smallcaps/
---
## Font.SmallCaps property

Yazı tipi küçük büyük harflerle biçimlendirilmişse doğrudur.

```csharp
public bool SmallCaps { get; set; }
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
