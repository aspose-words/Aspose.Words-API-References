---
title: FieldSeq.ResetHeadingLevel
linktitle: ResetHeadingLevel
articleTitle: ResetHeadingLevel
second_title: Aspose.Words per .NET
description: Scopri la proprietà ResetHeadingLevel di FieldSeq e gestisci facilmente i livelli di intestazione reimpostando i numeri di sequenza. Semplifica la formattazione dei tuoi documenti oggi stesso!
type: docs
weight: 40
url: /it/net/aspose.words.fields/fieldseq/resetheadinglevel/
---
## FieldSeq.ResetHeadingLevel property

Ottiene o imposta un numero intero che rappresenta un livello di intestazione a cui reimpostare il numero di sequenza. Restituisce -1 se il numero è assente.

```csharp
public string ResetHeadingLevel { get; set; }
```

## Esempi

Mostra come creare una numerazione utilizzando i campi SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// I campi SEQ visualizzano un conteggio che aumenta in ogni campo SEQ.
// Questi campi mantengono anche conteggi separati per ogni sequenza denominata univoca
// identificato dalla proprietà "SequenceIdentifier" del campo SEQ.
// Inserisci un campo SEQ che visualizzerà il valore del conteggio corrente di "MySequence",
// dopo aver utilizzato la proprietà "ResetNumber" per impostarla su 100.
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

// Inserire un'intestazione di livello 1.
builder.InsertBreak(BreakType.ParagraphBreak);
builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("This level 1 heading will reset MySequence to 1");
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// Inserire un altro campo SEQ dalla stessa sequenza e configurarlo per reimpostare il conteggio a ogni intestazione con 1.
builder.Write("\n#");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.ResetHeadingLevel = "1";
fieldSeq.Update();

// L'intestazione sopra è un'intestazione di livello 1, quindi il conteggio per questa sequenza viene reimpostato a 1.
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
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
