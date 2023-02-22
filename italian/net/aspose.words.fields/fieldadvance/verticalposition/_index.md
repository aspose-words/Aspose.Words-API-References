---
title: FieldAdvance.VerticalPosition
second_title: Aspose.Words per .NET API Reference
description: FieldAdvance proprietà. Ottiene o imposta il numero di punti di cui il testo che segue il campo deve essere spostato verticalmente dal bordo superiore della pagina.
type: docs
weight: 70
url: /it/net/aspose.words.fields/fieldadvance/verticalposition/
---
## FieldAdvance.VerticalPosition property

Ottiene o imposta il numero di punti di cui il testo che segue il campo deve essere spostato verticalmente dal bordo superiore della pagina.

```csharp
public string VerticalPosition { get; set; }
```

### Esempi

Mostra come inserire un campo ADVANCE e modificarne le proprietà.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This text is in its normal place.");

// Di seguito sono riportati due modi per utilizzare il campo AVANZAMENTO per regolare la posizione del testo che lo segue.
// Gli effetti di un campo ADVANCE continuano ad essere applicati fino alla fine del paragrafo,
// o un altro campo ADVANCE aggiorna i valori di offset/coordinate.
// 1 - Specificare un offset direzionale:
FieldAdvance field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.RightOffset = "5";
field.UpOffset = "5";

Assert.AreEqual(" ADVANCE  \\r 5 \\u 5", field.GetFieldCode());

builder.Write("This text will be moved up and to the right.");

field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.DownOffset = "5";
field.LeftOffset = "100";

Assert.AreEqual(" ADVANCE  \\d 5 \\l 100", field.GetFieldCode());

builder.Writeln("This text is moved down and to the left, overlapping the previous text.");

// 2 - Sposta il testo in una posizione specificata dalle coordinate:
field = (FieldAdvance)builder.InsertField(FieldType.FieldAdvance, true);
field.HorizontalPosition = "-100";
field.VerticalPosition = "200";

Assert.AreEqual(" ADVANCE  \\x -100 \\y 200", field.GetFieldCode());

builder.Write("This text is in a custom position.");

doc.Save(ArtifactsDir + "Field.ADVANCE.docx");
```

### Guarda anche

* class [FieldAdvance](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldadvance/)
* assemblea [Aspose.Words](../../../)


