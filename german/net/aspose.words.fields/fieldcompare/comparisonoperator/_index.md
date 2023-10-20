---
title: FieldCompare.ComparisonOperator
linktitle: ComparisonOperator
articleTitle: ComparisonOperator
second_title: Aspose.Words für .NET
description: FieldCompare ComparisonOperator eigendom. Ruft den Vergleichsoperator ab oder legt ihn fest in C#.
type: docs
weight: 20
url: /de/net/aspose.words.fields/fieldcompare/comparisonoperator/
---
## FieldCompare.ComparisonOperator property

Ruft den Vergleichsoperator ab oder legt ihn fest.

```csharp
public string ComparisonOperator { get; set; }
```

## Beispiele

Zeigt, wie Ausdrücke mithilfe eines COMPARE-Felds verglichen werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldCompare field = (FieldCompare)builder.InsertField(FieldType.FieldCompare, true);
field.LeftExpression = "3";
field.ComparisonOperator = "<";
field.RightExpression = "2";
field.Update();

// Das COMPARE-Feld zeigt eine „0“ oder eine „1“ an, abhängig von der Wahrheit seiner Aussage.
// Das Ergebnis dieser Anweisung ist falsch, sodass in diesem Feld eine „0“ angezeigt wird.
Assert.AreEqual(" COMPARE  3 < 2", field.GetFieldCode());
Assert.AreEqual("0", field.Result);

builder.Writeln();

field = (FieldCompare)builder.InsertField(FieldType.FieldCompare, true);
field.LeftExpression = "5";
field.ComparisonOperator = "=";
field.RightExpression = "2 + 3";
field.Update();

// Dieses Feld zeigt eine „1“ an, da die Aussage wahr ist.
Assert.AreEqual(" COMPARE  5 = \"2 + 3\"", field.GetFieldCode());
Assert.AreEqual("1", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.COMPARE.docx");
```

### Siehe auch

* class [FieldCompare](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
