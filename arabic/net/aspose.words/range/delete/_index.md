---
title: Range.Delete
linktitle: Delete
articleTitle: Delete
second_title: Aspose.Words لـ .NET
description: Range Delete طريقة. حذف كافة أحرف النطاق في C#.
type: docs
weight: 70
url: /ar/net/aspose.words/range/delete/
---
## Range.Delete method

حذف كافة أحرف النطاق.

```csharp
public void Delete()
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

* class [Range](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
