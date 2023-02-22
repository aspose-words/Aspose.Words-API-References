---
title: ParagraphFormat.SnapToGrid
second_title: Aspose.Words for .NET API Referansı
description: ParagraphFormat mülk. Geçerli paragrafın paragraftaki içerikleri düzenlerken sayfa ayarlarına göre belge kılavuz çizgilerini kullanıp kullanmayacağını belirtir .
type: docs
weight: 280
url: /tr/net/aspose.words/paragraphformat/snaptogrid/
---
## ParagraphFormat.SnapToGrid property

Geçerli paragrafın, paragraftaki içerikleri düzenlerken sayfa ayarlarına göre belge kılavuz çizgilerini kullanıp kullanmayacağını belirtir .

```csharp
public bool SnapToGrid { get; set; }
```

### Örnekler

Her sayfanın sahip olabileceği satır sayısı için bir sınırın nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Adım atmayı etkinleştirin ve ardından bu bölümde sayfa başına satır sayısını ayarlamak için kullanın.
// Yeterince büyük bir yazı tipi boyutu, üst üste binen karakterleri önlemek için bazı satırları bir sonraki sayfaya itecektir.
builder.PageSetup.LayoutMode = SectionLayoutMode.LineGrid;
builder.PageSetup.LinesPerPage = 15;

builder.ParagraphFormat.SnapToGrid = true;

for (int i = 0; i < 30; i++)
    builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");

doc.Save(ArtifactsDir + "PageSetup.LinesPerPage.docx");
```

### Ayrıca bakınız

* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../paragraphformat/)
* toplantı [Aspose.Words](../../../)


