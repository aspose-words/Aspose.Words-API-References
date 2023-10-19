---
title: Range.Delete
linktitle: Delete
articleTitle: Delete
second_title: Aspose.Words for .NET
description: Range Delete yöntem. Aralığın tüm karakterlerini siler C#'da.
type: docs
weight: 70
url: /tr/net/aspose.words/range/delete/
---
## Range.Delete method

Aralığın tüm karakterlerini siler.

```csharp
public void Delete()
```

## Örnekler

Bir aralıktaki tüm düğümlerin nasıl silineceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgedeki ilk bölüme metin ekleyin ve ardından başka bir bölüm ekleyin.
builder.Write("Section 1. ");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Write("Section 2.");

Assert.AreEqual("Section 1. \fSection 2.", doc.GetText().Trim());

// Tüm düğümleri kaldırarak ilk bölümü tamamen kaldırın
// bölümün kendisi de dahil olmak üzere kendi aralığı içinde.
doc.Sections[0].Range.Delete();

Assert.AreEqual(1, doc.Sections.Count);
Assert.AreEqual("Section 2.", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [Range](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
