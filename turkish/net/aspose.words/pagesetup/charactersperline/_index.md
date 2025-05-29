---
title: PageSetup.CharactersPerLine
linktitle: CharactersPerLine
articleTitle: CharactersPerLine
second_title: .NET için Aspose.Words
description: Belge düzeninizi PageSetup CharactersPerLine özelliğiyle kontrol edin. En iyi okunabilirlik ve tasarım için satır başına karakterleri kolayca ayarlayın.
type: docs
weight: 100
url: /tr/net/aspose.words/pagesetup/charactersperline/
---
## PageSetup.CharactersPerLine property

Belge ızgarasında satır başına karakter sayısını alır veya ayarlar.

```csharp
public int CharactersPerLine { get; set; }
```

## Notlar

Özelliğin minimum değeri 1'dir. Maksimum değer Normal stilinin sayfa genişliğine ve yazı tipi boyutuna bağlıdır. Minimum karakter aralığı yazı tipi boyutunun %90'ıdır. Örneğin, bir inçlik kenar boşluklarına sahip bir Mektup sayfasının satır başına maksimum karakter sayısı 43'tür.

Varsayılan olarak, özelliğin karakter aralığının Normal stilinin yazı boyutuna eşit olduğu bir değeri vardır.

## Örnekler

Her satırın sahip olabileceği karakter sayısının nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Atışı etkinleştirin ve ardından bunu bu bölümdeki satır başına karakter sayısını ayarlamak için kullanın.
builder.PageSetup.LayoutMode = SectionLayoutMode.Grid;
builder.PageSetup.CharactersPerLine = 10;

// Karakter sayısı yazı tipinin boyutuna da bağlıdır.
doc.Styles["Normal"].Font.Size = 20;

Assert.AreEqual(8, doc.FirstSection.PageSetup.CharactersPerLine);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "PageSetup.CharactersPerLine.docx");
```

### Ayrıca bakınız

* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
