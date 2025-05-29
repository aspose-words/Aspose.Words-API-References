---
title: FieldIf.LeftExpression
linktitle: LeftExpression
articleTitle: LeftExpression
second_title: Aspose.Words für .NET
description: Entdecken Sie die LeftExpression-Eigenschaft von FieldIf und verwalten Sie ganz einfach die linke Seite Ihres Vergleichsausdrucks für eine verbesserte Datenverarbeitung und -analyse.
type: docs
weight: 40
url: /de/net/aspose.words.fields/fieldif/leftexpression/
---
## FieldIf.LeftExpression property

Ruft den linken Teil des Vergleichsausdrucks ab oder legt ihn fest.

```csharp
public string LeftExpression { get; set; }
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

* class [FieldIf](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
