---
title: FieldIndex.SequenceName
linktitle: SequenceName
articleTitle: SequenceName
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldIndex SequenceName per gestire facilmente i nomi delle sequenze e migliorare l'efficienza della paginazione nelle tue applicazioni.
type: docs
weight: 150
url: /it/net/aspose.words.fields/fieldindex/sequencename/
---
## FieldIndex.SequenceName property

Ottiene o imposta il nome di una sequenza il cui numero è incluso nel numero di pagina.

```csharp
public string SequenceName { get; set; }
```

## Esempi

Mostra come suddividere un documento in porzioni combinando i campi INDEX e SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un campo INDICE che visualizzerà una voce per ogni campo XE trovato nel documento.
// Ogni voce visualizzerà il valore della proprietà Testo del campo XE sul lato sinistro,
// e il numero della pagina che contiene il campo XE sulla destra.
// Se i campi XE hanno lo stesso valore nella loro proprietà "Testo",
// il campo INDICE li raggrupperà in un'unica voce.
FieldIndex index = (FieldIndex)builder.InsertField(FieldType.FieldIndex, true);

// Nella proprietà SequenceName, assegna un nome a una sequenza di campi SEQ. Ogni voce di questo campo INDEX verrà ora visualizzata anche
// il numero su cui si trova il conteggio sequenziale nella posizione del campo XE che ha creato questa voce.
index.SequenceName = "MySequence";

// Imposta il testo che circonda la sequenza e i numeri di pagina per spiegarne il significato all'utente.
// Una voce creata con questa configurazione visualizzerà qualcosa come "MySequence at 1 on page 1" accanto al numero di pagina.
// PageNumberSeparator e SequenceSeparator non possono essere più lunghi di 15 caratteri.
index.PageNumberSeparator = "\tMySequence at ";
index.SequenceSeparator = " on page ";
Assert.IsTrue(index.HasSequenceName);

Assert.AreEqual(" INDEX  \\s MySequence \\e \"\tMySequence at \" \\d \" on page \"", index.GetFieldCode());

// I campi SEQ visualizzano un conteggio che aumenta in ogni campo SEQ.
// Questi campi mantengono anche conteggi separati per ogni sequenza denominata univoca
// identificato dalla proprietà "SequenceIdentifier" del campo SEQ.
// Inserisce un campo SEQ che sposta la sequenza "MySequence" a 1.
// Questo campo non è diverso dal normale testo del documento. Non apparirà nel sommario di un campo INDICE.
builder.InsertBreak(BreakType.PageBreak);
FieldSeq sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", sequenceField.GetFieldCode());

// Inserire un campo XE che creerà una voce nel campo INDICE.
// Poiché "MySequence" è a 1 e questo campo XE è a pagina 2, insieme ai separatori personalizzati che abbiamo definito sopra,
// la voce INDICE di questo campo visualizzerà "Cat" sul lato sinistro e "MySequence at 1 on page 2" sul lato destro.
FieldXE indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cat";

Assert.AreEqual(" XE  Cat", indexEntry.GetFieldCode());

// Inserire un'interruzione di pagina e utilizzare i campi SEQ per far avanzare "MySequence" a 3.
builder.InsertBreak(BreakType.PageBreak);
sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";
sequenceField = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
sequenceField.SequenceIdentifier = "MySequence";

// Inserire un campo XE con la stessa proprietà Text di quello precedente.
// La voce INDEX raggrupperà i campi XE con valori corrispondenti nella proprietà "Testo"
// in una voce anziché creare una voce per ogni campo XE.
// Poiché siamo a pagina 2 con "MySequence" a pagina 3, ", 3 a pagina 3" verrà aggiunto alla stessa voce INDEX di cui sopra.
// La parte del numero di pagina di quella voce INDEX ora visualizzerà "MySequence in 1 a pagina 2, 3 a pagina 3".
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Cat";

// Inserire un campo XE con un nuovo e univoco valore della proprietà Testo.
// Verrà aggiunta una nuova voce, con MySequence al punto 3 a pagina 4.
builder.InsertBreak(BreakType.PageBreak);
indexEntry = (FieldXE)builder.InsertField(FieldType.FieldIndexEntry, true);
indexEntry.Text = "Dog";

doc.UpdatePageLayout();
doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.INDEX.XE.Sequence.docx");
```

### Guarda anche

* class [FieldIndex](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
