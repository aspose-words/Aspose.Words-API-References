---
title: Font.LineSpacing
second_title: Aspose.Words لمراجع .NET API
description: Font ملكية. إرجاع تباعد الأسطر لهذا الخط بالنقاط.
type: docs
weight: 190
url: /ar/net/aspose.words/font/linespacing/
---
## Font.LineSpacing property

إرجاع تباعد الأسطر لهذا الخط (بالنقاط).

```csharp
public double LineSpacing { get; }
```

### أمثلة

يوضح كيفية الحصول على تباعد أسطر الخط بالنقاط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تعيين خطوط مختلفة لـ DocumentBuilder وتحقق من تباعد الأسطر.
builder.Font.Name = "Calibri";
Assert.AreEqual(14.6484375d, builder.Font.LineSpacing);

builder.Font.Name = "Times New Roman";
Assert.AreEqual(13.798828125d, builder.Font.LineSpacing);
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../font/)
* المجسم [Aspose.Words](../../../)


