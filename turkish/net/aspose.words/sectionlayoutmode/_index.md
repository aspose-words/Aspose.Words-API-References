---
title: SectionLayoutMode Enum
linktitle: SectionLayoutMode
articleTitle: SectionLayoutMode
second_title: Aspose.Words for .NET
description: Aspose.Words.SectionLayoutMode Sıralama. Belge ızgara davranışını tanımlamaya olanak tanıyan bir bölüm için düzen modunu belirtir C#'da.
type: docs
weight: 5750
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
| Grid | `1` | Sayfa başına satır ve satır başına karakter sayısını korumak için ilgili bölümün her satıra ve karaktere hem ek satır aralığı hem de karakter aralığı eklendiğini belirtir. Karakterler, kılavuz çizgileriyle otomatik olarak hizalanmayacaktır. yazarak. |
| LineGrid | `2` | Sayfa başına belirtilen satır sayısını korumak için ilgili bölümün it içindeki her satıra ilave satır aralığı ekleneceği belirtir. |
| SnapToChars | `3` | Sayfa başına belirli sayıda satır ve satır başına karakter sayısını korumak için ilgili bölümün her satıra ve içindeki karaktere ek satır aralığına ve karakter aralığına sahip olacağını belirtir. Karakterler, yazarken otomatik olarak kılavuz çizgileriyle hizalanacaktır. |

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

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
