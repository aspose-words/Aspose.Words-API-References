---
title: Section.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words لـ .NET
description: انسخ الأقسام بسهولة باستخدام طريقة نسخ الأقسام. بسّط سير عملك وحسّن إنتاجيتك مع هذه الأداة الفعّالة!
type: docs
weight: 130
url: /ar/net/aspose.words/section/clone/
---
## Section.Clone method

ينشئ نسخة مكررة من هذا القسم.

```csharp
public Section Clone()
```

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

* class [Section](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
