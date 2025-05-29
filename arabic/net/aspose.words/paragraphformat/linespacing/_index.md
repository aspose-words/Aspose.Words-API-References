---
title: ParagraphFormat.LineSpacing
linktitle: LineSpacing
articleTitle: LineSpacing
second_title: Aspose.Words لـ .NET
description: اضبط مسافات أسطر فقراتك بسهولة باستخدام خاصية ParagraphFormat LineSpacing. حسّن سهولة القراءة وأسلوب الكتابة في مستنداتك!
type: docs
weight: 190
url: /ar/net/aspose.words/paragraphformat/linespacing/
---
## ParagraphFormat.LineSpacing property

يحصل على أو يعين المسافة بين الأسطر (بالنقاط) للفقرة.

```csharp
public double LineSpacing { get; set; }
```

## ملاحظات

متى[`LineSpacingRule`](../linespacingrule/) تم تعيين الخاصية إلىAtLeast يمكن أن تكون المسافة بين الأسطر أكبر من أو تساوي، ولكن لا تقل أبدًا عن المسافة المحددة`LineSpacing` قيمة.

متى[`LineSpacingRule`](../linespacingrule/) تم تعيين الخاصية إلىExactly ، لا يتغير تباعد الأسطر أبدًا من x000d_ المحدد`LineSpacing` القيمة، حتى لو تم استخدام خط أكبر داخل الفقرة.

## أمثلة

يوضح كيفية العمل مع تباعد الأسطر.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي ثلاث قواعد لتباعد الأسطر يمكننا تعريفها باستخدام
// خاصية "LineSpacingRule" للفقرة لتكوين المسافة بين الفقرات.
// 1 - تعيين الحد الأدنى من المسافة.
// سيؤدي هذا إلى توفير حشوة رأسية لأسطر النص بأي حجم
//هذا صغير جدًا للحفاظ على الحد الأدنى لارتفاع السطر.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.AtLeast;
builder.ParagraphFormat.LineSpacing = 20;

builder.Writeln("Minimum line spacing of 20.");
builder.Writeln("Minimum line spacing of 20.");

// 2 - تعيين المسافة الدقيقة.
// استخدام أحجام الخطوط التي تكون كبيرة جدًا بالنسبة للتباعد سوف يؤدي إلى اقتطاع النص.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Exactly;
builder.ParagraphFormat.LineSpacing = 5;

builder.Writeln("Line spacing of exactly 5.");
builder.Writeln("Line spacing of exactly 5.");

// 3 - قم بتعيين المسافة كمضاعف للمسافة الافتراضية للأسطر، والتي تكون 12 نقطة بشكل افتراضي.
//هذا النوع من التباعد سوف يتناسب مع أحجام الخطوط المختلفة.
builder.ParagraphFormat.LineSpacingRule = LineSpacingRule.Multiple;
builder.ParagraphFormat.LineSpacing = 18;

builder.Writeln("Line spacing of 1.5 default lines.");
builder.Writeln("Line spacing of 1.5 default lines.");

doc.Save(ArtifactsDir + "ParagraphFormat.LineSpacing.docx");
```

### أنظر أيضا

* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
