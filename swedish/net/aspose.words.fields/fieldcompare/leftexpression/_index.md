---
title: FieldCompare.LeftExpression
linktitle: LeftExpression
articleTitle: LeftExpression
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldCompare LeftExpression, få enkel åtkomst till eller modifiera vänster sida av dina jämförelseuttryck för förbättrad dataanalys.
type: docs
weight: 30
url: /sv/net/aspose.words.fields/fieldcompare/leftexpression/
---
## FieldCompare.LeftExpression property

Hämtar eller anger den vänstra delen av jämförelseuttrycket.

```csharp
public string LeftExpression { get; set; }
```

## Exempel

Visar hur man jämför uttryck med hjälp av ett JÄMFÖR-fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldCompare field = (FieldCompare)builder.InsertField(FieldType.FieldCompare, true);
field.LeftExpression = "3";
field.ComparisonOperator = "<";
field.RightExpression = "2";
field.Update();

// JÄMFÖR-fältet visar en "0" eller en "1", beroende på hur sant dess påstående är.
// Resultatet av denna sats är falskt så att detta fält kommer att visa en "0".
Assert.AreEqual(" COMPARE  3 < 2", field.GetFieldCode());
Assert.AreEqual("0", field.Result);

builder.Writeln();

field = (FieldCompare)builder.InsertField(FieldType.FieldCompare, true);
field.LeftExpression = "5";
field.ComparisonOperator = "=";
field.RightExpression = "2 + 3";
field.Update();

// Det här fältet visar en "1" eftersom påståendet är sant.
Assert.AreEqual(" COMPARE  5 = \"2 + 3\"", field.GetFieldCode());
Assert.AreEqual("1", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.COMPARE.docx");
```

### Se även

* class [FieldCompare](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
