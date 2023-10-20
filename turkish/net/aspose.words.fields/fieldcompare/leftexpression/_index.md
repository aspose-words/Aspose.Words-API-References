---
title: FieldCompare.LeftExpression
linktitle: LeftExpression
articleTitle: LeftExpression
second_title: Aspose.Words for .NET
description: FieldCompare LeftExpression mülk. Karşılaştırma ifadesinin sol kısmını alır veya ayarlar C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words.fields/fieldcompare/leftexpression/
---
## FieldCompare.LeftExpression property

Karşılaştırma ifadesinin sol kısmını alır veya ayarlar.

```csharp
public string LeftExpression { get; set; }
```

## Örnekler

KARŞILAŞTIRMA alanı kullanılarak ifadelerin nasıl karşılaştırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldCompare field = (FieldCompare)builder.InsertField(FieldType.FieldCompare, true);
field.LeftExpression = "3";
field.ComparisonOperator = "<";
field.RightExpression = "2";
field.Update();

// KARŞILAŞTIRMA alanı, ifadesinin doğruluğuna bağlı olarak "0" veya "1" değerini görüntüler.
// Bu ifadenin sonucu yanlış olduğundan bu alan "0" değerini gösterecektir.
Assert.AreEqual(" COMPARE  3 < 2", field.GetFieldCode());
Assert.AreEqual("0", field.Result);

builder.Writeln();

field = (FieldCompare)builder.InsertField(FieldType.FieldCompare, true);
field.LeftExpression = "5";
field.ComparisonOperator = "=";
field.RightExpression = "2 + 3";
field.Update();

// İfade doğru olduğundan bu alan "1" değerini gösterir.
Assert.AreEqual(" COMPARE  5 = \"2 + 3\"", field.GetFieldCode());
Assert.AreEqual("1", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.COMPARE.docx");
```

### Ayrıca bakınız

* class [FieldCompare](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
