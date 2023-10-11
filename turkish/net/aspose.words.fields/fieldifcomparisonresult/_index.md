---
title: Enum FieldIfComparisonResult
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fields.FieldIfComparisonResult Sıralama. IF alanı koşulu değerlendirmesinin sonucunu belirtir.
type: docs
weight: 2010
url: /tr/net/aspose.words.fields/fieldifcomparisonresult/
---
## FieldIfComparisonResult enumeration

IF alanı koşulu değerlendirmesinin sonucunu belirtir.

```csharp
public enum FieldIfComparisonResult
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Error | `0` | Durumda bir hata var. |
| True | `1` | Koşul:`doğru` . |
| False | `2` | Koşul:`YANLIŞ` . |

### Örnekler

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

* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)


