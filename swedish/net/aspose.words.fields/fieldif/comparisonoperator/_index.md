---
title: FieldIf.ComparisonOperator
linktitle: ComparisonOperator
articleTitle: ComparisonOperator
second_title: Aspose.Words för .NET
description: Upptäck egenskapen FieldIf ComparisonOperator och hantera och anpassa enkelt jämförelseoperatorer för förbättrad datahantering och analys.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldif/comparisonoperator/
---
## FieldIf.ComparisonOperator property

Hämtar eller ställer in jämförelseoperatorn.

```csharp
public string ComparisonOperator { get; set; }
```

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

* class [FieldIf](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
