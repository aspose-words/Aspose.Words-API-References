---
title: FieldToc
second_title: Aspose.Words per .NET API Reference
description: Implementa il campo TOC.
type: docs
weight: 2380
url: /it/net/aspose.words.fields/fieldtoc/
---
## FieldToc class

Implementa il campo TOC.

```csharp
public class FieldToc : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldToc](fieldtoc)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldtoc/bookmarkname) { get; set; } | Ottiene o imposta il nome del segnalibro che contrassegna la parte del documento utilizzata per creare la tabella. |
| [CaptionlessTableOfFiguresLabel](../../aspose.words.fields/fieldtoc/captionlesstableoffigureslabel) { get; set; } | Ottiene o imposta il nome dell'identificatore di sequenza utilizzato durante la creazione di una tabella di cifre che non include l'etichetta e il numero della didascalia . |
| [CustomStyles](../../aspose.words.fields/fieldtoc/customstyles) { get; set; } | Ottiene o imposta un elenco di stili diversi dagli stili di intestazione incorporati da includere nel sommario. |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [End](../../aspose.words.fields/field/end) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [EntryIdentifier](../../aspose.words.fields/fieldtoc/entryidentifier) { get; set; } | Ottiene o imposta una stringa che deve corrispondere agli identificatori di tipo dei campi TC inclusi. |
| [EntryLevelRange](../../aspose.words.fields/fieldtoc/entrylevelrange) { get; set; } | Ottiene o imposta un intervallo di livelli delle voci del sommario da includere. |
| [EntrySeparator](../../aspose.words.fields/fieldtoc/entryseparator) { get; set; } | Ottiene o imposta una sequenza di caratteri che separa una voce e il relativo numero di pagina. |
| [Format](../../aspose.words.fields/field/format) { get; } | Ottiene a[`FieldFormat`](../fieldformat) oggetto che fornisce l'accesso digitato alla formattazione del campo. |
| [HeadingLevelRange](../../aspose.words.fields/fieldtoc/headinglevelrange) { get; set; } | Ottiene o imposta un intervallo di livelli di intestazione da includere. |
| [HideInWebLayout](../../aspose.words.fields/fieldtoc/hideinweblayout) { get; set; } | Ottiene o imposta se nascondere l'intestazione di tabulazione e i numeri di pagina nella visualizzazione layout Web. |
| [InsertHyperlinks](../../aspose.words.fields/fieldtoc/inserthyperlinks) { get; set; } | Ottiene o imposta se creare collegamenti ipertestuali alle voci del sommario. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolarne il risultato). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [PageNumberOmittingLevelRange](../../aspose.words.fields/fieldtoc/pagenumberomittinglevelrange) { get; set; } | Ottiene o imposta un intervallo di livelli delle voci del sommario da cui omettere i numeri di pagina. |
| [PrefixedSequenceIdentifier](../../aspose.words.fields/fieldtoc/prefixedsequenceidentifier) { get; set; } | Ottiene o imposta l'identificatore di una sequenza per la quale deve essere aggiunto un prefisso al numero di pagina della voce. |
| [PreserveLineBreaks](../../aspose.words.fields/fieldtoc/preservelinebreaks) { get; set; } | Ottiene o imposta se conservare i caratteri di nuova riga all'interno delle voci della tabella. |
| [PreserveTabs](../../aspose.words.fields/fieldtoc/preservetabs) { get; set; } | Ottiene o imposta se conservare le voci delle schede all'interno delle voci della tabella. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Ottiene o imposta il testo che si trova tra il separatore di campo e la fine del campo. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Ottiene il nodo che rappresenta il separatore di campo. Può essere nullo. |
| [SequenceSeparator](../../aspose.words.fields/fieldtoc/sequenceseparator) { get; set; } | Ottiene o imposta la sequenza di caratteri utilizzata per separare i numeri di sequenza e i numeri di pagina. |
| [Start](../../aspose.words.fields/field/start) { get; } | Ottiene il nodo che rappresenta l'inizio del campo. |
| [TableOfFiguresLabel](../../aspose.words.fields/fieldtoc/tableoffigureslabel) { get; set; } | Ottiene o imposta il nome dell'identificatore di sequenza utilizzato durante la creazione di una tabella di cifre. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Ottiene il tipo di campo di Microsoft Word. |
| [UseParagraphOutlineLevel](../../aspose.words.fields/fieldtoc/useparagraphoutlinelevel) { get; set; } | Ottiene o imposta se utilizzare il livello di struttura del paragrafo applicato. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non è presente alcun separatore). Sono inclusi sia il codice campo che il risultato campo dei campi figlio. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è un separatore). |
| [Remove](../../aspose.words.fields/field/remove)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del suo nodo padre, restituisce il suo paragrafo padre. Se il campo è già stato rimosso, ritorna **nullo** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Esegue lo scollegamento del campo. |
| [Update](../../aspose.words.fields/field/update)() | Esegue l'aggiornamento del campo. Genera se il campo è già in fase di aggiornamento. |
| [Update](../../aspose.words.fields/field/update)(bool) | Esegue un aggiornamento del campo. Genera se il campo è già in fase di aggiornamento. |
| [UpdatePageNumbers](../../aspose.words.fields/fieldtoc/updatepagenumbers)() | Aggiorna i numeri di pagina per gli elementi in questo sommario. |

### Osservazioni

Crea un sommario (che può anche essere un sommario) usando le voci specificate dai campi TC, i loro livelli di intestazione e gli stili specificati, e inserisce quella tabella in questo punto del documento.

### Esempi

Mostra come inserire un sommario e popolarlo con voci basate sugli stili di intestazione.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.StartBookmark("MyBookmark");

    // Inserisce un campo TOC, che compilerà tutte le intestazioni in un sommario.
    // Per ogni intestazione, questo campo creerà una riga con il testo in quello stile di intestazione a sinistra,
    // e la pagina in cui compare l'intestazione a destra.
    FieldToc field = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

    // Usa la proprietà BookmarkName per elencare solo le intestazioni
    // che appaiono entro i limiti di un segnalibro con il nome "MyBookmark".
    field.BookmarkName = "MyBookmark";

    // Il testo con uno stile di intestazione integrato, ad esempio "Intestazione 1", applicato ad esso verrà conteggiato come intestazione.
    // Possiamo nominare stili aggiuntivi da raccogliere come intestazioni dal TOC in questa proprietà e nei relativi livelli TOC.
    field.CustomStyles = "Quote; 6; Intense Quote; 7";

    // Per impostazione predefinita, i livelli Styles/TOC sono separati da una virgola nella proprietà CustomStyles,
    // ma possiamo impostare un delimitatore personalizzato in questa proprietà.
    doc.FieldOptions.CustomTocStyleSeparator = ";";

    // Configura il campo per escludere tutte le intestazioni con livelli di sommario al di fuori di questo intervallo.
    field.HeadingLevelRange = "1-3";

    // Il sommario non visualizzerà i numeri di pagina delle intestazioni i cui livelli di sommario rientrano in questo intervallo.
    field.PageNumberOmittingLevelRange = "2-5";

     // Imposta una stringa personalizzata che separerà ogni intestazione dal numero di pagina.
    field.EntrySeparator = "-";
    field.InsertHyperlinks = true;
    field.HideInWebLayout = false;
    field.PreserveLineBreaks = true;
    field.PreserveTabs = true;
    field.UseParagraphOutlineLevel = false;

    InsertNewPageWithHeading(builder, "First entry", "Heading 1");
    builder.Writeln("Paragraph text.");
    InsertNewPageWithHeading(builder, "Second entry", "Heading 1");
    InsertNewPageWithHeading(builder, "Third entry", "Quote");
    InsertNewPageWithHeading(builder, "Fourth entry", "Intense Quote");

    // Queste due intestazioni avranno i numeri di pagina omessi perché rientrano nell'intervallo "2-5".
    InsertNewPageWithHeading(builder, "Fifth entry", "Heading 2");
    InsertNewPageWithHeading(builder, "Sixth entry", "Heading 3");

    // Questa voce non viene visualizzata perché "Intestazione 4" è al di fuori dell'intervallo "1-3" che abbiamo impostato in precedenza.
    InsertNewPageWithHeading(builder, "Seventh entry", "Heading 4");

    builder.EndBookmark("MyBookmark");
    builder.Writeln("Paragraph text.");

    // Questa voce non viene visualizzata perché è al di fuori del segnalibro specificato dal sommario.
    InsertNewPageWithHeading(builder, "Eighth entry", "Heading 1");

    Assert.AreEqual(" TOC  \\b MyBookmark \\t \"Quote; 6; Intense Quote; 7\" \\o 1-3 \\n 2-5 \\p - \\h \\x \\w", field.GetFieldCode());

    field.UpdatePageNumbers();
    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOC.docx");

/// <summary>
/// Inizia una nuova pagina e inserisci un paragrafo di uno stile specificato.
/// </summary>
public void InsertNewPageWithHeading(DocumentBuilder builder, string captionText, string styleName)
{
    builder.InsertBreak(BreakType.PageBreak);
    string originalStyle = builder.ParagraphFormat.StyleName;
    builder.ParagraphFormat.Style = builder.Document.Styles[styleName];
    builder.Writeln(captionText);
    builder.ParagraphFormat.Style = builder.Document.Styles[originalStyle];
}
```

Mostra come popolare un campo TOC con voci utilizzando i campi SEQ.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Un campo TOC può creare una voce nel suo sommario per ogni campo SEQ trovato nel documento.
// Ogni voce contiene il paragrafo che include il campo SEQ e il numero della pagina su cui appare il campo.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

// I campi SEQ mostrano un conteggio che aumenta ad ogni campo SEQ.
// Questi campi mantengono anche conteggi separati per ciascuna sequenza denominata univoca
// identificato dalla proprietà "SequenceIdentifier" del campo SEQ.
// Utilizzare la proprietà "TableOfFiguresLabel" per denominare una sequenza principale per il sommario.
// Ora, questo sommario creerà solo voci dai campi SEQ con il loro "SequenceIdentifier" impostato su "MySequence".
fieldToc.TableOfFiguresLabel = "MySequence";

// Possiamo nominare un'altra sequenza di campi SEQ nella proprietà "PrefixedSequenceIdentifier".
 // I campi SEQ di questa sequenza di prefissi non creeranno voci TOC.
// Ogni voce TOC creata da un campo SEQ della sequenza principale ora visualizzerà anche il conteggio
// la sequenza del prefisso è attualmente attiva nel campo SEQ della sequenza primaria che ha effettuato la voce.
fieldToc.PrefixedSequenceIdentifier = "PrefixSequence";

// Ogni voce TOC visualizzerà il conteggio della sequenza del prefisso immediatamente a sinistra
// del numero di pagina su cui appare il campo SEQ della sequenza principale.
// Possiamo specificare un separatore personalizzato che apparirà tra questi due numeri.
fieldToc.SequenceSeparator = ">";

Assert.AreEqual(" TOC  \\c MySequence \\s PrefixSequence \\d >", fieldToc.GetFieldCode());

builder.InsertBreak(BreakType.PageBreak);

// Esistono due modi per utilizzare i campi SEQ per popolare questo sommario.
// 1 - Inserimento di un campo SEQ che appartiene alla sequenza di prefissi del TOC:
// Questo campo incrementerà il conteggio della sequenza SEQ per "PrefixSequence" di 1.
// Poiché questo campo non appartiene alla sequenza principale identificata
// dalla proprietà "TableOfFiguresLabel" del sommario, non apparirà come voce.
FieldSeq fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "PrefixSequence";
builder.InsertParagraph();

Assert.AreEqual(" SEQ  PrefixSequence", fieldSeq.GetFieldCode());

// 2 - Inserimento di un campo SEQ che appartiene alla sequenza principale del TOC:
// Questo campo SEQ creerà una voce nel sommario.
// La voce TOC conterrà il paragrafo in cui si trova il campo SEQ e il numero della pagina in cui appare.
// Questa voce visualizzerà anche il conteggio a cui si trova attualmente la sequenza di prefissi,
// separato dal numero di pagina dal valore nella proprietà SeqenceSeparator del sommario.
// Il conteggio "PrefixSequence" è a 1, questo campo SEQ della sequenza principale è a pagina 2,
// e il separatore è ">", quindi la voce visualizzerà "1>2".
builder.Write("First TOC entry, MySequence #");
fieldSeq = (FieldSeq)builder.InsertField(FieldType.FieldSequence, true);
fieldSeq.SequenceIdentifier = "MySequence";

Assert.AreEqual(" SEQ  MySequence", fieldSeq.GetFieldCode());

// Inserisci una pagina, fai avanzare la sequenza del prefisso di 2 e inserisci un campo SEQ per creare una voce TOC in seguito.
// La sequenza del prefisso è ora a 2 e il campo SEQ della sequenza principale è a pagina 3,
// quindi la voce TOC visualizzerà "2>3" al conteggio delle pagine.
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

* class [Field](../field)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
