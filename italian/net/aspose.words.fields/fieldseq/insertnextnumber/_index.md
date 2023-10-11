---
title: FieldSeq.InsertNextNumber
second_title: Aspose.Words per .NET API Reference
description: FieldSeq proprietà. Ottiene o imposta se inserire il numero di sequenza successivo per lelemento specificato.
type: docs
weight: 30
url: /it/net/aspose.words.fields/fieldseq/insertnextnumber/
---
## FieldSeq.InsertNextNumber property

Ottiene o imposta se inserire il numero di sequenza successivo per l'elemento specificato.

```csharp
public bool InsertNextNumber { get; set; }
```

### Esempi

Mostra la creazione della numerazione utilizzando i campi SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// I campi SEQ visualizzano un conteggio che aumenta in ciascun campo SEQ.
// Questi campi mantengono inoltre conteggi separati per ciascuna sequenza con nome univoco
// identificato dalla proprietà "SequenceIdentifier" del campo SEQ.
// Inserisci un campo SEQ che visualizzerà il valore di conteggio corrente di "MySequence",
// dopo aver utilizzato la proprietà "ResetNumber" per impostarlo su 100.
builder.Write("#");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetNumber = "100";
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\r 100", fieldSeq.GetFieldCode());
Assert.AreEqual("100", fieldSeq.Result);

// Visualizza il numero successivo in questa sequenza con un altro campo SEQ.
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.Update();

Assert.AreEqual("101", fieldSeq.Result);

// Inserisci un'intestazione di livello 1.
builder.InsertBreak(BreakType.ParagraphBreak);
builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("This level 1 heading will reset MySequence to 1");
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// Inserisci un altro campo SEQ dalla stessa sequenza e configuralo per reimpostare il conteggio ad ogni intestazione con 1.
builder.Write("\n#");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetHeadingLevel = "1";
fieldSeq.Update();

// L'intestazione sopra è un'intestazione di livello 1, quindi il conteggio per questa sequenza viene reimpostato su 1.
Assert.AreEqual(" SEQ  MySequence \\s 1", fieldSeq.GetFieldCode());
Assert.AreEqual("1", fieldSeq.Result);

// Passa al numero successivo di questa sequenza.
builder.Write(", #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.InsertNextNumber = true;
fieldSeq.Update();

Assert.AreEqual(" SEQ  MySequence \\n", fieldSeq.GetFieldCode());
Assert.AreEqual("2", fieldSeq.Result);

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.ResetNumbering.docx");
```

### Guarda anche

* class [FieldSeq](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldseq/)
* assemblea [Aspose.Words](../../../)


