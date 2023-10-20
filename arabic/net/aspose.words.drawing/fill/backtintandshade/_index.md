---
title: Fill.BackTintAndShade
linktitle: BackTintAndShade
articleTitle: BackTintAndShade
second_title: Aspose.Words لـ .NET
description: Fill BackTintAndShade ملكية. الحصول على أو تعيين قيمة مزدوجة تؤدي إلى تفتيح أو تغميق لون الخلفية في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.drawing/fill/backtintandshade/
---
## Fill.BackTintAndShade property

الحصول على أو تعيين قيمة مزدوجة تؤدي إلى تفتيح أو تغميق لون الخلفية.

```csharp
public double BackTintAndShade { get; set; }
```

## ملاحظات

القيم المسموح بها تقع ضمن النطاق من -1 (الأغمق) إلى 1 (الأفتح) لهذه الخاصية. الصفر (0) محايد. محاولة تعيين هذه الخاصية إلى قيمة أقل من -1 أو أكثر من 1 تؤدي إلىArgumentOutOfRangeException.

## أمثلة

يوضح كيفية تعيين لون السمة للون شكل المقدمة/الخلفية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.RoundRectangle, 80, 80);

Fill fill = shape.Fill;
fill.ForeThemeColor = ThemeColor.Dark1;
fill.BackThemeColor = ThemeColor.Background2;

// ملاحظة: لا تستخدم "BackThemeColor" و"BackTintAndShade" لملء الخط.
if (fill.BackTintAndShade == 0)
    fill.BackTintAndShade = 0.2;

doc.Save(ArtifactsDir + "Shape.FillThemeColor.docx");
```

### أنظر أيضا

* class [Fill](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
