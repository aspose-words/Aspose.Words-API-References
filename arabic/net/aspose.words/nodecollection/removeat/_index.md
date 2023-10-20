---
title: NodeCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words لـ .NET
description: NodeCollection RemoveAt طريقة. إزالة العقدة الموجودة في الفهرس المحدد من المجموعة ومن المستند في C#.
type: docs
weight: 100
url: /ar/net/aspose.words/nodecollection/removeat/
---
## NodeCollection.RemoveAt method

إزالة العقدة الموجودة في الفهرس المحدد من المجموعة ومن المستند.

```csharp
public void RemoveAt(int index)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| index | Int32 | الفهرس الصفري للعقدة. الفهارس السالبة مسموح بها وتشير إلى الوصول من الجزء الخلفي من القائمة. على سبيل المثال -1 يعني العقدة الأخيرة، -2 يعني الثانية قبل الأخيرة وهكذا. |

## أمثلة

يوضح كيفية إضافة وإزالة الأقسام في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.AreEqual("Section 1\x000cSection 2", doc.GetText().Trim());

// احذف القسم الأول من المستند.
doc.Sections.RemoveAt(0);

Assert.AreEqual("Section 2", doc.GetText().Trim());

// إلحاق نسخة مما هو الآن القسم الأول بنهاية المستند.
int lastSectionIdx = doc.Sections.Count - 1;
Section newSection = doc.Sections[lastSectionIdx].Clone();
doc.Sections.Add(newSection);

Assert.AreEqual("Section 2\x000cSection 2", doc.GetText().Trim());
```

### أنظر أيضا

* class [NodeCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
