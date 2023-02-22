---
title: Enum FieldIfComparisonResult
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fields.FieldIfComparisonResult Sıralama. EĞER alan koşulu değerlendirmesinin sonucunu belirtir.
type: docs
weight: 1860
url: /tr/net/aspose.words.fields/fieldifcomparisonresult/
---
## FieldIfComparisonResult enumeration

EĞER alan koşulu değerlendirmesinin sonucunu belirtir.

```csharp
public enum FieldIfComparisonResult
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Error | `0` | Koşulda bir hata var. |
| True | `1` | Koşul:`doğru` . |
| False | `2` | Koşul:`yanlış` . |

### Örnekler

EĞER alanının nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Statement 1: ");
FieldIf field = (FieldIf)builder.InsertField(FieldType.FieldIf, true);
field.LeftExpression = "0";
field.ComparisonOperator = "=";
field.RightExpression = "1";

// EĞER alanı, "TrueText" özelliğinden bir dize görüntüler,
// veya oluşturduğumuz ifadenin doğruluğuna bağlı olarak "FalseText" özelliği.
field.TrueText = "True";
field.FalseText = "False";
field.Update();

// Bu durumda "0 = 1" yanlıştır, bu nedenle görüntülenen sonuç "Yanlış" olacaktır.
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

// Bu sefer ifade doğrudur, bu nedenle görüntülenen sonuç "True" olacaktır.
Assert.AreEqual(" IF  5 = \"2 + 3\" True False", field.GetFieldCode());
Assert.AreEqual(FieldIfComparisonResult.True, field.EvaluateCondition());
Assert.AreEqual("True", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IF.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Fields](../../aspose.words.fields/)
* toplantı [Aspose.Words](../../)


