---
title: FieldIf.EvaluateCondition
linktitle: EvaluateCondition
articleTitle: EvaluateCondition
second_title: .NET için Aspose.Words
description: FieldIf EvaluateCondition yönteminin koşulları nasıl etkili bir şekilde değerlendirerek kodunuzun performansını ve güvenilirliğini nasıl artırdığını keşfedin.
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

Bir[`FieldIfComparisonResult`](../../fieldifcomparisonresult/) koşul değerlendirmesinin sonucunu temsil eden değer.

## Örnekler

Bir IF alanının nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Statement 1: ");
FieldIf field = (FieldIf)builder.InsertField(FieldType.FieldIf, true);
field.LeftExpression = "0";
field.ComparisonOperator = "=";
field.RightExpression = "1";

// IF alanı, "TrueText" özelliğinden bir dize görüntüler,
// veya oluşturduğumuz ifadenin doğruluğuna bağlı olarak onun "FalseText" özelliği.
field.TrueText = "True";
field.FalseText = "False";
field.Update();

// Bu durumda "0 = 1" yanlıştır, dolayısıyla görüntülenen sonuç "False" olacaktır.
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

// Bu sefer ifade doğru olduğundan görüntülenen sonuç "True" olacaktır.
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
