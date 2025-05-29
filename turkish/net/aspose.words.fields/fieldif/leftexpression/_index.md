---
title: FieldIf.LeftExpression
linktitle: LeftExpression
articleTitle: LeftExpression
second_title: .NET için Aspose.Words
description: FieldIf'in LeftExpression özelliğini keşfedin, gelişmiş veri işleme ve analizi için karşılaştırma ifadenizin sol tarafını kolayca yönetin.
type: docs
weight: 40
url: /tr/net/aspose.words.fields/fieldif/leftexpression/
---
## FieldIf.LeftExpression property

Karşılaştırma ifadesinin sol kısmını alır veya ayarlar.

```csharp
public string LeftExpression { get; set; }
```

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

* class [FieldIf](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
