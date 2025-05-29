---
title: FieldCompare.ComparisonOperator
linktitle: ComparisonOperator
articleTitle: ComparisonOperator
second_title: .NET için Aspose.Words
description: FieldCompare ComparisonOperator özelliğini keşfedin; gelişmiş veri analizi ve verimlilik için karşılaştırma operatörlerinizi kolayca yönetin.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/fieldcompare/comparisonoperator/
---
## FieldCompare.ComparisonOperator property

Karşılaştırma operatörünü alır veya ayarlar.

```csharp
public string ComparisonOperator { get; set; }
```

## Örnekler

COMPARE alanını kullanarak ifadelerin nasıl karşılaştırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldCompare field = (FieldCompare)builder.InsertField(FieldType.FieldCompare, true);
field.LeftExpression = "3";
field.ComparisonOperator = "<";
field.RightExpression = "2";
field.Update();

// COMPARE alanı, ifadesinin doğruluğuna bağlı olarak "0" veya "1" görüntüler.
// Bu ifadenin sonucu yanlış olduğundan bu alanda "0" değeri gösterilecektir.
Assert.AreEqual(" COMPARE  3 < 2", field.GetFieldCode());
Assert.AreEqual("0", field.Result);

builder.Writeln();

field = (FieldCompare)builder.InsertField(FieldType.FieldCompare, true);
field.LeftExpression = "5";
field.ComparisonOperator = "=";
field.RightExpression = "2 + 3";
field.Update();

// İfade doğru olduğundan bu alan "1" olarak gösterilir.
Assert.AreEqual(" COMPARE  5 = \"2 + 3\"", field.GetFieldCode());
Assert.AreEqual("1", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.COMPARE.docx");
```

### Ayrıca bakınız

* class [FieldCompare](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
