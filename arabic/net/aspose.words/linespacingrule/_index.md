---
title: LineSpacingRule Enum
linktitle: LineSpacingRule
articleTitle: LineSpacingRule
second_title: Aspose.Words لـ .NET
description: اكتشف قاعدة بيانات Aspose.Words.LineSpacingRule لتخصيص مسافات أسطر الفقرات. حسّن تنسيق المستندات بتحكم دقيق وسهولة قراءة مُحسّنة.
type: docs
weight: 3890
url: /ar/net/aspose.words/linespacingrule/
---
## LineSpacingRule enumeration

يحدد قيم المسافة بين الأسطر للفقرة.

```csharp
public enum LineSpacingRule
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| AtLeast | `0` | يمكن أن تكون المسافة بين الأسطر أكبر من أو تساوي، ولكن لا تقل أبدًا عن، القيمة المحددة في[`LineSpacing`](../paragraphformat/linespacing/) الملكية. |
| Exactly | `1` | لا يتغير تباعد الأسطر أبدًا عن القيمة المحددة في [`LineSpacing`](../paragraphformat/linespacing/) الخاصية، حتى إذا تم استخدام خط أكبر داخل الفقرة. |
| Multiple | `2` | يتم تحديد المسافة بين الأسطر في[`LineSpacing`](../paragraphformat/linespacing/) خاصية هي عدد الأسطر. السطر الواحد يساوي ١٢ نقطة. |

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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
