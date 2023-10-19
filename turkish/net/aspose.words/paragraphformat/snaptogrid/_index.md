---
title: ParagraphFormat.SnapToGrid
linktitle: SnapToGrid
articleTitle: SnapToGrid
second_title: Aspose.Words for .NET
description: ParagraphFormat SnapToGrid mülk. Geçerli paragrafın paragraftaki içerikleri düzenlerken sayfa başına belge ızgara çizgilerini kullanıp kullanmayacağını ayarlar belirtir C#'da.
type: docs
weight: 290
url: /tr/net/aspose.words/paragraphformat/snaptogrid/
---
## ParagraphFormat.SnapToGrid property

Geçerli paragrafın, paragraftaki içerikleri düzenlerken sayfa başına belge ızgara çizgilerini kullanıp kullanmayacağını ayarlar belirtir.

```csharp
public bool SnapToGrid { get; set; }
```

## Örnekler

Her sayfanın sahip olabileceği satır sayısına ilişkin sınırın nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Perdelemeyi etkinleştirin ve ardından bu bölümdeki sayfa başına satır sayısını ayarlamak için bunu kullanın.
// Yeterince büyük bir yazı tipi boyutu, karakterlerin çakışmasını önlemek için bazı satırları sonraki sayfaya doğru itecektir.
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
