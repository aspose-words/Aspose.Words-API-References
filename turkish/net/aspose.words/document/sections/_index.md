---
title: Document.Sections
linktitle: Sections
articleTitle: Sections
second_title: .NET için Aspose.Words
description: Tüm belge bölümlerinin eksiksiz koleksiyonuna erişmek, içerik organizasyonunuzu ve gezinmenizi geliştirmek için Belge Bölümleri özelliğini keşfedin.
type: docs
weight: 390
url: /tr/net/aspose.words/document/sections/
---
## Document.Sections property

Belgedeki tüm bölümleri temsil eden bir koleksiyon döndürür.

```csharp
public SectionCollection Sections { get; }
```

## Örnekler

Bir belgeye bölümlerin nasıl ekleneceğini ve kaldırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.AreEqual("Section 1\x000cSection 2", doc.GetText().Trim());

// Belgeden ilk bölümü sil.
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

// Bölüm sonu türleri, yeni bir bölümün önceki bölümden nasıl ayrılacağını belirler.
// Aşağıda beş tür bölüm sonu bulunmaktadır.
// 1 - Bir sonraki bölümü yeni bir sayfada başlatır:
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Writeln("This text is in section 2.");

Assert.AreEqual(SectionStart.NewPage, doc.Sections[1].PageSetup.SectionStart);

// 2 - Mevcut sayfada bir sonraki bölümü başlatır:
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Writeln("This text is in section 3.");

Assert.AreEqual(SectionStart.Continuous, doc.Sections[2].PageSetup.SectionStart);

// 3 - Bir sonraki bölümü yeni bir çift sayfada başlatır:
builder.InsertBreak(BreakType.SectionBreakEvenPage);
builder.Writeln("This text is in section 4.");

Assert.AreEqual(SectionStart.EvenPage, doc.Sections[3].PageSetup.SectionStart);

// 4 - Bir sonraki bölümü yeni bir tek sayfada başlatır:
builder.InsertBreak(BreakType.SectionBreakOddPage);
builder.Writeln("This text is in section 5.");

Assert.AreEqual(SectionStart.OddPage, doc.Sections[4].PageSetup.SectionStart);

// 5 - Bir sonraki bölümü yeni bir sütunda başlatır:
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
