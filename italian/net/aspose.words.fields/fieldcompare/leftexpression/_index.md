---
title: FieldCompare.LeftExpression
linktitle: LeftExpression
articleTitle: LeftExpression
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldCompare LeftExpression, accedi facilmente o modifica il lato sinistro delle tue espressioni di confronto per un'analisi avanzata dei dati.
type: docs
weight: 30
url: /it/net/aspose.words.fields/fieldcompare/leftexpression/
---
## FieldCompare.LeftExpression property

Ottiene o imposta la parte sinistra dell'espressione di confronto.

```csharp
public string LeftExpression { get; set; }
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
