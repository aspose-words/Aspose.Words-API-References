---
title: Fill.BackTintAndShade
linktitle: BackTintAndShade
articleTitle: BackTintAndShade
second_title: Aspose.Words لـ .NET
description: قم بضبط خاصية BackTintAndShade لتفتيح أو تعتيم لون الخلفية بسهولة، مما يعزز الجاذبية البصرية لتصميمك وتجربة المستخدم.
type: docs
weight: 30
url: /ar/net/aspose.words.drawing/fill/backtintandshade/
---
## Fill.BackTintAndShade property

يحصل على قيمة مزدوجة لتفتيح أو تعتيم لون الخلفية أو تعيينها.

```csharp
public double BackTintAndShade { get; set; }
```

### استثناءات

| استثناء | حالة |
| --- | --- |
| ArgumentOutOfRangeException | قم بالرمي إذا قمت بتعيين هذه الخاصية إلى قيمة أقل من -1 أو أكثر من 1. |

## ملاحظات

القيم المسموح بها تتراوح من -1 (الأغمق) إلى 1 (الأفتح) لهذه الخاصية.

الصفر (0) محايد.

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
