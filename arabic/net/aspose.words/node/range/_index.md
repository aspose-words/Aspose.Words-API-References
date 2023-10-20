---
title: Node.Range
linktitle: Range
articleTitle: Range
second_title: Aspose.Words لـ .NET
description: Node Range ملكية. إرجاع أRange الكائن الذي يمثل جزء المستند الموجود في هذه العقدة في C#.
type: docs
weight: 80
url: /ar/net/aspose.words/node/range/
---
## Node.Range property

إرجاع أ[`Range`](../../range/) الكائن الذي يمثل جزء المستند الموجود في هذه العقدة.

```csharp
public Range Range { get; }
```

## أمثلة

يوضح كيفية حذف جميع العقد من النطاق.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أضف نصًا إلى القسم الأول في المستند، ثم أضف قسمًا آخر.
builder.Write("Section 1. ");
builder.InsertBreak(BreakType.SectionBreakContinuous);
builder.Write("Section 2.");

Assert.AreEqual("Section 1. \fSection 2.", doc.GetText().Trim());

// قم بإزالة القسم الأول بالكامل عن طريق إزالة جميع العقد
// ضمن نطاقه، بما في ذلك القسم نفسه.
doc.Sections[0].Range.Delete();

Assert.AreEqual(1, doc.Sections.Count);
Assert.AreEqual("Section 2.", doc.GetText().Trim());
```

### أنظر أيضا

* class [Range](../../range/)
* class [Node](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
