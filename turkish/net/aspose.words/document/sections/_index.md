---
title: Document.Sections
linktitle: Sections
articleTitle: Sections
second_title: Aspose.Words for .NET
description: Document Sections mülk. Belgedeki tüm bölümleri temsil eden bir koleksiyon döndürür C#'da.
type: docs
weight: 370
url: /tr/net/aspose.words/document/sections/
---
## Document.Sections property

Belgedeki tüm bölümleri temsil eden bir koleksiyon döndürür.

```csharp
public SectionCollection Sections { get; }
```

## Örnekler

Bir belgede bölümlerin nasıl eklenip kaldırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.AreEqual("Section 1\x000cSection 2", doc.GetText().Trim());

// Dokümanın ilk bölümünü silin.
doc.Sections.RemoveAt(0);

Assert.AreEqual("Section 2", doc.GetText().Trim());

// Şimdi ilk bölümün bir kopyasını belgenin sonuna ekleyin.
int lastSectionIdx = doc.Sections.Count - 1;
Section newSection = doc.Sections[lastSectionIdx].Clone();
doc.Sections.Add(newSection);

Assert.AreEqual("Section 2\x000cSection 2", doc.GetText().Trim());
```

Yeni bir bölümün kendisini öncekinden nasıl ayıracağının nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("This text is in section 1.");

// Bölüm sonu türleri, yeni bir bölümün kendisini önceki bölümden nasıl ayıracağını belirler.
// Aşağıda beş tür bölüm sonu verilmiştir.
// 1 - Sonraki bölümü yeni bir sayfada başlatır:
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("This text is in section 2.");

Assert.AreEqual(SectionStart.NewPage, doc.Sections[1].PageSetup.SectionStart);

// 2 - Geçerli sayfada sonraki bölümü başlatır:
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("This text is in section 3.");

Assert.AreEqual(SectionStart.Continuous, doc.Sections[2].PageSetup.SectionStart);

// 3 - Sonraki bölümü yeni çift sayfada başlatır:
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Writeln("This text is in section 4.");

Assert.AreEqual(SectionStart.EvenPage, doc.Sections[3].PageSetup.SectionStart);

// 4 - Sonraki bölümü yeni tek sayı sayfasında başlatır:
builder.InsertBreak(BreakType.SectionBreakOddPage);
builder.Writeln("This text is in section 5.");

Assert.AreEqual(SectionStart.OddPage, doc.Sections[4].PageSetup.SectionStart);

// 5 - Sonraki bölümü yeni bir sütunda başlatır:
TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.SetCount(2);

builder.InsertBreak(BreakType.SectionBreakNewColumn);
builder.Writeln("This text is in section 6.");

Assert.AreEqual(SectionStart.NewColumn, doc.Sections[5].PageSetup.SectionStart);

doc.Save(ArtifactsDir + "PageSetup.SetSectionStart.docx");
```

### Ayrıca bakınız

* class [SectionCollection](../../sectioncollection/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
