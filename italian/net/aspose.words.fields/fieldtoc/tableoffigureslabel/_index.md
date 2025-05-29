---
title: FieldToc.TableOfFiguresLabel
linktitle: TableOfFiguresLabel
articleTitle: TableOfFiguresLabel
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldToc TableOfFiguresLabel per personalizzare facilmente il tuo indice delle figure. Migliora l'organizzazione e la chiarezza del tuo documento!
type: docs
weight: 160
url: /it/net/aspose.words.fields/fieldtoc/tableoffigureslabel/
---
## FieldToc.TableOfFiguresLabel property

Ottiene o imposta il nome dell'identificatore di sequenza utilizzato durante la creazione di una tabella di figure.

```csharp
public string TableOfFiguresLabel { get; set; }
```

## Esempi

Mostra come popolare un campo TOC con voci utilizzando i campi SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Un campo TOC può creare una voce nel suo indice per ogni campo SEQ trovato nel documento.
// Ogni voce contiene il paragrafo che include il campo SEQ e il numero di pagina in cui appare il campo.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// I campi SEQ visualizzano un conteggio che aumenta in ogni campo SEQ.
// Questi campi mantengono anche conteggi separati per ogni sequenza denominata univoca
// identificato dalla proprietà "SequenceIdentifier" del campo SEQ.
// Utilizzare la proprietà "TableOfFiguresLabel" per assegnare un nome alla sequenza principale per l'indice.
// Ora, questo TOC creerà voci solo dai campi SEQ con il loro "SequenceIdentifier" impostato su "MySequence".
fieldToc.TableOfFiguresLabel = "MySequence";

// Possiamo nominare un'altra sequenza di campi SEQ nella proprietà "PrefixedSequenceIdentifier".
 // I campi SEQ di questa sequenza di prefissi non creeranno voci TOC.
// Ogni voce TOC creata da un campo SEQ della sequenza principale ora visualizzerà anche il conteggio che
// la sequenza del prefisso è attualmente attiva nel campo SEQ della sequenza primaria che ha creato la voce.
fieldToc.PrefixedSequenceIdentifier = "PrefixSequence";

// Ogni voce del TOC visualizzerà il conteggio della sequenza del prefisso immediatamente a sinistra
// del numero di pagina in cui appare il campo SEQ della sequenza principale.
// Possiamo specificare un separatore personalizzato che apparirà tra questi due numeri.
fieldToc.SequenceSeparator = ">";

Assert.AreEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);

// Esistono due modi per utilizzare i campi SEQ per popolare questo indice.
// 1 - Inserimento di un campo SEQ appartenente alla sequenza di prefissi del TOC:
// Questo campo incrementerà di 1 il conteggio delle sequenze SEQ per "PrefixSequence".
// Poiché questo campo non appartiene alla sequenza principale identificata
// tramite la proprietà "TableOfFiguresLabel" del TOC, non verrà visualizzato come voce.
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();

Assert.AreEqual(" SEQ  PrefixSequence", fieldSeq.GetFieldCode());

// 2 - Inserimento di un campo SEQ appartenente alla sequenza principale del TOC:
// Questo campo SEQ creerà una voce nel sommario.
// La voce TOC conterrà il paragrafo in cui si trova il campo SEQ e il numero della pagina in cui appare.
// Questa voce mostrerà anche il conteggio attuale della sequenza di prefissi,
// separato dal numero di pagina dal valore della proprietà SeqenceSeparator del TOC.
// Il conteggio "PrefixSequence" è a 1, questo campo SEQ della sequenza principale si trova a pagina 2,
// e il separatore è ">", quindi la voce visualizzerà "1>2".
builder.Write("First TOC entry, MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", fieldSeq.GetFieldCode());

// Inserisce una pagina, fa avanzare di 2 la sequenza del prefisso e inserisce un campo SEQ per creare in seguito una voce di sommario.
// La sequenza del prefisso è ora a 2 e il campo SEQ della sequenza principale è a pagina 3,
// quindi la voce TOC visualizzerà "2>3" al suo conteggio di pagine.
builder.InsertBreak(BreakType.PageBreak);
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
builder.Write("Second TOC entry, MySequence #");
fieldSeq.SequenceIdentifier = "MySequence";

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.TOC.SEQ.docx");
```

### Guarda anche

* class [FieldToc](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
