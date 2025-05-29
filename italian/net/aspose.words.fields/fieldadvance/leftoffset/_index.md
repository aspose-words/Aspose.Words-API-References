---
title: FieldAdvance.LeftOffset
linktitle: LeftOffset
articleTitle: LeftOffset
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldAdvance LeftOffset per regolare facilmente l'allineamento del testo impostando punti per uno spostamento preciso verso sinistra. Migliora il layout del tuo documento!
type: docs
weight: 40
url: /it/net/aspose.words.fields/fieldadvance/leftoffset/
---
## FieldAdvance.LeftOffset property

Ottiene o imposta il numero di punti di cui il testo che segue il campo deve essere spostato a sinistra.

```csharp
public string LeftOffset { get; set; }
```

## Esempi

Mostra come inserire un campo ADVANCE e modificarne le proprietà.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("This text is in its normal place.");

// Di seguito sono riportati due modi per utilizzare il campo ADVANCE per regolare la posizione del testo che lo segue.
// Gli effetti di un campo ADVANCE continuano ad essere applicati fino alla fine del paragrafo,
// oppure un altro campo ADVANCE aggiorna i valori di offset/coordinate.
// 1 - Specificare uno scostamento direzionale:
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
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
