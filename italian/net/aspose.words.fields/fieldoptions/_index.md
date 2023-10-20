---
title: FieldOptions Class
linktitle: FieldOptions
articleTitle: FieldOptions
second_title: Aspose.Words per .NET
description: Aspose.Words.Fields.FieldOptions classe. Rappresenta le opzioni per controllare la gestione dei campi in un documento in C#.
type: docs
weight: 2250
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
| [BibliographyStylesProvider](../../aspose.words.fields/fieldoptions/bibliographystylesprovider/) { get; set; } | Ottiene o imposta un provider che restituisce uno stile bibliografico per il[`FieldBibliography`](../fieldbibliography/) E[`FieldCitation`](../fieldcitation/) campi. |
| [BuiltInTemplatesPaths](../../aspose.words.fields/fieldoptions/builtintemplatespaths/) { get; set; } | Ottiene o imposta i percorsi dei modelli incorporati di MS Word. |
| [ComparisonExpressionEvaluator](../../aspose.words.fields/fieldoptions/comparisonexpressionevaluator/) { get; set; } | Ottiene o imposta il valutatore delle espressioni di confronto dei campi. |
| [CurrentUser](../../aspose.words.fields/fieldoptions/currentuser/) { get; set; } | Ottiene o imposta le informazioni sull'utente corrente. |
| [CustomTocStyleSeparator](../../aspose.words.fields/fieldoptions/customtocstyleseparator/) { get; set; } | Ottiene o imposta il separatore di stile personalizzato per l'opzione \t[`FieldToc`](../fieldtoc/) campo. |
| [DefaultDocumentAuthor](../../aspose.words.fields/fieldoptions/defaultdocumentauthor/) { get; set; } | Ottiene o imposta il nome dell'autore del documento predefinito. Se il nome dell'autore è già specificato nelle proprietà integrate del documento, questa opzione non viene considerata. |
| [FieldDatabaseProvider](../../aspose.words.fields/fieldoptions/fielddatabaseprovider/) { get; set; } | Ottiene o imposta un provider che restituisce un risultato della query per[`FieldDatabase`](../fielddatabase/) campo. |
| [FieldIndexFormat](../../aspose.words.fields/fieldoptions/fieldindexformat/) { get; set; } | Ottiene o imposta a[`FieldIndexFormat`](./fieldindexformat/) che rappresenta la formattazione per il[`FieldIndex`](../fieldindex/) campi nel documento. |
| [FieldUpdateCultureProvider](../../aspose.words.fields/fieldoptions/fieldupdatecultureprovider/) { get; set; } | Ottiene o imposta un provider che restituisce un oggetto cultura specifico per ogni campo particolare. |
| [FieldUpdateCultureSource](../../aspose.words.fields/fieldoptions/fieldupdateculturesource/) { get; set; } | Specifica le impostazioni cultura da utilizzare per formattare il risultato del campo. |
| [FieldUpdatingCallback](../../aspose.words.fields/fieldoptions/fieldupdatingcallback/) { get; set; } | Ottiene o imposta[`IFieldUpdatingCallback`](../ifieldupdatingcallback/) implementazione |
| [FieldUpdatingProgressCallback](../../aspose.words.fields/fieldoptions/fieldupdatingprogresscallback/) { get; set; } | Ottiene o imposta[`IFieldUpdatingProgressCallback`](../ifieldupdatingprogresscallback/) implementazione. |
| [FileName](../../aspose.words.fields/fieldoptions/filename/) { get; set; } | Ottiene o imposta il nome del file del documento. |
| [IsBidiTextSupportedOnUpdate](../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) { get; set; } | Ottiene o imposta il valore che indica se il testo bidirezionale è completamente supportato durante l'aggiornamento del campo o meno. |
| [LegacyNumberFormat](../../aspose.words.fields/fieldoptions/legacynumberformat/) { get; set; } | Ottiene o imposta il valore che indica se il formato numerico legacy (prima di AW 13.10) per i campi è abilitato o meno. |
| [PreProcessCulture](../../aspose.words.fields/fieldoptions/preprocessculture/) { get; set; } | Ottiene o imposta le impostazioni cultura per preelaborare i valori dei campi. |
| [ResultFormatter](../../aspose.words.fields/fieldoptions/resultformatter/) { get; set; } | Permette di controllare come viene formattato il risultato del campo. |
| [TemplateName](../../aspose.words.fields/fieldoptions/templatename/) { get; set; } | Ottiene o imposta il nome del file del modello utilizzato dal documento. |
| [ToaCategories](../../aspose.words.fields/fieldoptions/toacategories/) { get; set; } | Ottiene o imposta la tabella delle categorie delle autorità. |
| [UseInvariantCultureNumberFormat](../../aspose.words.fields/fieldoptions/useinvariantculturenumberformat/) { get; set; } | Ottiene o imposta il valore che indica che il formato numerico viene analizzato utilizzando impostazioni cultura invarianti o not |
| [UserPromptRespondent](../../aspose.words.fields/fieldoptions/userpromptrespondent/) { get; set; } | Ottiene o imposta l'intervistato per le richieste dell'utente durante l'aggiornamento del campo. |

## Esempi

Mostra come specificare l'origine delle impostazioni cultura utilizzate per la formattazione della data durante un aggiornamento di campo o una stampa unione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci due campi di unione con la locale tedesca.
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// Imposta la lingua corrente sull'inglese americano dopo aver preservato il valore originale in una variabile.
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// Questa unione utilizzerà la lingua del thread corrente per formattare la data, inglese americano.
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// Configura la successiva unione per ricavare il valore della lingua dal codice di campo. Il valore di quella cultura sarà tedesco.
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// Il primo risultato dell'unione contiene una data formattata in inglese, mentre il secondo è in tedesco.
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// Ripristina la lingua originale del thread.
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
