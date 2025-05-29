---
title: FieldSeq.BookmarkName
linktitle: BookmarkName
articleTitle: BookmarkName
second_title: Aspose.Words per .NET
description: Scopri la proprietà FieldSeq BookmarkName per gestire facilmente la navigazione nei documenti. Imposta o recupera i nomi dei segnalibri per un riferimento fluido agli elementi.
type: docs
weight: 20
url: /it/net/aspose.words.fields/fieldseq/bookmarkname/
---
## FieldSeq.BookmarkName property

Ottiene o imposta un nome di segnalibro che fa riferimento a un elemento in un'altra posizione del documento anziché nella posizione corrente.

```csharp
public string BookmarkName { get; set; }
```

## Esempi

Mostra come combinare i campi indice e sequenza.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Un campo TOC può creare una voce nel suo indice per ogni campo SEQ trovato nel documento.
// Ogni voce contiene il paragrafo che contiene il campo SEQ,
// e il numero della pagina in cui appare il campo.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// Configurare questo campo TOC in modo che abbia una proprietà SequenceIdentifier con il valore "MySequence".
fieldToc.TableOfFiguresLabel = "MySequence";

// Configura questo campo TOC per selezionare solo i campi SEQ che rientrano nei limiti di un segnalibro
// denominato "TOCBookmark".
fieldToc.BookmarkName = "TOCBookmark";
builder.InsertBreak(BreakType.PageBreak);

Assert.AreEqual(" TOC  \\c MySequence \\b TOCBookmark", fieldToc.GetFieldCode());

// I campi SEQ visualizzano un conteggio che aumenta in ogni campo SEQ.
// Questi campi mantengono anche conteggi separati per ogni sequenza denominata univoca
// identificato dalla proprietà "SequenceIdentifier" del campo SEQ.
// Inserire un campo SEQ che abbia un identificatore di sequenza che corrisponda al TOC
// Proprietà TableOfFiguresLabel. Questo campo non creerà una voce nel sommario poiché è esterno
// i limiti del segnalibro designati da "BookmarkName".
builder.Write("MySequence #");
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will not show up in the TOC because it is outside of the bookmark.");

builder.StartBookmark("TOCBookmark");

// La sequenza di questo campo SEQ corrisponde alla proprietà "TableOfFiguresLabel" del TOC ed è compresa nei limiti del segnalibro.
// Il paragrafo che contiene questo campo verrà visualizzato nell'indice come voce.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", will show up in the TOC next to the entry for the above caption.");

// La sequenza di questo campo SEQ non corrisponde alla proprietà "TableOfFiguresLabel" del TOC,
// e rientra nei limiti del segnalibro. Il relativo paragrafo non verrà visualizzato nell'indice come voce.
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "OtherSequence";
builder.Writeln(", will not show up in the TOC because it's from a different sequence identifier.");

// La sequenza di questo campo SEQ corrisponde alla proprietà "TableOfFiguresLabel" del TOC ed è compresa nei limiti del segnalibro.
// Questo campo fa riferimento anche a un altro segnalibro. Il contenuto di quel segnalibro apparirà nella voce dell'indice di questo campo SEQ.
// Il campo SEQ stesso non visualizzerà il contenuto di quel segnalibro.
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
fieldSeq.BookmarkName = "SEQBookmark";
Assert.AreEqual(" SEQ  MySequence SEQBookmark", fieldSeq.GetFieldCode());

// Crea un segnalibro con contenuti che verranno visualizzati nella voce TOC grazie al campo SEQ soprastante che vi fa riferimento.
builder.InsertBreak(BreakType.PageBreak);
builder.StartBookmark("SEQBookmark");
builder.Write("MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";
builder.Writeln(", text from inside SEQBookmark.");
builder.EndBookmark("SEQBookmark");

builder.EndBookmark("TOCBookmark");

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.SEQ.Bookmark.docx");
```

### Guarda anche

* class [FieldSeq](../)
* spazio dei nomi [Aspose.Words.Fields](../../../aspose.words.fields/)
* assemblea [Aspose.Words](../../../)
