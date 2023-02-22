---
title: ShapeBase.IsHorizontalRule
second_title: Aspose.Words لمراجع .NET API
description: ShapeBase ملكية. إرجاع صحيح إذا كان هذا الشكل قاعدة أفقية.
type: docs
weight: 260
url: /ar/net/aspose.words.drawing/shapebase/ishorizontalrule/
---
## ShapeBase.IsHorizontalRule property

إرجاع صحيح إذا كان هذا الشكل قاعدة أفقية.

```csharp
public bool IsHorizontalRule { get; }
```

### أمثلة

يوضح كيفية إدراج شكل تسطير أفقي ، وتخصيص تنسيقه.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertHorizontalRule();

HorizontalRuleFormat horizontalRuleFormat = shape.HorizontalRuleFormat;
horizontalRuleFormat.Alignment = HorizontalRuleAlignment.Center;
horizontalRuleFormat.WidthPercent = 70;
horizontalRuleFormat.Height = 3;
horizontalRuleFormat.Color = Color.Blue;
horizontalRuleFormat.NoShade = true;

Assert.True(shape.IsHorizontalRule);
Assert.True(shape.HorizontalRuleFormat.NoShade);
```

### أنظر أيضا

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../shapebase/)
* المجسم [Aspose.Words](../../../)


