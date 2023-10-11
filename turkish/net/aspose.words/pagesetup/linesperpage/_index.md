---
title: PageSetup.LinesPerPage
second_title: Aspose.Words for .NET API Referansı
description: PageSetup mülk. Belge kılavuzundaki sayfa başına satır sayısını alır veya ayarlar.
type: docs
weight: 240
url: /tr/net/aspose.words/pagesetup/linesperpage/
---
## PageSetup.LinesPerPage property

Belge kılavuzundaki sayfa başına satır sayısını alır veya ayarlar.

```csharp
public int LinesPerPage { get; set; }
```

### Notlar

Özelliğin minimum değeri 1'dir. Maksimum değer, Normal stilinin sayfa yüksekliğine ve yazı tipi boyutuna bağlıdır. Minimum satır aralığı yazı tipi boyutunun yüzde 136'sıdır. Örneğin, bir inç kenar boşluklarına sahip bir Letter sayfasının sayfası başına maksimum satır sayısı 39'dur.

Varsayılan olarak özellik, satır aralığının Normal stildeki yazı tipi boyutundan 1,5 kat daha büyük olduğu bir değere sahiptir.

### Örnekler

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

* class [PageSetup](../)
* ad alanı [Aspose.Words](../../pagesetup/)
* toplantı [Aspose.Words](../../../)


