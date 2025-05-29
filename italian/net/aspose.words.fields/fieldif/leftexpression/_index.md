---
title: FieldIf.LeftExpression
linktitle: LeftExpression
articleTitle: LeftExpression
second_title: Aspose.Words per .NET
description: Scopri la proprietà LeftExpression di FieldIf e gestisci facilmente il lato sinistro della tua espressione di confronto per una migliore gestione e analisi dei dati.
type: docs
weight: 40
url: /it/net/aspose.words.fields/fieldif/leftexpression/
---
## FieldIf.LeftExpression property

Ottiene o imposta la parte sinistra dell'espressione di confronto.

```csharp
public string LeftExpression { get; set; }
```

## Esempi

Mostra come inserire un campo SE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Statement 1: ");
FieldIf field = (FieldIf)builder.InsertField(FieldType.FieldIf, true);
field.LeftExpression = "0";
field.ComparisonOperator = "=";
field.RightExpression = "1";

// Il campo IF visualizzerà una stringa dalla sua proprietà "TrueText",
// o la sua proprietà "FalseText", a seconda della veridicità dell'affermazione che abbiamo costruito.
field.TrueText = "True";
field.FalseText = "False";
field.Update();

// In questo caso, "0 = 1" non è corretto, quindi il risultato visualizzato sarà "Falso".
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

// Questa volta l'affermazione è corretta, quindi il risultato visualizzato sarà "True".
Assert.AreEqual(" IF  5 = \"2 + 3\" True False", field.GetFieldCode());
Assert.AreEqual(FieldIfComparisonResult.True, field.EvaluateCondition());
Assert.AreEqual("True", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.IF.docx");
```

### Guarda anche

* class [FieldIf](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
