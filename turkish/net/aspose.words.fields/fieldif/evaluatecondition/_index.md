---
title: FieldIf.EvaluateCondition
linktitle: EvaluateCondition
articleTitle: EvaluateCondition
second_title: Aspose.Words for .NET
description: FieldIf EvaluateCondition yöntem. Durumu değerlendirir C#'da.
type: docs
weight: 70
url: /tr/net/aspose.words.fields/fieldif/evaluatecondition/
---
## FieldIf.EvaluateCondition method

Durumu değerlendirir.

```csharp
public FieldIfComparisonResult EvaluateCondition()
```

### Geri dönüş değeri

A[`FieldIfComparisonResult`](../../fieldifcomparisonresult/) durum değerlendirmesinin sonucunu temsil eden değer.

## Örnekler

IF alanının nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Statement 1: ");
FieldIf field = (FieldIf)builder.InsertField(FieldType.FieldIf, true);
field.LeftExpression = "0";
field.ComparisonOperator = "=";
field.RightExpression = "1";

// IF alanı "TrueText" özelliğinden bir dize görüntüleyecektir,
// veya oluşturduğumuz ifadenin doğruluğuna bağlı olarak "FalseText" özelliği.
field.TrueText = "True";
field.FalseText = "False";
field.Update();

// Bu durumda "0 = 1" yanlış olduğundan görüntülenen sonuç "Yanlış" olacaktır.
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

// Bu sefer ifade doğrudur, dolayısıyla görüntülenen sonuç "Doğru" olacaktır.
Assert.AreEqual(" IF  5 = \"2 + 3\" True False", field.GetFieldCode());
Assert.AreEqual(FieldIfComparisonResult.True, field.EvaluateCondition());
Assert.AreEqual("True", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IF.docx");
```

### Ayrıca bakınız

* enum [FieldIfComparisonResult](../../fieldifcomparisonresult/)
* class [FieldIf](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
