---
title: Section.PrependContent
linktitle: PrependContent
articleTitle: PrependContent
second_title: .NET için Aspose.Words
description: İçeriğinizi Section PrependContent yöntemiyle geliştirin; gelişmiş organizasyon ve netlik için kaynak bölüm metnini başa zahmetsizce ekleyin.
type: docs
weight: 160
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

## Notlar

Sadece içerik[`Body`](../body/) kaynak bölümü kopyalanır, sayfa düzeni, başlıklar ve altbilgiler kopyalanmaz.

Kaynak bölüm farklı bir belgeye aitse düğümler otomatik olarak içe aktarılır.

Hedef belgede yeni bir bölüm oluşturulmuyor.

## Örnekler

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

// Birinci bölümün içeriğini üçüncü bölümün başına ekle.
Section sectionToPrepend = doc.Sections[0];
section.PrependContent(sectionToPrepend);

// İkinci bölümün içeriğini üçüncü bölümün sonuna ekle.
Section sectionToAppend = doc.Sections[1];
section.AppendContent(sectionToAppend);

// "PrependContent" ve "AppendContent" yöntemleri herhangi bir yeni bölüm oluşturmadı.
Assert.AreEqual(3, doc.Sections.Count);
Assert.AreEqual("Section 1" + ControlChar.ParagraphBreak +
                "Section 3" + ControlChar.ParagraphBreak +
                "Section 2" + ControlChar.SectionBreak, section.GetText());
```

### Ayrıca bakınız

* class [Section](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
