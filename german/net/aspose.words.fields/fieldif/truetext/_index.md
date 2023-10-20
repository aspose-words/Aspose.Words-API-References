---
title: FieldIf.TrueText
linktitle: TrueText
articleTitle: TrueText
second_title: Aspose.Words für .NET
description: FieldIf TrueText eigendom. Ruft den angezeigten Text ab oder legt diesen fest wenn der Vergleichsausdruck wahr ist in C#.
type: docs
weight: 60
url: /de/net/aspose.words.fields/fieldif/truetext/
---
## FieldIf.TrueText property

Ruft den angezeigten Text ab oder legt diesen fest, wenn der Vergleichsausdruck wahr ist.

```csharp
public string TrueText { get; set; }
```

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

// Das IF-Feld zeigt eine Zeichenfolge entweder seiner „TrueText“-Eigenschaft an,
// oder seine „FalseText“-Eigenschaft, abhängig von der Wahrheit der Aussage, die wir erstellt haben.
field.TrueText = "True";
field.FalseText = "False";
field.Update();

// In diesem Fall ist „0 = 1“ falsch, daher wird das angezeigte Ergebnis „Falsch“ sein.
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

// Diesmal ist die Aussage korrekt, daher wird das angezeigte Ergebnis „True“ sein.
Assert.AreEqual(" IF  5 = \"2 + 3\" True False", field.GetFieldCode());
Assert.AreEqual(FieldIfComparisonResult.True, field.EvaluateCondition());
Assert.AreEqual("True", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IF.docx");
```

### Siehe auch

* class [FieldIf](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
