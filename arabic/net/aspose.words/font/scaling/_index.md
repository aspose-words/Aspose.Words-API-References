---
title: Font.Scaling
second_title: Aspose.Words لمراجع .NET API
description: Font ملكية. الحصول على أو تعيين مقياس عرض الأحرف بالنسبة المئوية.
type: docs
weight: 310
url: /ar/net/aspose.words/font/scaling/
---
## Font.Scaling property

الحصول على أو تعيين مقياس عرض الأحرف بالنسبة المئوية.

```csharp
public int Scaling { get; set; }
```

### أمثلة

يوضح كيفية ضبط القياس الأفقي والتباعد للأحرف.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إضافة نص وزيادة عرض الأحرف إلى 150%.
builder.Font.Scaling = 150;
builder.Writeln("Wide characters");

// أضف نصًا وأضف 1pt من التباعد الأفقي الإضافي بين كل حرف.
builder.Font.Spacing = 1;
builder.Writeln("Expanded by 1pt");

// إضافة نص وتقريب الأحرف من بعضها البعض بمقدار 1pt.
builder.Font.Spacing = -1;
builder.Writeln("Condensed by 1pt");

doc.Save(ArtifactsDir + "Font.ScalingSpacing.docx");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../font/)
* المجسم [Aspose.Words](../../../)


