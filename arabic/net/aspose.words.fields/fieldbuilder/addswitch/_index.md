---
title: FieldBuilder.AddSwitch
linktitle: AddSwitch
articleTitle: AddSwitch
second_title: Aspose.Words لـ .NET
description: FieldBuilder AddSwitch طريقة. إضافة مفتاح الحقل في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldbuilder/addswitch/
---
## AddSwitch(*string*) {#addswitch}

إضافة مفتاح الحقل.

```csharp
public FieldBuilder AddSwitch(string switchName)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| switchName | String | اسم التبديل. |

## ملاحظات

يضيف هذا التحميل الزائد علامة (مفتاح بدون وسيطة).

## أمثلة

يوضح كيفية إنشاء الحقول باستخدام منشئ الحقول، ثم إدراجها في المستند.

```csharp
Document doc = new Document();

// فيما يلي ثلاثة أمثلة للبناء الميداني الذي تم إجراؤه باستخدام أداة إنشاء الحقول.
// 1 - حقل واحد:
// استخدم منشئ الحقول لإضافة حقل SYMBOL الذي يعرض الرمز ƒ (Florin).
FieldBuilder builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(402);
builder.AddSwitch("\\f", "Arial");
builder.AddSwitch("\\s", 25);
builder.AddSwitch("\\u");
Field field = builder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph);

Assert.AreEqual(" SYMBOL 402 \\f Arial \\s 25 \\u ", field.GetFieldCode());

// 2 - حقل متداخل:
// استخدم منشئ الحقول لإنشاء حقل صيغة يستخدمه منشئ حقل آخر كحقل داخلي.
FieldBuilder innerFormulaBuilder = new FieldBuilder(FieldType.FieldFormula);
innerFormulaBuilder.AddArgument(100);
innerFormulaBuilder.AddArgument("+");
innerFormulaBuilder.AddArgument(74);

// أنشئ منشئًا آخر لحقل SYMBOL آخر، وأدخل حقل الصيغة
 // الذي أنشأناه أعلاه في حقل SYMBOL كوسيطة له.
builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(innerFormulaBuilder);
field = builder.BuildAndInsert(doc.FirstSection.Body.AppendParagraph(string.Empty));

// سيستخدم حقل SYMBOL الخارجي نتيجة حقل الصيغة، 174، كوسيطة له،
// مما سيجعل الحقل يعرض رمز ® (العلامة المسجلة) حيث أن رقم الحرف الخاص به هو 174.
Assert.AreEqual(" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field.GetFieldCode());

// 3 - حقول ووسائط متداخلة متعددة:
// الآن، سوف نستخدم منشئًا لإنشاء حقل IF، والذي يعرض إحدى قيمتي السلسلة المخصصة،
// اعتمادًا على قيمة الصواب/الخطأ للتعبير الخاص بها. للحصول على قيمة صحيحة/خطأ
// الذي يحدد السلسلة التي يعرضها حقل IF، سيختبر حقل IF تعبيرين رقميين للمساواة.
// سنوفر التعبيرين في شكل حقول صيغة، والتي سنضعها داخل حقل IF.
FieldBuilder leftExpression = new FieldBuilder(FieldType.FieldFormula);
leftExpression.AddArgument(2);
leftExpression.AddArgument("+");
leftExpression.AddArgument(3);

FieldBuilder rightExpression = new FieldBuilder(FieldType.FieldFormula);
rightExpression.AddArgument(2.5);
rightExpression.AddArgument("*");
rightExpression.AddArgument(5.2);

// بعد ذلك، سنقوم ببناء وسيطتين للحقل، والتي ستكون بمثابة سلاسل إخراج صحيحة/خطأ لحقل IF.
// ستعيد هذه الوسيطات استخدام قيم الإخراج لتعبيراتنا الرقمية.
FieldArgumentBuilder trueOutput = new FieldArgumentBuilder();
trueOutput.AddText("True, both expressions amount to ");
trueOutput.AddField(leftExpression);

FieldArgumentBuilder falseOutput = new FieldArgumentBuilder();
falseOutput.AddNode(new Run(doc, "False, "));
falseOutput.AddField(leftExpression);
falseOutput.AddNode(new Run(doc, " does not equal "));
falseOutput.AddField(rightExpression);

 // وأخيرًا، سنقوم بإنشاء منشئ حقل آخر لحقل IF ودمج كل التعبيرات.
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

* class [FieldBuilder](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)

---

## AddSwitch(*string, string*) {#addswitch_3}

إضافة مفتاح الحقل.

```csharp
public FieldBuilder AddSwitch(string switchName, string switchArgument)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| switchName | String | اسم التبديل. |
| switchArgument | String | قيمة التبديل. |

## أمثلة

يوضح كيفية إنشاء الحقول باستخدام منشئ الحقول، ثم إدراجها في المستند.

```csharp
Document doc = new Document();

// فيما يلي ثلاثة أمثلة للبناء الميداني الذي تم إجراؤه باستخدام أداة إنشاء الحقول.
// 1 - حقل واحد:
// استخدم منشئ الحقول لإضافة حقل SYMBOL الذي يعرض الرمز ƒ (Florin).
FieldBuilder builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(402);
builder.AddSwitch("\\f", "Arial");
builder.AddSwitch("\\s", 25);
builder.AddSwitch("\\u");
Field field = builder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph);

Assert.AreEqual(" SYMBOL 402 \\f Arial \\s 25 \\u ", field.GetFieldCode());

// 2 - حقل متداخل:
// استخدم منشئ الحقول لإنشاء حقل صيغة يستخدمه منشئ حقل آخر كحقل داخلي.
FieldBuilder innerFormulaBuilder = new FieldBuilder(FieldType.FieldFormula);
innerFormulaBuilder.AddArgument(100);
innerFormulaBuilder.AddArgument("+");
innerFormulaBuilder.AddArgument(74);

// أنشئ منشئًا آخر لحقل SYMBOL آخر، وأدخل حقل الصيغة
 // الذي أنشأناه أعلاه في حقل SYMBOL كوسيطة له.
builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(innerFormulaBuilder);
field = builder.BuildAndInsert(doc.FirstSection.Body.AppendParagraph(string.Empty));

// سيستخدم حقل SYMBOL الخارجي نتيجة حقل الصيغة، 174، كوسيطة له،
// مما سيجعل الحقل يعرض رمز ® (العلامة المسجلة) حيث أن رقم الحرف الخاص به هو 174.
Assert.AreEqual(" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field.GetFieldCode());

// 3 - حقول ووسائط متداخلة متعددة:
// الآن، سوف نستخدم منشئًا لإنشاء حقل IF، والذي يعرض إحدى قيمتي السلسلة المخصصة،
// اعتمادًا على قيمة الصواب/الخطأ للتعبير الخاص بها. للحصول على قيمة صحيحة/خطأ
// الذي يحدد السلسلة التي يعرضها حقل IF، سيختبر حقل IF تعبيرين رقميين للمساواة.
// سنوفر التعبيرين في شكل حقول صيغة، والتي سنضعها داخل حقل IF.
FieldBuilder leftExpression = new FieldBuilder(FieldType.FieldFormula);
leftExpression.AddArgument(2);
leftExpression.AddArgument("+");
leftExpression.AddArgument(3);

FieldBuilder rightExpression = new FieldBuilder(FieldType.FieldFormula);
rightExpression.AddArgument(2.5);
rightExpression.AddArgument("*");
rightExpression.AddArgument(5.2);

// بعد ذلك، سنقوم ببناء وسيطتين للحقل، والتي ستكون بمثابة سلاسل إخراج صحيحة/خطأ لحقل IF.
// ستعيد هذه الوسيطات استخدام قيم الإخراج لتعبيراتنا الرقمية.
FieldArgumentBuilder trueOutput = new FieldArgumentBuilder();
trueOutput.AddText("True, both expressions amount to ");
trueOutput.AddField(leftExpression);

FieldArgumentBuilder falseOutput = new FieldArgumentBuilder();
falseOutput.AddNode(new Run(doc, "False, "));
falseOutput.AddField(leftExpression);
falseOutput.AddNode(new Run(doc, " does not equal "));
falseOutput.AddField(rightExpression);

 // وأخيرًا، سنقوم بإنشاء منشئ حقل آخر لحقل IF ودمج كل التعبيرات.
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

* class [FieldBuilder](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)

---

## AddSwitch(*string, int*) {#addswitch_2}

إضافة مفتاح الحقل.

```csharp
public FieldBuilder AddSwitch(string switchName, int switchArgument)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| switchName | String | اسم التبديل. |
| switchArgument | Int32 | قيمة التبديل. |

## أمثلة

يوضح كيفية إنشاء الحقول باستخدام منشئ الحقول، ثم إدراجها في المستند.

```csharp
Document doc = new Document();

// فيما يلي ثلاثة أمثلة للبناء الميداني الذي تم إجراؤه باستخدام أداة إنشاء الحقول.
// 1 - حقل واحد:
// استخدم منشئ الحقول لإضافة حقل SYMBOL الذي يعرض الرمز ƒ (Florin).
FieldBuilder builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(402);
builder.AddSwitch("\\f", "Arial");
builder.AddSwitch("\\s", 25);
builder.AddSwitch("\\u");
Field field = builder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph);

Assert.AreEqual(" SYMBOL 402 \\f Arial \\s 25 \\u ", field.GetFieldCode());

// 2 - حقل متداخل:
// استخدم منشئ الحقول لإنشاء حقل صيغة يستخدمه منشئ حقل آخر كحقل داخلي.
FieldBuilder innerFormulaBuilder = new FieldBuilder(FieldType.FieldFormula);
innerFormulaBuilder.AddArgument(100);
innerFormulaBuilder.AddArgument("+");
innerFormulaBuilder.AddArgument(74);

// أنشئ منشئًا آخر لحقل SYMBOL آخر، وأدخل حقل الصيغة
 // الذي أنشأناه أعلاه في حقل SYMBOL كوسيطة له.
builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(innerFormulaBuilder);
field = builder.BuildAndInsert(doc.FirstSection.Body.AppendParagraph(string.Empty));

// سيستخدم حقل SYMBOL الخارجي نتيجة حقل الصيغة، 174، كوسيطة له،
// مما سيجعل الحقل يعرض رمز ® (العلامة المسجلة) حيث أن رقم الحرف الخاص به هو 174.
Assert.AreEqual(" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field.GetFieldCode());

// 3 - حقول ووسائط متداخلة متعددة:
// الآن، سوف نستخدم منشئًا لإنشاء حقل IF، والذي يعرض إحدى قيمتي السلسلة المخصصة،
// اعتمادًا على قيمة الصواب/الخطأ للتعبير الخاص بها. للحصول على قيمة صحيحة/خطأ
// الذي يحدد السلسلة التي يعرضها حقل IF، سيختبر حقل IF تعبيرين رقميين للمساواة.
// سنوفر التعبيرين في شكل حقول صيغة، والتي سنضعها داخل حقل IF.
FieldBuilder leftExpression = new FieldBuilder(FieldType.FieldFormula);
leftExpression.AddArgument(2);
leftExpression.AddArgument("+");
leftExpression.AddArgument(3);

FieldBuilder rightExpression = new FieldBuilder(FieldType.FieldFormula);
rightExpression.AddArgument(2.5);
rightExpression.AddArgument("*");
rightExpression.AddArgument(5.2);

// بعد ذلك، سنقوم ببناء وسيطتين للحقل، والتي ستكون بمثابة سلاسل إخراج صحيحة/خطأ لحقل IF.
// ستعيد هذه الوسيطات استخدام قيم الإخراج لتعبيراتنا الرقمية.
FieldArgumentBuilder trueOutput = new FieldArgumentBuilder();
trueOutput.AddText("True, both expressions amount to ");
trueOutput.AddField(leftExpression);

FieldArgumentBuilder falseOutput = new FieldArgumentBuilder();
falseOutput.AddNode(new Run(doc, "False, "));
falseOutput.AddField(leftExpression);
falseOutput.AddNode(new Run(doc, " does not equal "));
falseOutput.AddField(rightExpression);

 // وأخيرًا، سنقوم بإنشاء منشئ حقل آخر لحقل IF ودمج كل التعبيرات.
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

* class [FieldBuilder](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)

---

## AddSwitch(*string, double*) {#addswitch_1}

إضافة مفتاح الحقل.

```csharp
public FieldBuilder AddSwitch(string switchName, double switchArgument)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| switchName | String | اسم التبديل. |
| switchArgument | Double | قيمة التبديل. |

## أمثلة

يوضح كيفية إنشاء الحقول باستخدام منشئ الحقول، ثم إدراجها في المستند.

```csharp
Document doc = new Document();

// فيما يلي ثلاثة أمثلة للبناء الميداني الذي تم إجراؤه باستخدام أداة إنشاء الحقول.
// 1 - حقل واحد:
// استخدم منشئ الحقول لإضافة حقل SYMBOL الذي يعرض الرمز ƒ (Florin).
FieldBuilder builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(402);
builder.AddSwitch("\\f", "Arial");
builder.AddSwitch("\\s", 25);
builder.AddSwitch("\\u");
Field field = builder.BuildAndInsert(doc.FirstSection.Body.FirstParagraph);

Assert.AreEqual(" SYMBOL 402 \\f Arial \\s 25 \\u ", field.GetFieldCode());

// 2 - حقل متداخل:
// استخدم منشئ الحقول لإنشاء حقل صيغة يستخدمه منشئ حقل آخر كحقل داخلي.
FieldBuilder innerFormulaBuilder = new FieldBuilder(FieldType.FieldFormula);
innerFormulaBuilder.AddArgument(100);
innerFormulaBuilder.AddArgument("+");
innerFormulaBuilder.AddArgument(74);

// أنشئ منشئًا آخر لحقل SYMBOL آخر، وأدخل حقل الصيغة
 // الذي أنشأناه أعلاه في حقل SYMBOL كوسيطة له.
builder = new FieldBuilder(FieldType.FieldSymbol);
builder.AddArgument(innerFormulaBuilder);
field = builder.BuildAndInsert(doc.FirstSection.Body.AppendParagraph(string.Empty));

// سيستخدم حقل SYMBOL الخارجي نتيجة حقل الصيغة، 174، كوسيطة له،
// مما سيجعل الحقل يعرض رمز ® (العلامة المسجلة) حيث أن رقم الحرف الخاص به هو 174.
Assert.AreEqual(" SYMBOL \u0013 = 100 + 74 \u0014\u0015 ", field.GetFieldCode());

// 3 - حقول ووسائط متداخلة متعددة:
// الآن، سوف نستخدم منشئًا لإنشاء حقل IF، والذي يعرض إحدى قيمتي السلسلة المخصصة،
// اعتمادًا على قيمة الصواب/الخطأ للتعبير الخاص بها. للحصول على قيمة صحيحة/خطأ
// الذي يحدد السلسلة التي يعرضها حقل IF، سيختبر حقل IF تعبيرين رقميين للمساواة.
// سنوفر التعبيرين في شكل حقول صيغة، والتي سنضعها داخل حقل IF.
FieldBuilder leftExpression = new FieldBuilder(FieldType.FieldFormula);
leftExpression.AddArgument(2);
leftExpression.AddArgument("+");
leftExpression.AddArgument(3);

FieldBuilder rightExpression = new FieldBuilder(FieldType.FieldFormula);
rightExpression.AddArgument(2.5);
rightExpression.AddArgument("*");
rightExpression.AddArgument(5.2);

// بعد ذلك، سنقوم ببناء وسيطتين للحقل، والتي ستكون بمثابة سلاسل إخراج صحيحة/خطأ لحقل IF.
// ستعيد هذه الوسيطات استخدام قيم الإخراج لتعبيراتنا الرقمية.
FieldArgumentBuilder trueOutput = new FieldArgumentBuilder();
trueOutput.AddText("True, both expressions amount to ");
trueOutput.AddField(leftExpression);

FieldArgumentBuilder falseOutput = new FieldArgumentBuilder();
falseOutput.AddNode(new Run(doc, "False, "));
falseOutput.AddField(leftExpression);
falseOutput.AddNode(new Run(doc, " does not equal "));
falseOutput.AddField(rightExpression);

 // وأخيرًا، سنقوم بإنشاء منشئ حقل آخر لحقل IF ودمج كل التعبيرات.
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

* class [FieldBuilder](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
