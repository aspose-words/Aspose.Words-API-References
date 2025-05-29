---
title: ParagraphFormat.SnapToGrid
linktitle: SnapToGrid
articleTitle: SnapToGrid
second_title: .NET için Aspose.Words
description: ParagraphFormat SnapToGrid özelliğinin, paragraflarınızı belge kılavuz çizgileriyle hizalayarak düzen hassasiyetini nasıl artırdığını ve cilalı bir görünüm sağladığını keşfedin.
type: docs
weight: 300
url: /tr/net/aspose.words/paragraphformat/snaptogrid/
---
## ParagraphFormat.SnapToGrid property

Geçerli paragrafın, paragraftaki içerikleri düzenlerken sayfa başına belge kılavuz çizgileri ayarlarını kullanıp kullanmayacağını belirtir.

```csharp
public bool SnapToGrid { get; set; }
```

## Örnekler

Her sayfanın sahip olabileceği satır sayısı için bir sınır belirlemenin nasıl yapılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Atışı etkinleştirin ve ardından bunu bu bölümdeki sayfa başına satır sayısını ayarlamak için kullanın.
// Yeterince büyük bir yazı tipi boyutu, karakterlerin üst üste gelmesini önlemek için bazı satırların bir sonraki sayfaya doğru itilmesini sağlayacaktır.
builder.PageSetup.LayoutMode = SectionLayoutMode.LineGrid;
builder.PageSetup.LinesPerPage = 15;

builder.ParagraphFormat.SnapToGrid = true;

for (int i = 0; i < 30; i++)
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.Save(ArtifactsDir + "PageSetup.LinesPerPage.docx");
```

### Ayrıca bakınız

* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
