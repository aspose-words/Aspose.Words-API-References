---
title: FieldIndex.HasSequenceName
second_title: Aspose.Words per .NET API Reference
description: FieldIndex proprietà. Ottiene un valore che indica se è necessario utilizzare una sequenza durante la creazione del risultato del campo.
type: docs
weight: 60
url: /it/net/aspose.words.fields/fieldindex/hassequencename/
---
## FieldIndex.HasSequenceName property

Ottiene un valore che indica se è necessario utilizzare una sequenza durante la creazione del risultato del campo.

```csharp
public bool HasSequenceName { get; }
```

### Esempi

Mostra come dividere un documento in parti combinando i campi INDEX e SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un campo INDICE che visualizzerà una voce per ogni campo XE trovato nel documento.
// Ogni voce visualizzerà il valore della proprietà Text del campo XE sul lato sinistro,
// e il numero della pagina che contiene il campo XE a destra.
// Se i campi XE hanno lo stesso valore nella loro proprietà "Testo",
// il campo INDICE li raggrupperà in un'unica voce.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Nella proprietà SequenceName, denominare una sequenza di campi SEQ. Verrà ora visualizzata anche ogni voce di questo campo INDICE
// il numero su cui si trova il conteggio della sequenza nella posizione del campo XE che ha creato questa voce.
index.SequenceName = "MySequence";

// Imposta il testo che circonda la sequenza e i numeri di pagina per spiegarne il significato all'utente.
// Una voce creata con questa configurazione mostrerà qualcosa come "MySequence at 1 on page 1" al suo numero di pagina.
// PageNumberSeparator e SequenceSeparator non possono contenere più di 15 caratteri.
index.PageNumberSeparator = "\tMySequence at ";
index.SequenceSeparator = " on page ";
Assert.IsTrue(index.HasSequenceName);

Assert.AreEqual(" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index.GetFieldCode());

// I campi SEQ visualizzano un conteggio che aumenta in ciascun campo SEQ.
// Questi campi mantengono inoltre conteggi separati per ciascuna sequenza con nome univoco
// identificato dalla proprietà "SequenceIdentifier" del campo SEQ.
// Inserisci un campo SEQ che sposta la sequenza "MySequence" su 1.
// Questo campo non è diverso dal normale testo del documento. Non verrà visualizzato nel sommario di un campo INDICE.
builder.InsertBreak(BreakType.PageBreak);
FieldSeq sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", sequenceField.GetFieldCode());

// Inserisci un campo XE che creerà una voce nel campo INDICE.
// Poiché "MySequence" è su 1 e questo campo XE è a pagina 2, insieme ai separatori personalizzati definiti sopra,
// la voce INDEX di questo campo visualizzerà "Cat" sul lato sinistro e "MySequence at 1 on page 2" sul lato destro.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cat";

Assert.AreEqual(" XE  Cat", indexEntry.GetFieldCode());

// Inserisci un'interruzione di pagina e utilizza i campi SEQ per far avanzare "MySequence" a 3.
builder.InsertBreak(BreakType.PageBreak);
sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";
sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";

// Inserisci un campo XE con la stessa proprietà Text di quello sopra.
// La voce INDEX raggrupperà i campi XE con valori corrispondenti nella proprietà "Testo".
// in una voce invece di creare una voce per ciascun campo XE.
// Poiché siamo a pagina 2 con "MySequence" a 3, ", 3 a pagina 3" verrà aggiunto alla stessa voce INDEX di cui sopra.
// La parte del numero di pagina di quella voce INDEX ora visualizzerà "MySequence at 1 a pagina 2, 3 a pagina 3".
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cat";

// Inserisci un campo XE con un valore della proprietà Text nuovo e univoco.
// Questo aggiungerà una nuova voce, con MySequence al 3 a pagina 4.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Dog";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Sequence.docx");
```

### Guarda anche

* class [FieldIndex](../)
* spazio dei nomi [Aspose.Words.Fields](../../fieldindex/)
* assemblea [Aspose.Words](../../../)


