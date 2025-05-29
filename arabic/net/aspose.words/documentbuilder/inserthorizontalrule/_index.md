---
title: DocumentBuilder.InsertHorizontalRule
linktitle: InsertHorizontalRule
articleTitle: InsertHorizontalRule
second_title: Aspose.Words لـ .NET
description: قم بتعزيز مستنداتك باستخدام طريقة InsertHorizontalRule في DocumentBuilder، وقم بإضافة خطوط أفقية أنيقة بسهولة لتحسين التنظيم والجاذبية البصرية.
type: docs
weight: 370
url: /ar/net/aspose.words/documentbuilder/inserthorizontalrule/
---
## DocumentBuilder.InsertHorizontalRule method

يقوم بإدراج شكل مسطرة أفقية في المستند.

```csharp
public Shape InsertHorizontalRule()
```

### قيمة الإرجاع

الشكل الذي يشكل مسطرة أفقية.

## أمثلة

يوضح كيفية إدراج شكل مسطرة أفقية وتخصيص تنسيقها.

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
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
