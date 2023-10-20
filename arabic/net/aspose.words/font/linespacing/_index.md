---
title: Font.LineSpacing
linktitle: LineSpacing
articleTitle: LineSpacing
second_title: Aspose.Words لـ .NET
description: Font LineSpacing ملكية. إرجاع تباعد الأسطر لهذا الخط بالنقاط في C#.
type: docs
weight: 190
url: /ar/net/aspose.words/font/linespacing/
---
## Font.LineSpacing property

إرجاع تباعد الأسطر لهذا الخط (بالنقاط).

```csharp
public double LineSpacing { get; }
```

## أمثلة

يوضح كيفية الحصول على تباعد أسطر الخط بالنقاط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتعيين خطوط مختلفة لـ DocumentBuilder وتحقق من تباعد الأسطر.
builder.Font.Name = "Calibri";
Assert.AreEqual(14.6484375d, builder.Font.LineSpacing);

builder.Font.Name = "Times New Roman";
Assert.AreEqual(13.798828125d, builder.Font.LineSpacing);
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
