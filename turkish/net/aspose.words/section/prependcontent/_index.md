---
title: Section.PrependContent
second_title: Aspose.Words for .NET API Referansı
description: Section yöntem. Bu bölümün başına kaynak bölümün içeriğinin bir kopyasını ekler.
type: docs
weight: 140
url: /tr/net/aspose.words/section/prependcontent/
---
## Section.PrependContent method

Bu bölümün başına kaynak bölümün içeriğinin bir kopyasını ekler.

```csharp
public void PrependContent(Section sourceSection)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| sourceSection | Section | İçeriğin kopyalanacağı bölüm. |

### Notlar

sadece içeriği[`Body`](../body/) kaynak bölümünün kopyalanması, sayfa düzeni, üstbilgi ve altbilgilerinin kopyalanmaması.

Kaynak bölüm farklı bir belgeye aitse düğümler otomatik olarak içe aktarılır.

Hedef belgede yeni bölüm oluşturulmaz.

### Örnekler

Bir bölümün içeriğinin başka bir bölüme nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 3");

Section section = doc.Sections[2];

Assert.AreEqual("Section 3" + ControlChar.SectionBreak, section.GetText());

// Birinci bölümün içeriğini üçüncü bölümün başına ekleyin.
Section sectionToPrepend = doc.Sections[0];
section.PrependContent(sectionToPrepend);

// İkinci bölümün içeriğini üçüncü bölümün sonuna ekleyin.
Section sectionToAppend = doc.Sections[1];
section.AppendContent(sectionToAppend);

// "PrependContent" ve "AppendContent" yöntemleri yeni bölüm oluşturmadı.
Assert.AreEqual(3, doc.Sections.Count);
Assert.AreEqual("Section 1" + ControlChar.ParagraphBreak +
                "Section 3" + ControlChar.ParagraphBreak +
                "Section 2" + ControlChar.SectionBreak, section.GetText());
```

### Ayrıca bakınız

* class [Section](../)
* ad alanı [Aspose.Words](../../section/)
* toplantı [Aspose.Words](../../../)


