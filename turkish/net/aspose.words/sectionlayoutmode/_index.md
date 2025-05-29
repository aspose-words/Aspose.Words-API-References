---
title: SectionLayoutMode Enum
linktitle: SectionLayoutMode
articleTitle: SectionLayoutMode
second_title: .NET için Aspose.Words
description: Bölüm düzenlerini optimize etmek ve gelişmiş biçimlendirme denetimi için belge ızgara davranışını geliştirmek üzere Aspose.Words.SectionLayoutMode enum'unu keşfedin.
type: docs
weight: 6580
url: /tr/net/aspose.words/sectionlayoutmode/
---
## SectionLayoutMode enumeration

Belge ızgara davranışını tanımlamaya olanak tanıyan bir bölüm için düzen modunu belirtir.

```csharp
public enum SectionLayoutMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Default | `0` | Belgedeki ilgili bölümün içeriğine hiçbir belge ızgarasının uygulanmayacağını belirtir. |
| Grid | `1` | Her satıra ve içindeki karaktere, sayfa başına belirli sayıda satır ve satır başına belirli sayıda karakter sağlamak için, ilgili bölümün hem ek satır aralığına hem de karakter aralığına eklenmesi gerektiğini belirtir. Karakterler, yazarken kılavuz çizgileriyle otomatik olarak hizalanmayacaktır. |
| LineGrid | `2` | Sayfa başına belirtilen satır sayısını korumak için ilgili bölümün her satırına ek satır aralığının eklenmesi gerektiğini belirtir. |
| SnapToChars | `3` | Her satıra ve içindeki karaktere, sayfa başına belirli sayıda satır ve satır başına belirli sayıda karakter sağlamak için, ilgili bölümün hem ek satır aralığına hem de karakter aralığına eklenmesi gerektiğini belirtir. Karakterler, yazarken kılavuz çizgileriyle otomatik olarak hizalanır. |

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
