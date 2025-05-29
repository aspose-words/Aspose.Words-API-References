---
title: PageSetup.LinesPerPage
linktitle: LinesPerPage
articleTitle: LinesPerPage
second_title: .NET için Aspose.Words
description: Belge düzeninizi PageSetup LinesPerPage özelliğiyle kontrol edin. En iyi okunabilirlik ve organizasyon için sayfa başına satırları kolayca ayarlayın.
type: docs
weight: 240
url: /tr/net/aspose.words/pagesetup/linesperpage/
---
## PageSetup.LinesPerPage property

Belge ızgarasında sayfa başına satır sayısını alır veya ayarlar.

```csharp
public int LinesPerPage { get; set; }
```

## Notlar

Özelliğin minimum değeri 1'dir. Maksimum değer Normal stilinin sayfa yüksekliğine ve yazı tipi boyutuna bağlıdır. Minimum satır aralığı yazı tipi boyutunun %136'sıdır. Örneğin, bir inçlik kenar boşluklarına sahip bir Mektup sayfasının sayfa başına maksimum satır sayısı 39'dur.

Varsayılan olarak, özelliğin, satır aralığının Normal stilinin yazı tipi boyutundan 1,5 kat daha büyük olduğu bir değeri vardır.

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

* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
