---
title: FieldCompare.RightExpression
linktitle: RightExpression
articleTitle: RightExpression
second_title: Aspose.Words per .NET
description: FieldCompare RightExpression proprietà. Ottiene o imposta la parte destra dellespressione di confronto in C#.
type: docs
weight: 40
url: /it/net/aspose.words.fields/fieldcompare/rightexpression/
---
## FieldCompare.RightExpression property

Ottiene o imposta la parte destra dell'espressione di confronto.

```csharp
public string RightExpression { get; set; }
```

## Esempi

Mostra come confrontare le espressioni utilizzando un campo COMPARE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldCompare field = (FieldCompare)builder.InsertField(FieldType.FieldCompare, true);
field.LeftExpression = "3";
field.ComparisonOperator = "<";
field.RightExpression = "2";
field.Update();

// Il campo COMPARE visualizza uno "0" o un "1", a seconda della verità della sua affermazione.
// Il risultato di questa affermazione è falso, quindi questo campo visualizzerà uno "0".
Assert.AreEqual(" COMPARE  3 < 2", field.GetFieldCode());
Assert.AreEqual("0", field.Result);

builder.Writeln();

field = (FieldCompare)builder.InsertField(FieldType.FieldCompare, true);
field.LeftExpression = "5";
field.ComparisonOperator = "=";
field.RightExpression = "2 + 3";
field.Update();

// Questo campo visualizza un "1" poiché l'affermazione è vera.
Assert.AreEqual(" COMPARE  5 = \"2 + 3\"", field.GetFieldCode());
Assert.AreEqual("1", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.COMPARE.docx");
```

### Guarda anche

* class [FieldCompare](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
