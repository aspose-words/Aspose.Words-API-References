---
title: ParagraphFormat.LineSpacing
second_title: Aspose.Words لمراجع .NET API
description: ParagraphFormat ملكية. الحصول على أو تعيين تباعد الأسطر بالنقاط للفقرة.
type: docs
weight: 190
url: /ar/net/aspose.words/paragraphformat/linespacing/
---
## ParagraphFormat.LineSpacing property

الحصول على أو تعيين تباعد الأسطر (بالنقاط) للفقرة.

```csharp
public double LineSpacing { get; set; }
```

### ملاحظات

متى[`LineSpacingRule`](../linespacingrule/) تم تعيين الخاصية علىAtLeast ، يمكن أن يكون تباعد الأسطر أكبر من أو يساوي ‎ ولكن لا يقل أبدًا عن المحدد`LineSpacing` قيمة.

متى[`LineSpacingRule`](../linespacingrule/) تم تعيين الخاصية علىExactly ، لا يتغير تباعد الأسطر أبدًا من المحدد`LineSpacing` القيمة، حتى إذا تم استخدام خط أكبر داخل الفقرة.

### أمثلة

يوضح كيفية العمل مع تباعد الأسطر.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي ثلاث قواعد لتباعد الأسطر يمكننا تحديدها باستخدام ملف
// خاصية "LineSpacingRule" الخاصة بالفقرة لتكوين التباعد بين الفقرات.
// 1 - قم بتعيين الحد الأدنى للتباعد.
// سيعطي هذا حشوة رأسية لأسطر النص من أي حجم
// صغير جدًا بحيث لا يحافظ على الحد الأدنى لارتفاع الخط.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.AtLeast;
builder.ParagraphFormat.LineSpacing = 20;

builder.Writeln("Minimum line spacing of 20.");
builder.Writeln("Minimum line spacing of 20.");

// 2 - ضبط التباعد الدقيق.
// سيؤدي استخدام أحجام الخطوط الكبيرة جدًا بالنسبة للتباعد إلى اقتطاع النص.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Exactly;
builder.ParagraphFormat.LineSpacing = 5;

builder.Writeln("Line spacing of exactly 5.");
builder.Writeln("Line spacing of exactly 5.");

// 3 - قم بتعيين التباعد كمضاعف لتباعد الأسطر الافتراضي، وهو 12 نقطة افتراضيًا.
// هذا النوع من التباعد سوف يتناسب مع أحجام الخطوط المختلفة.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Multiple;
builder.ParagraphFormat.LineSpacing = 18;

builder.Writeln("Line spacing of 1.5 default lines.");
builder.Writeln("Line spacing of 1.5 default lines.");

doc.Save(ArtifactsDir + "ParagraphFormat.LineSpacing.docx");
```

### أنظر أيضا

* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../paragraphformat/)
* المجسم [Aspose.Words](../../../)


