---
title: FieldIfComparisonResult Enum
linktitle: FieldIfComparisonResult
articleTitle: FieldIfComparisonResult
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Fields.FieldIfComparisonResult-enumen, som definierar resultaten av IF-fältutvärderingar och förbättrar dina dokumentautomatiseringsfunktioner.
type: docs
weight: 2420
url: /sv/net/aspose.words.fields/fieldifcomparisonresult/
---
## FieldIfComparisonResult enumeration

Anger resultatet av utvärderingen av IF-fältets villkor.

```csharp
public enum FieldIfComparisonResult
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Error | `0` | Det finns ett fel i villkoret. |
| True | `1` | Villkoret är`sann` . |
| False | `2` | Villkoret är`falsk` . |

## Exempel

Visar hur man infogar ett OM-fält.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Statement 1: ");
FieldIf field = (FieldIf)builder.InsertField(FieldType.FieldIf, true);
field.LeftExpression = "0";
field.ComparisonOperator = "=";
field.RightExpression = "1";

// OM-fältet visar en sträng från antingen dess "TrueText"-egenskap,
// eller dess "FalseText"-egenskap, beroende på sanningshalten i det påstående vi har konstruerat.
field.TrueText = "True";
field.FalseText = "False";
field.Update();

// I det här fallet är "0 = 1" felaktigt, så det visade resultatet blir "Falskt".
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

// Den här gången är påståendet korrekt, så det visade resultatet blir "Sant".
Assert.AreEqual(" IF  5 = \"2 + 3\" True False", field.GetFieldCode());
Assert.AreEqual(FieldIfComparisonResult.True, field.EvaluateCondition());
Assert.AreEqual("True", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IF.docx");
```

### Se även

* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)
