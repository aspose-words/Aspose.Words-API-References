---
title: FindReplaceOptions.IgnoreShapes
second_title: Aspose.Words لمراجع .NET API
description: FindReplaceOptions ملكية. الحصول على قيمة منطقية أو تعيينها تشير إلى تجاهل الأشكال داخل النص.
type: docs
weight: 110
url: /ar/net/aspose.words.replacing/findreplaceoptions/ignoreshapes/
---
## FindReplaceOptions.IgnoreShapes property

الحصول على قيمة منطقية أو تعيينها تشير إلى تجاهل الأشكال داخل النص.

القيمة الافتراضية هي`خطأ شنيع`.

```csharp
public bool IgnoreShapes { get; set; }
```

### أمثلة

يوضح كيفية تجاهل الأشكال أثناء استبدال النص.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertShape(ShapeType.Balloon, 200, 200);            
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder.Document.Range.Replace("Lorem ipsum dolor sit amet, consectetur adipiscing elit.Lorem ipsum dolor sit amet, consectetur adipiscing elit.",
    "Lorem ipsum dolor sit amet, consectetur adipiscing elit.", new FindReplaceOptions() { IgnoreShapes = true });
Assert.AreEqual("Lorem ipsum dolor sit amet, consectetur adipiscing elit.", builder.Document.GetText().Trim());
```

### أنظر أيضا

* class [FindReplaceOptions](../)
* مساحة الاسم [Aspose.Words.Replacing](../../findreplaceoptions/)
* المجسم [Aspose.Words](../../../)


