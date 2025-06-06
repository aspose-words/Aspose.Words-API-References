---
title: FieldIf.EvaluateCondition
linktitle: EvaluateCondition
articleTitle: EvaluateCondition
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تقوم طريقة FieldIf EvaluateCondition بتقييم الظروف بكفاءة، مما يعزز أداء الكود الخاص بك وموثوقيته.
type: docs
weight: 70
url: /ar/net/aspose.words.fields/fieldif/evaluatecondition/
---
## FieldIf.EvaluateCondition method

يقيم الشرط.

```csharp
public FieldIfComparisonResult EvaluateCondition()
```

### قيمة الإرجاع

أ[`FieldIfComparisonResult`](../../fieldifcomparisonresult/) القيمة التي تمثل نتيجة تقييم الشرط.

## أمثلة

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
// أو خاصية "FalseText" الخاصة بها، اعتمادًا على صحة العبارة التي أنشأناها.
field.TrueText = "True";
field.FalseText = "False";
field.Update();

// في هذه الحالة، "0 = 1" غير صحيحة، وبالتالي فإن النتيجة المعروضة ستكون "False".
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

// هذه المرة العبارة صحيحة، لذا فإن النتيجة المعروضة ستكون "صحيح".
Assert.AreEqual(" IF  5 = \"2 + 3\" True False", field.GetFieldCode());
Assert.AreEqual(FieldIfComparisonResult.True, field.EvaluateCondition());
Assert.AreEqual("True", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IF.docx");
```

### أنظر أيضا

* enum [FieldIfComparisonResult](../../fieldifcomparisonresult/)
* class [FieldIf](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
