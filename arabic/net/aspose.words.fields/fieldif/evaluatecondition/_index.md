---
title: FieldIf.EvaluateCondition
second_title: Aspose.Words لمراجع .NET API
description: FieldIf طريقة. تقييم الحالة.
type: docs
weight: 70
url: /ar/net/aspose.words.fields/fieldif/evaluatecondition/
---
## FieldIf.EvaluateCondition method

تقييم الحالة.

```csharp
public FieldIfComparisonResult EvaluateCondition()
```

### قيمة الإرجاع

أ[`FieldIfComparisonResult`](../../fieldifcomparisonresult/) القيمة التي تمثل نتيجة تقييم الحالة.

### أمثلة

يوضح كيفية إدراج حقل IF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Statement 1: ");
FieldIf field = (FieldIf)builder.InsertField(FieldType.FieldIf, true);
field.LeftExpression = "0";
field.ComparisonOperator = "=";
field.RightExpression = "1";

// سيعرض حقل IF سلسلة من خاصية "TrueText" الخاصة به،
// أو خاصية "FalseText" الخاصة بها، اعتمادًا على صحة العبارة التي قمنا ببنائها.
field.TrueText = "True";
field.FalseText = "False";
field.Update();

// في هذه الحالة، "0 = 1" غير صحيح، لذا ستكون النتيجة المعروضة "خطأ".
Assert.AreEqual(" IF  0 = 1 True False", field.GetFieldCode());
Assert.AreEqual(FieldIfComparisonResult.False, field.EvaluateCondition());
Assert.AreEqual("False", field.Result);

builder.Write("\nStatement 2: ");
field = (FieldIf)builder.InsertField(FieldType.FieldIf, true);
field.LeftExpression = "5";
field.ComparisonOperator = "=";
field.RightExpression = "2 + 3";
field.TrueText = "True";
field.FalseText = "False";
field.Update();

// هذه المرة العبارة صحيحة، لذا ستكون النتيجة المعروضة "صحيح".
Assert.AreEqual(" IF  5 = \"2 + 3\" True False", field.GetFieldCode());
Assert.AreEqual(FieldIfComparisonResult.True, field.EvaluateCondition());
Assert.AreEqual("True", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IF.docx");
```

### أنظر أيضا

* enum [FieldIfComparisonResult](../../fieldifcomparisonresult/)
* class [FieldIf](../)
* مساحة الاسم [Aspose.Words.Fields](../../fieldif/)
* المجسم [Aspose.Words](../../../)


