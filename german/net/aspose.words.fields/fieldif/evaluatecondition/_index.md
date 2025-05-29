---
title: FieldIf.EvaluateCondition
linktitle: EvaluateCondition
articleTitle: EvaluateCondition
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Methode „FieldIf EvaluateCondition“ Bedingungen effizient bewertet und so die Leistung und Zuverlässigkeit Ihres Codes verbessert.
type: docs
weight: 70
url: /de/net/aspose.words.fields/fieldif/evaluatecondition/
---
## FieldIf.EvaluateCondition method

Wertet die Bedingung aus.

```csharp
public FieldIfComparisonResult EvaluateCondition()
```

### Rückgabewert

A[`FieldIfComparisonResult`](../../fieldifcomparisonresult/) Wert, der das Ergebnis der Bedingungsauswertung darstellt.

## Beispiele

Zeigt, wie ein IF-Feld eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Statement 1: ");
FieldIf field = (FieldIf)builder.InsertField(FieldType.FieldIf, true);
field.LeftExpression = "0";
field.ComparisonOperator = "=";
field.RightExpression = "1";

// Das IF-Feld zeigt eine Zeichenfolge aus seiner Eigenschaft "TrueText" an,
// oder seine Eigenschaft „FalseText“, abhängig von der Wahrheit der von uns erstellten Aussage.
field.TrueText = "True";
field.FalseText = "False";
field.Update();

// In diesem Fall ist „0 = 1“ falsch, daher ist das angezeigte Ergebnis „Falsch“.
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

// Dieses Mal ist die Anweisung korrekt, daher ist das angezeigte Ergebnis „True“.
Assert.AreEqual(" IF  5 = \"2 + 3\" True False", field.GetFieldCode());
Assert.AreEqual(FieldIfComparisonResult.True, field.EvaluateCondition());
Assert.AreEqual("True", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IF.docx");
```

### Siehe auch

* enum [FieldIfComparisonResult](../../fieldifcomparisonresult/)
* class [FieldIf](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
