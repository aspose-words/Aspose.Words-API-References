---
title: FieldStyleRef
second_title: Aspose.Words per .NET API Reference
description: Implementa il campo STYLEREF.
type: docs
weight: 2290
url: /it/net/aspose.words.fields/fieldstyleref/
---
## FieldStyleRef class

Implementa il campo STYLEREF.

```csharp
public class FieldStyleRef : Field
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [FieldStyleRef](fieldstyleref)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | Ottiene il testo che rappresenta il risultato del campo visualizzato. |
| [End](../../aspose.words.fields/field/end) { get; } | Ottiene il nodo che rappresenta la fine del campo. |
| [Format](../../aspose.words.fields/field/format) { get; } | Ottiene a[`FieldFormat`](../fieldformat) oggetto che fornisce l'accesso digitato alla formattazione del campo. |
| [InsertParagraphNumber](../../aspose.words.fields/fieldstyleref/insertparagraphnumber) { get; set; } | Ottiene o imposta se inserire il numero di paragrafo del paragrafo di riferimento esattamente come appare nel documento. |
| [InsertParagraphNumberInFullContext](../../aspose.words.fields/fieldstyleref/insertparagraphnumberinfullcontext) { get; set; } | Ottiene o imposta se inserire il numero di paragrafo del paragrafo di riferimento nel contesto completo. |
| [InsertParagraphNumberInRelativeContext](../../aspose.words.fields/fieldstyleref/insertparagraphnumberinrelativecontext) { get; set; } | Ottiene o imposta se inserire il numero di paragrafo del paragrafo di riferimento nel contesto relativo. |
| [InsertRelativePosition](../../aspose.words.fields/fieldstyleref/insertrelativeposition) { get; set; } | Ottiene o imposta se inserire la posizione relativa del paragrafo di riferimento. |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | Ottiene o imposta se il campo è bloccato (non dovrebbe ricalcolarne il risultato). |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | Ottiene o imposta l'LCID del campo. |
| [Result](../../aspose.words.fields/field/result) { get; set; } | Ottiene o imposta il testo che si trova tra il separatore di campo e la fine del campo. |
| [SearchFromBottom](../../aspose.words.fields/fieldstyleref/searchfrombottom) { get; set; } | Ottiene o imposta se eseguire la ricerca dalla parte inferiore della pagina corrente, anziché dall'alto. |
| [Separator](../../aspose.words.fields/field/separator) { get; } | Ottiene il nodo che rappresenta il separatore di campo. Può essere nullo. |
| [Start](../../aspose.words.fields/field/start) { get; } | Ottiene il nodo che rappresenta l'inizio del campo. |
| [StyleName](../../aspose.words.fields/fieldstyleref/stylename) { get; set; } | Ottiene o imposta il nome dello stile in base al quale è formattato il testo da cercare. |
| [SuppressNonDelimiters](../../aspose.words.fields/fieldstyleref/suppressnondelimiters) { get; set; } | Ottiene o imposta se eliminare i caratteri non delimitatori. |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | Ottiene il tipo di campo di Microsoft Word. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non è presente alcun separatore). Sono inclusi sia il codice campo che il risultato campo dei campi figlio. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | Restituisce il testo tra l'inizio del campo e il separatore di campo (o la fine del campo se non c'è un separatore). |
| [Remove](../../aspose.words.fields/field/remove)() | Rimuove il campo dal documento. Restituisce un nodo subito dopo il campo. Se la fine del campo è l'ultimo figlio del suo nodo padre, restituisce il suo paragrafo padre. Se il campo è già stato rimosso, ritorna **nullo** . |
| [Unlink](../../aspose.words.fields/field/unlink)() | Esegue lo scollegamento del campo. |
| [Update](../../aspose.words.fields/field/update)() | Esegue l'aggiornamento del campo. Genera se il campo è già in fase di aggiornamento. |
| [Update](../../aspose.words.fields/field/update)(bool) | Esegue un aggiornamento del campo. Genera se il campo è già in fase di aggiornamento. |

### Osservazioni

STYLEREF viene utilizzato per fare riferimento a un frammento di testo all'interno del documento formattato con lo stile specificato.

### Esempi

Mostra come utilizzare i campi STYLEREF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un elenco basato su un modello di elenco di Microsoft Word.
Aspose.Words.Lists.List list = doc.Lists.Add(Aspose.Words.Lists.ListTemplate.NumberDefault);

// Questo elenco generato visualizzerà "1.a )".
 // Lo spazio prima della parentesi è un carattere non delimitatore, che possiamo sopprimere.
list.ListLevels[0].NumberFormat = "\x0000.";
list.ListLevels[1].NumberFormat = "\x0001 )";

// Aggiungi testo e applica stili di paragrafo a cui faranno riferimento i campi STYLEREF.
builder.ListFormat.List = list;
builder.ListFormat.ListIndent();
builder.ParagraphFormat.Style = doc.Styles["List Paragraph"];
builder.Writeln("Item 1");
builder.ParagraphFormat.Style = doc.Styles["Quote"];
builder.Writeln("Item 2");
builder.ParagraphFormat.Style = doc.Styles["List Paragraph"];
builder.Writeln("Item 3");
builder.ListFormat.RemoveNumbers();
builder.ParagraphFormat.Style = doc.Styles["Normal"];

// Inserisci un campo STYLEREF nell'intestazione e visualizza il primo testo in stile "Paragrafo elenco" nel documento.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
FieldStyleRef field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";

// Inserisci un campo STYLEREF nel piè di pagina e visualizza l'ultimo testo.
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "List Paragraph";
field.SearchFromBottom = true;

builder.MoveToDocumentEnd();

// Possiamo anche usare i campi STYLEREF per fare riferimento ai numeri degli elenchi di elenchi.
builder.Write("\nParagraph number: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumber = true;

builder.Write("\nParagraph number, relative context: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInRelativeContext = true;

builder.Write("\nParagraph number, full context: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInFullContext = true;

builder.Write("\nParagraph number, full context, non-delimiter chars suppressed: ");
field = (FieldStyleRef)builder.InsertField(FieldType.FieldStyleRef, true);
field.StyleName = "Quote";
field.InsertParagraphNumberInFullContext = true;
field.SuppressNonDelimiters = true;

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.STYLEREF.docx");
```

### Guarda anche

* class [Field](../field)
* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
