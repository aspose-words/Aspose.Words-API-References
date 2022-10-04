---
title: FieldCitation
second_title: Aspose.Words per .NET API Reference
description: Implementa il campo CITATION.
type: docs
weight: 1530
url: /it/net/aspose.words.fields/fieldcitation/
---
## FieldCitation class

Implementa il campo CITATION.

```csharp
public class FieldCitation : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldCitation](fieldcitation/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [AnotherSourceTag](../../aspose.words.fields/fieldcitation/anothersourcetag/) { get; set; } | Ottiene o imposta un valore che elabora il **Etichetta** valore dell'elemento di un'altra fonte da includere nella citazione. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [End](../../aspose.words.fields/field/end/) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Ottiene a[`FieldFormat`](../fieldformat/) oggetto che fornisce l'accesso digitato alla formattazione del campo. |
| [FormatLanguageId](../../aspose.words.fields/fieldcitation/formatlanguageid/) { get; set; } | Ottiene o imposta l'ID lingua utilizzato insieme allo stile bibliografico specificato per formattare la citazione nel documento. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolarne il risultato). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [PageNumber](../../aspose.words.fields/fieldcitation/pagenumber/) { get; set; } | Ottiene o imposta un numero di pagina associato alla citazione. |
| [Prefix](../../aspose.words.fields/fieldcitation/prefix/) { get; set; } | Ottiene o imposta un prefisso anteposto alla citazione. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Ottiene o imposta il testo che si trova tra il separatore di campo e la fine del campo. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Ottiene il nodo che rappresenta il separatore di campo. Può essere nullo. |
| [SourceTag](../../aspose.words.fields/fieldcitation/sourcetag/) { get; set; } | Ottiene o imposta un valore che elabora il **Etichetta**valore dell'elemento della sorgente da inserire. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Ottiene il nodo che rappresenta l'inizio del campo. |
| [Suffix](../../aspose.words.fields/fieldcitation/suffix/) { get; set; } | Ottiene o imposta un suffisso che viene aggiunto alla citazione. |
| [SuppressAuthor](../../aspose.words.fields/fieldcitation/suppressauthor/) { get; set; } | Ottiene o imposta se le informazioni sull'autore vengono eliminate dalla citazione. |
| [SuppressTitle](../../aspose.words.fields/fieldcitation/suppresstitle/) { get; set; } | Ottiene o imposta se le informazioni sul titolo vengono eliminate dalla citazione. |
| [SuppressYear](../../aspose.words.fields/fieldcitation/suppressyear/) { get; set; } | Ottiene o imposta se le informazioni sull'anno vengono eliminate dalla citazione. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Ottiene il tipo di campo di Microsoft Word. |
| [VolumeNumber](../../aspose.words.fields/fieldcitation/volumenumber/) { get; set; } | Ottiene o imposta un numero di volume associato alla citazione. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non è presente alcun separatore). Sono inclusi sia il codice campo che il risultato campo dei campi figlio. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è un separatore). |
| [Remove](../../aspose.words.fields/field/remove/)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del suo nodo padre, restituisce il suo paragrafo padre. Se il campo è già stato rimosso, ritorna **nullo** . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Esegue lo scollegamento del campo. |
| [Update](../../aspose.words.fields/field/update/)() | Esegue l'aggiornamento del campo. Genera se il campo è già in fase di aggiornamento. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Esegue un aggiornamento del campo. Genera se il campo è già in fase di aggiornamento. |

### Osservazioni

Inserisce il contenuto del file **Fonte** elemento con un specificato **Etichetta** elemento utilizzando uno stile bibliografico.

### Esempi

Mostra come lavorare con i campi CITAZIONE e BIBLIOGRAFIA.

```csharp
// Apre un documento contenente le fonti bibliografiche in cui possiamo trovare
// Microsoft Word tramite riferimenti -> Citazioni e amp; Bibliografia -> Gestisci le fonti.
Document doc = new Document(MyDir + "Bibliography.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Text to be cited with one source.");

// Crea una citazione con solo il numero di pagina e l'autore del libro di riferimento.
FieldCitation fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);

// Ci riferiamo alle fonti usando i loro nomi di tag.
fieldCitation.SourceTag = "Book1";
fieldCitation.PageNumber = "85";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = true;
fieldCitation.SuppressYear = true;

Assert.AreEqual(" CITATION  Book1 \\p 85 \\t \\y", fieldCitation.GetFieldCode());

// Crea una citazione più dettagliata che citi due fonti.
builder.InsertParagraph();
builder.Write("Text to be cited with two sources.");
fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);
fieldCitation.SourceTag = "Book1";
fieldCitation.AnotherSourceTag = "Book2";
fieldCitation.FormatLanguageId = "en-US";
fieldCitation.PageNumber = "19";
fieldCitation.Prefix = "Prefix ";
fieldCitation.Suffix = " Suffix";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = false;
fieldCitation.SuppressYear = false;
fieldCitation.VolumeNumber = "VII";

Assert.AreEqual(" CITATION  Book1 \\m Book2 \\l en-US \\p 19 \\f \"Prefix \" \\s \" Suffix\" \\v VII", fieldCitation.GetFieldCode());

// Possiamo usare un campo BIBLIOGRAFIA per visualizzare tutte le fonti all'interno del documento.
builder.InsertBreak(BreakType.PageBreak);
FieldBibliography fieldBibliography = (FieldBibliography)builder.InsertField(FieldType.FieldBibliography, true);
fieldBibliography.FormatLanguageId = "1124";

Assert.AreEqual(" BIBLIOGRAPHY  \\l 1124", fieldBibliography.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CITATION.docx");
```

### Guarda anche

* class [Field](../field/)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
