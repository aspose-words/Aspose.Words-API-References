---
title: PageSetup.CharactersPerLine
linktitle: CharactersPerLine
articleTitle: CharactersPerLine
second_title: Aspose.Words for .NET
description: PageSetup CharactersPerLine mülk. Belge kılavuzundaki satır başına karakter sayısını alır veya ayarlar C#'da.
type: docs
weight: 100
url: /tr/net/aspose.words/pagesetup/charactersperline/
---
## PageSetup.CharactersPerLine property

Belge kılavuzundaki satır başına karakter sayısını alır veya ayarlar.

```csharp
public int CharactersPerLine { get; set; }
```

## Notlar

Özelliğin minimum değeri 1'dir. Maksimum değer, Normal stilinin sayfa genişliğine ve yazı tipi boyutuna bağlıdır. Minimum karakter aralığı yazı tipi boyutunun yüzde 90'ıdır. Örneğin, bir inç kenar boşluklarına sahip bir Letter sayfasının satırı başına maksimum karakter sayısı 43'tür.

Varsayılan olarak özellik, karakter aralığının Normal stilinin yazı tipi boyutuna eşit olduğu bir değere sahiptir.

## Örnekler

Her satırın sahip olabileceği karakter sayısı için nasıl belirtileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Perdelemeyi etkinleştirin ve ardından bu bölümde satır başına karakter sayısını ayarlamak için bunu kullanın.
builder.PageSetup.LayoutMode = SectionLayoutMode.Grid;
builder.PageSetup.CharactersPerLine = 10;

// Karakter sayısı aynı zamanda yazı tipinin boyutuna da bağlıdır.
doc.Styles["Normal"].Font.Size = 20;

Assert.AreEqual(8, doc.FirstSection.PageSetup.CharactersPerLine);

builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "PageSetup.CharactersPerLine.docx");
```

### Ayrıca bakınız

* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
