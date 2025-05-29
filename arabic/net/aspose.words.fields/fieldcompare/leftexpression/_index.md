---
title: FieldCompare.LeftExpression
linktitle: LeftExpression
articleTitle: LeftExpression
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FieldCompare LeftExpression، ويمكنك الوصول بسهولة إلى الجانب الأيسر من تعبيرات المقارنة أو تعديله لتحسين تحليل البيانات.
type: docs
weight: 30
url: /ar/net/aspose.words.fields/fieldcompare/leftexpression/
---
## FieldCompare.LeftExpression property

يحصل على الجزء الأيسر من تعبير المقارنة أو يعينه.

```csharp
public string LeftExpression { get; set; }
```

## أمثلة

يوضح كيفية مقارنة التعبيرات باستخدام حقل COMPARE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldCompare field = (FieldCompare)builder.InsertField(FieldType.FieldCompare, true);
field.LeftExpression = "3";
field.ComparisonOperator = "<";
field.RightExpression = "2";
field.Update();

// يعرض حقل المقارنة "0" أو "1"، اعتمادًا على صحة بيانه.
//نتيجة هذه العبارة خاطئة، لذا سيعرض هذا الحقل "0".
Assert.AreEqual(" COMPARE  3 < 2", field.GetFieldCode());
Assert.AreEqual("0", field.Result);

builder.Writeln();

field = (FieldCompare)builder.InsertField(FieldType.FieldCompare, true);
field.LeftExpression = "5";
field.ComparisonOperator = "=";
field.RightExpression = "2 + 3";
field.Update();

// يعرض هذا الحقل الرقم "1" لأن العبارة صحيحة.
Assert.AreEqual(" COMPARE  5 = \"2 + 3\"", field.GetFieldCode());
Assert.AreEqual("1", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.COMPARE.docx");
```

### أنظر أيضا

* class [FieldCompare](../)
* مساحة الاسم [Aspose.Words.Fields](../../../aspose.words.fields/)
* المجسم [Aspose.Words](../../../)
