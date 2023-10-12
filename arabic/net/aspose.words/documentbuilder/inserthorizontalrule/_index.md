---
title: DocumentBuilder.InsertHorizontalRule
second_title: Aspose.Words لمراجع .NET API
description: DocumentBuilder طريقة. إدراج شكل مسطرة أفقية في المستند.
type: docs
weight: 350
url: /ar/net/aspose.words/documentbuilder/inserthorizontalrule/
---
## DocumentBuilder.InsertHorizontalRule method

إدراج شكل مسطرة أفقية في المستند.

```csharp
public Shape InsertHorizontalRule()
```

### قيمة الإرجاع

الشكل الذي يمثل القاعدة الأفقية.

### أمثلة

يوضح كيفية إدراج شكل قاعدة أفقية، وتخصيص تنسيقه.

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

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* مساحة الاسم [Aspose.Words](../../documentbuilder/)
* المجسم [Aspose.Words](../../../)


