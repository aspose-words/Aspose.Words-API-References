---
title: FindReplaceOptions.IgnoreShapes
linktitle: IgnoreShapes
articleTitle: IgnoreShapes
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية تجاهل الأشكال في FindReplaceOptions. تحكّم في تضمين الأشكال في معالجة النصوص باستخدام هذا الإعداد المنطقي الأساسي لتحسين الدقة.
type: docs
weight: 110
url: /ar/net/aspose.words.replacing/findreplaceoptions/ignoreshapes/
---
## FindReplaceOptions.IgnoreShapes property

يحصل على قيمة منطقية أو يعينها للإشارة إلى تجاهل الأشكال داخل النص.

القيمة الافتراضية هي`خطأ شنيع`.

```csharp
public bool IgnoreShapes { get; set; }
```

## أمثلة

يوضح كيفية تجاهل الأشكال أثناء استبدال النص.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertShape(ShapeType.Balloon, 200, 200);
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

FindReplaceOptions findReplaceOptions = new FindReplaceOptions() { IgnoreShapes = true };
builder.Document.Range.Replace("Lorem ipsum dolor sit amet, consectetur adipiscing elit.Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
    "Lorem ipsum dolor sit amet, consectetur adipiscing elit.", findReplaceOptions);
Assert.AreEqual("Lorem ipsum dolor sit amet, consectetur adipiscing elit.", builder.Document.GetText().Trim());
```

### أنظر أيضا

* class [FindReplaceOptions](../)
* مساحة الاسم [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* المجسم [Aspose.Words](../../../)
