---
title: FieldCompare.RightExpression
linktitle: RightExpression
articleTitle: RightExpression
second_title: Aspose.Words per .NET
description: Scopri la proprietà RightExpression di FieldCompare per gestire e personalizzare facilmente il lato destro delle tue espressioni di confronto per ottenere prestazioni ottimali.
type: docs
weight: 40
url: /it/net/aspose.words.fields/fieldcompare/rightexpression/
---
## FieldCompare.RightExpression property

Ottiene o imposta la parte corretta dell'espressione di confronto.

```csharp
public string RightExpression { get; set; }
```

## Esempi

Mostra come confrontare espressioni utilizzando un campo COMPARE.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

FieldCompare field = (FieldCompare)builder.InsertField(FieldType.FieldCompare, true);
field.LeftExpression = "3";
field.ComparisonOperator = "<";
field.RightExpression = "2";
field.Update();

// Il campo COMPARE visualizza "0" o "1", a seconda che la sua affermazione sia veritiera.
// Il risultato di questa istruzione è falso, quindi questo campo visualizzerà "0".
Assert.AreEqual(" COMPARE  3 < 2", field.GetFieldCode());
Assert.AreEqual("0", field.Result);

builder.Writeln();

field = (FieldCompare)builder.InsertField(FieldType.FieldCompare, true);
field.LeftExpression = "5";
field.ComparisonOperator = "=";
field.RightExpression = "2 + 3";
field.Update();

// Questo campo visualizza "1" poiché l'affermazione è vera.
Assert.AreEqual(" COMPARE  5 = \"2 + 3\"", field.GetFieldCode());
Assert.AreEqual("1", field.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.COMPARE.docx");
```

### Guarda anche

* class [FieldCompare](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
