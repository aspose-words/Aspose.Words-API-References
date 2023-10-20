---
title: ShapeBase.IsTopLevel
linktitle: IsTopLevel
articleTitle: IsTopLevel
second_title: Aspose.Words لـ .NET
description: ShapeBase IsTopLevel ملكية. إرجاعحقيقيإذا لم يكن هذا الشكل تابعًا لشكل المجموعة في C#.
type: docs
weight: 350
url: /ar/net/aspose.words.drawing/shapebase/istoplevel/
---
## ShapeBase.IsTopLevel property

إرجاع`حقيقي`إذا لم يكن هذا الشكل تابعًا لشكل المجموعة.

```csharp
public bool IsTopLevel { get; }
```

## أمثلة

يوضح كيفية معرفة ما إذا كان الشكل جزءًا من شكل مجموعة.

```csharp
Document doc = new Document();

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
shape.WrapType = WrapType.None;

// الشكل بشكل افتراضي ليس جزءًا من أي شكل مجموعة، وبالتالي تم تعيين الخاصية "IsTopLevel" على "true".
Assert.True(shape.IsTopLevel);

GroupShape group = new GroupShape(doc);
group.AppendChild(shape);

// بمجرد دمج شكل في شكل مجموعة، تتغير الخاصية "IsTopLevel" إلى "خطأ".
Assert.False(shape.IsTopLevel);
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
