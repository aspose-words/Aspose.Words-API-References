---
title: ShapeBase.IsTopLevel
linktitle: IsTopLevel
articleTitle: IsTopLevel
second_title: Aspose.Words لـ .NET
description: اكتشف ShapeBase IsTopLevel. تحقق سريعًا من استقلالية الشكل، مما يُحسّن سير عمل التصميم لديك من خلال إدارة فعالة للمجموعة.
type: docs
weight: 370
url: /ar/net/aspose.words.drawing/shapebase/istoplevel/
---
## ShapeBase.IsTopLevel property

إرجاع`حقيقي` إذا لم يكن هذا الشكل طفلاً لشكل المجموعة.

```csharp
public bool IsTopLevel { get; }
```

## أمثلة

يوضح كيفية معرفة ما إذا كان الشكل جزءًا من مجموعة أشكال.

```csharp
Document doc = new Document();

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
shape.WrapType = WrapType.None;

// بشكل افتراضي، لا يعد الشكل جزءًا من أي شكل مجموعة، وبالتالي يتم تعيين الخاصية "IsTopLevel" على "true".
Assert.True(shape.IsTopLevel);

GroupShape group = new GroupShape(doc);
group.AppendChild(shape);

// بمجرد دمج شكل في شكل المجموعة، تتغير خاصية "IsTopLevel" إلى "false".
Assert.False(shape.IsTopLevel);
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
