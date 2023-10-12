---
title: ParagraphFormat.LineSpacingRule
second_title: Aspose.Words لمراجع .NET API
description: ParagraphFormat ملكية. الحصول على أو تعيين تباعد الأسطر للفقرة.
type: docs
weight: 200
url: /ar/net/aspose.words/paragraphformat/linespacingrule/
---
## ParagraphFormat.LineSpacingRule property

الحصول على أو تعيين تباعد الأسطر للفقرة.

```csharp
public LineSpacingRule LineSpacingRule { get; set; }
```

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

* enum [LineSpacingRule](../../linespacingrule/)
* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../paragraphformat/)
* المجسم [Aspose.Words](../../../)


