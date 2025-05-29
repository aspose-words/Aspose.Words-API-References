---
title: Font.LineSpacing
linktitle: LineSpacing
articleTitle: LineSpacing
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Font LineSpacing، التي توفر مسافة دقيقة بين السطور بالنقاط، مما يعزز قابلية قراءة النص وتصميمه.
type: docs
weight: 190
url: /ar/net/aspose.words/font/linespacing/
---
## Font.LineSpacing property

إرجاع المسافة بين أسطر هذا الخط (بالنقاط).

```csharp
public double LineSpacing { get; }
```

## أمثلة

يوضح كيفية الحصول على المسافة بين أسطر الخط، بالنقاط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تعيين خطوط مختلفة لـ DocumentBuilder والتحقق من تباعد السطور الخاصة بها.
builder.Font.Name = "Calibri";
Assert.AreEqual(14.6484375d, builder.Font.LineSpacing);

builder.Font.Name = "Times New Roman";
Assert.AreEqual(13.798828125d, builder.Font.LineSpacing);
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
