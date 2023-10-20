---
title: FieldCompare.ComparisonOperator
linktitle: ComparisonOperator
articleTitle: ComparisonOperator
second_title: Aspose.Words لـ .NET
description: FieldCompare ComparisonOperator ملكية. الحصول على عامل المقارنة أو تعيينه في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.fields/fieldcompare/comparisonoperator/
---
## FieldCompare.ComparisonOperator property

الحصول على عامل المقارنة أو تعيينه.

```csharp
public string ComparisonOperator { get; set; }
```

## أمثلة

يوضح كيفية مقارنة التعبيرات باستخدام حقل المقارنة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldCompare field = (FieldCompare)builder.InsertField(FieldType.FieldCompare, true);
field.LeftExpression = "3";
field.ComparisonOperator = "<";
field.RightExpression = "2";
field.Update();

// يعرض حقل المقارنة "0" أو "1"، اعتمادًا على حقيقة العبارة الخاصة به.
// نتيجة هذه العبارة خاطئة، لذا سيعرض هذا الحقل "0".
Assert.AreEqual(" COMPARE  3 < 2", field.GetFieldCode());
Assert.AreEqual("0", field.Result);

builder.Writeln();

field = (FieldCompare)builder.InsertField(FieldType.FieldCompare, true);
field.LeftExpression = "5";
field.ComparisonOperator = "=";
field.RightExpression = "2 + 3";
field.Update();

// يعرض هذا الحقل "1" نظرًا لأن العبارة صحيحة.
Assert.AreEqual(" COMPARE  5 = \"2 + 3\"", field.GetFieldCode());
Assert.AreEqual("1", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.COMPARE.docx");
```

### أنظر أيضا

* class [FieldCompare](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
