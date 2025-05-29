---
title: FieldOptions Class
linktitle: FieldOptions
articleTitle: FieldOptions
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Fields.FieldOptions per ottimizzare la gestione dei campi nei documenti, migliorando il flusso di lavoro e l'efficienza della gestione dei documenti.
type: docs
weight: 2660
url: /it/net/aspose.words.fields/fieldoptions/
---
## FieldOptions class

Rappresenta le opzioni per controllare la gestione dei campi in un documento.

Per saperne di più, visita il[Lavorare con i campi](https://docs.aspose.com/words/net/working-with-fields/) articolo di documentazione.

```csharp
public sealed class FieldOptions
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BarcodeGenerator](../../aspose.words.fields/fieldoptions/barcodegenerator/) { get; set; } | Ottiene o imposta il generatore di codici a barre personalizzato. |
| [BibliographyStylesProvider](../../aspose.words.fields/fieldoptions/bibliographystylesprovider/) { get; set; } | Ottiene o imposta un provider che restituisce uno stile bibliografico per [`FieldBibliography`](../fieldbibliography/) E[`FieldCitation`](../fieldcitation/) campi. |
| [BuiltInTemplatesPaths](../../aspose.words.fields/fieldoptions/builtintemplatespaths/) { get; set; } | Ottiene o imposta i percorsi dei modelli incorporati di MS Word. |
| [ComparisonExpressionEvaluator](../../aspose.words.fields/fieldoptions/comparisonexpressionevaluator/) { get; set; } | Ottiene o imposta il valutatore delle espressioni di confronto dei campi. |
| [CurrentUser](../../aspose.words.fields/fieldoptions/currentuser/) { get; set; } | Ottiene o imposta le informazioni correnti dell'utente. |
| [CustomTocStyleSeparator](../../aspose.words.fields/fieldoptions/customtocstyleseparator/) { get; set; } | Ottiene o imposta il separatore di stile personalizzato per l'opzione \t in[`FieldToc`](../fieldtoc/) campo. |
| [DefaultDocumentAuthor](../../aspose.words.fields/fieldoptions/defaultdocumentauthor/) { get; set; } | Ottiene o imposta il nome predefinito dell'autore del documento. Se il nome dell'autore è già specificato nelle proprietà predefinite del documento, questa opzione non viene considerata. |
| [FieldDatabaseProvider](../../aspose.words.fields/fieldoptions/fielddatabaseprovider/) { get; set; } | Ottiene o imposta un provider che restituisce un risultato di query per[`FieldDatabase`](../fielddatabase/) campo. |
| [FieldIndexFormat](../../aspose.words.fields/fieldoptions/fieldindexformat/) { get; set; } | Ottiene o imposta un[`FieldIndexFormat`](./fieldindexformat/) che rappresenta la formattazione per il[`FieldIndex`](../fieldindex/) campi nel documento. |
| [FieldUpdateCultureProvider](../../aspose.words.fields/fieldoptions/fieldupdatecultureprovider/) { get; set; } | Ottiene o imposta un provider che restituisce un oggetto cultura specifico per ogni campo particolare. |
| [FieldUpdateCultureSource](../../aspose.words.fields/fieldoptions/fieldupdateculturesource/) { get; set; } | Specifica quale cultura utilizzare per formattare il risultato del campo. |
| [FieldUpdatingCallback](../../aspose.words.fields/fieldoptions/fieldupdatingcallback/) { get; set; } | Ottiene o imposta[`IFieldUpdatingCallback`](../ifieldupdatingcallback/) implementazione |
| [FieldUpdatingProgressCallback](../../aspose.words.fields/fieldoptions/fieldupdatingprogresscallback/) { get; set; } | Ottiene o imposta[`IFieldUpdatingProgressCallback`](../ifieldupdatingprogresscallback/) implementazione. |
| [FileName](../../aspose.words.fields/fieldoptions/filename/) { get; set; } | Ottiene o imposta il nome del file del documento. |
| [IsBidiTextSupportedOnUpdate](../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) { get; set; } | Ottiene o imposta il valore che indica se il testo bidirezionale è completamente supportato durante l'aggiornamento del campo o meno. |
| [LegacyNumberFormat](../../aspose.words.fields/fieldoptions/legacynumberformat/) { get; set; } | Ottiene o imposta il valore che indica se il formato numerico legacy (precedente ad AW 13.10) per i campi è abilitato o meno. |
| [PreProcessCulture](../../aspose.words.fields/fieldoptions/preprocessculture/) { get; set; } | Ottiene o imposta la cultura per preelaborare i valori dei campi. |
| [ResultFormatter](../../aspose.words.fields/fieldoptions/resultformatter/) { get; set; } | Consente di controllare come viene formattato il risultato del campo. |
| [TemplateName](../../aspose.words.fields/fieldoptions/templatename/) { get; set; } | Ottiene o imposta il nome del file del modello utilizzato dal documento. |
| [ToaCategories](../../aspose.words.fields/fieldoptions/toacategories/) { get; set; } | Ottiene o imposta la tabella delle categorie delle autorità. |
| [UseInvariantCultureNumberFormat](../../aspose.words.fields/fieldoptions/useinvariantculturenumberformat/) { get; set; } | Ottiene o imposta il valore che indica che il formato numerico viene analizzato utilizzando la cultura invariante o meno |
| [UserPromptRespondent](../../aspose.words.fields/fieldoptions/userpromptrespondent/) { get; set; } | Ottiene o imposta il rispondente per le richieste utente durante l'aggiornamento del campo. |

## Esempi

Mostra come specificare l'origine della cultura utilizzata per la formattazione della data durante un aggiornamento di campo o una stampa unione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserire due campi di unione con impostazioni locali tedesche.
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// Imposta la cultura corrente su inglese americano dopo aver preservato il valore originale in una variabile.
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// Questa unione utilizzerà la cultura del thread corrente per formattare la data, inglese (Stati Uniti).
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// Configura la prossima unione in modo che il valore della lingua di destinazione derivi dal codice di campo. Il valore di quella lingua sarà tedesco.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// Il primo risultato della fusione contiene una data formattata in inglese, mentre il secondo è in tedesco.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// Ripristina la cultura originale del thread.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
