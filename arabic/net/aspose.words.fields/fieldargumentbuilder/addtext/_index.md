---
title: FieldArgumentBuilder.AddText
linktitle: AddText
articleTitle: AddText
second_title: Aspose.Words لـ .NET
description: حسّن حججك باستخدام طريقة AddText في FieldArgumentBuilder. أضف نصًا عاديًا بسهولة لتحسين الوضوح والوظائف.
type: docs
weight: 40
url: /ar/net/aspose.words.fields/fieldargumentbuilder/addtext/
---
## FieldArgumentBuilder.AddText method

يضيف نصًا عاديًا إلى الوسيطة.

```csharp
public FieldArgumentBuilder AddText(string text)
```

## أمثلة

يوضح كيفية إنشاء الحقول باستخدام منشئ الحقول، ثم إدراجها في المستند.

```csharp
Document doc = new Document();

// فيما يلي ثلاثة أمثلة لبناء الحقل تم إجراؤها باستخدام منشئ الحقل.
// 1 - حقل واحد:
// استخدم منشئ الحقول لإضافة حقل SYMBOL الذي يعرض الرمز ƒ (فلورين).
FieldBuilder builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(402);
builder.AddSwitch("\\f", "Arial");
builder.AddSwitch("\\s", 25);
builder.AddSwitch("\\u");
Field field = builder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph);

Assert.AreEqual(" SYMBOL 402 \\f Arial \\s 25 \\u ", field.GetFieldCode());

// 2 - الحقل المتداخل:
// استخدم منشئ الحقول لإنشاء حقل صيغة يستخدم كحقل داخلي بواسطة منشئ حقول آخر.
FieldBuilder innerFormulaBuilder = new FieldBuilder(FieldType.FieldFormula);
innerFormulaBuilder.AddArgument(100);
innerFormulaBuilder.AddArgument("+");
innerFormulaBuilder.AddArgument(74);

// قم بإنشاء منشئ آخر لحقل رمز آخر، وأدخل حقل الصيغة
 // الذي قمنا بإنشائه أعلاه في حقل SYMBOL كحجة له.
builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(innerFormulaBuilder);
field = builder.BuildAndInsert(doc.FirstSection.Body.AppendParagraph(string.Empty));

// سيستخدم حقل الرمز الخارجي نتيجة حقل الصيغة، 174، كحجة له،
// مما سيجعل الحقل يعرض رمز ® (العلامة المسجلة) حيث أن رقم حرفه هو 174.
Assert.AreEqual(" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field.GetFieldCode());

// 3 - حقول وحجج متعددة متداخلة:
// الآن، سوف نستخدم منشئًا لإنشاء حقل IF، والذي يعرض إحدى قيمتي السلسلة المخصصة،
// بناءً على قيمة صواب/خطأ في تعبيره. للحصول على قيمة صواب/خطأ
// الذي يحدد السلسلة التي يعرضها حقل IF، وسوف يقوم حقل IF باختبار تعبيرين رقميين للمساواة.
// سوف نقوم بتوفير التعبيرين في شكل حقول الصيغة، والتي سوف نقوم بوضعها داخل حقل IF.
FieldBuilder leftExpression = new FieldBuilder(FieldType.FieldFormula);
leftExpression.AddArgument(2);
leftExpression.AddArgument("+");
leftExpression.AddArgument(3);

FieldBuilder rightExpression = new FieldBuilder(FieldType.FieldFormula);
rightExpression.AddArgument(2.5);
rightExpression.AddArgument("*");
rightExpression.AddArgument(5.2);

// بعد ذلك، سنقوم ببناء وسيطتين للحقل، والتي ستعملان كسلاسل إخراج صحيحة/خاطئة لحقل IF.
// ستعيد هذه الحجج استخدام قيم الإخراج الخاصة بتعبيراتنا الرقمية.
FieldArgumentBuilder trueOutput = new FieldArgumentBuilder();
trueOutput.AddText("True, both expressions amount to ");
trueOutput.AddField(leftExpression);

FieldArgumentBuilder falseOutput = new FieldArgumentBuilder();
falseOutput.AddNode(new Run(doc, "False, "));
falseOutput.AddField(leftExpression);
falseOutput.AddNode(new Run(doc, " does not equal "));
falseOutput.AddField(rightExpression);

 // أخيرًا، سنقوم بإنشاء منشئ حقل آخر لحقل IF ودمج جميع التعبيرات.
builder = new FieldBuilder(FieldType.FieldIf);
builder.AddArgument(leftExpression);
builder.AddArgument("=");
builder.AddArgument(rightExpression);
builder.AddArgument(trueOutput);
builder.AddArgument(falseOutput);
field = builder.BuildAndInsert(doc.FirstSection.Body.AppendParagraph(string.Empty));

Assert.AreEqual(" IF \u0013 = 2 + 3 \u0014\u0015 = \u0013 = 2.5 * 5.2 \u0014\u0015 " +
                "\"True, both expressions amount to \u0013 = 2 + 3 \u0014\u0015\" " +
                "\"False, \u0013 = 2 + 3 \u0014\u0015 does not equal \u0013 = 2.5 * 5.2 \u0014\u0015\" ", field.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SYMBOL.docx");
```

### أنظر أيضا

* class [FieldArgumentBuilder](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
