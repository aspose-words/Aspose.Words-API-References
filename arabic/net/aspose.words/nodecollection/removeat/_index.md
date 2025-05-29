---
title: NodeCollection.RemoveAt
linktitle: RemoveAt
articleTitle: RemoveAt
second_title: Aspose.Words لـ .NET
description: أزل العقد من مجموعتك بسهولة باستخدام طريقة NodeCollection RemoveAt. سهّل إدارة المستندات بإزالة عقد محددة بسرعة.
type: docs
weight: 100
url: /ar/net/aspose.words/nodecollection/removeat/
---
## NodeCollection.RemoveAt method

يزيل العقدة الموجودة في الفهرس المحدد من المجموعة ومن المستند.

```csharp
public void RemoveAt(int index)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| index | Int32 | الفهرس المبني على الصفر للعقدة. يُسمح بالمؤشرات السلبية وتشير إلى الوصول من نهاية القائمة. على سبيل المثال -1 يعني العقدة الأخيرة، -2 يعني العقدة الثانية قبل الأخيرة وهكذا. |

## أمثلة

يوضح كيفية إضافة أقسام وإزالتها في مستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.Write("Section 2");

Assert.AreEqual("Section 1\x000cSection 2", doc.GetText().Trim());

//حذف القسم الأول من المستند.
doc.Sections.RemoveAt(0);

Assert.AreEqual("Section 2", doc.GetText().Trim());

// قم بإضافة نسخة من القسم الأول إلى نهاية المستند.
int lastSectionIdx = doc.Sections.Count - 1;
Section newSection = doc.Sections[lastSectionIdx].Clone();
doc.Sections.Add(newSection);

Assert.AreEqual("Section 2\x000cSection 2", doc.GetText().Trim());
```

### أنظر أيضا

* class [NodeCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
