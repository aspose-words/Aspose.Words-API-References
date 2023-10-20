---
title: MailMerge Class
linktitle: MailMerge
articleTitle: MailMerge
second_title: Aspose.Words per .NET
description: Aspose.Words.MailMerging.MailMerge classe. Rappresenta la funzionalità di stampa unione in C#.
type: docs
weight: 3840
url: /it/net/aspose.words.mailmerging/mailmerge/
---
## MailMerge class

Rappresenta la funzionalità di stampa unione.

Per saperne di più, visita il[Stampa unione e reporting](https://docs.aspose.com/words/net/mail-merge-and-reporting/) articolo di documentazione.

```csharp
public class MailMerge
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [CleanupOptions](../../aspose.words.mailmerging/mailmerge/cleanupoptions/) { get; set; } | Ottiene o imposta un set di flag che specificano quali elementi devono essere rimossi durante la stampa unione. |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/) { get; set; } | Ottiene o imposta un valore che indica se i paragrafi con segni di punteggiatura sono considerati vuoti e devono essere rimossi seRemoveEmptyParagraphs l'opzione è specificata. |
| [FieldMergingCallback](../../aspose.words.mailmerging/mailmerge/fieldmergingcallback/) { get; set; } | Si verifica durante la stampa unione quando nel documento viene rilevato un campo di stampa unione. |
| [MailMergeCallback](../../aspose.words.mailmerging/mailmerge/mailmergecallback/) { get; set; } | Permette di gestire eventi particolari durante la stampa in serie. |
| [MappedDataFields](../../aspose.words.mailmerging/mailmerge/mappeddatafields/) { get; } | Restituisce una raccolta che rappresenta i campi dati mappati per l'operazione di stampa unione. |
| [MergeDuplicateRegions](../../aspose.words.mailmerging/mailmerge/mergeduplicateregions/) { get; set; } | Ottiene o imposta un valore che indica se tutte le aree di stampa unione del documento con il nome di un'origine dati devono essere unite durante l'esecuzione di una stampa unione con aree rispetto all'origine dati o solo la prima. |
| [MergeWholeDocument](../../aspose.words.mailmerging/mailmerge/mergewholedocument/) { get; set; } | Ottiene o imposta un valore che indica se i campi nell'intero documento vengono aggiornati durante l'esecuzione di una stampa unione con regioni. |
| [PreserveUnusedTags](../../aspose.words.mailmerging/mailmerge/preserveunusedtags/) { get; set; } | Ottiene o imposta un valore che indica se i tag "mustache" non utilizzati devono essere conservati. |
| [RegionEndTag](../../aspose.words.mailmerging/mailmerge/regionendtag/) { get; set; } | Ottiene o imposta un tag di fine della regione di stampa unione. |
| [RegionStartTag](../../aspose.words.mailmerging/mailmerge/regionstarttag/) { get; set; } | Ottiene o imposta un tag iniziale della regione di stampa unione. |
| [RestartListsAtEachSection](../../aspose.words.mailmerging/mailmerge/restartlistsateachsection/) { get; set; } | Ottiene o imposta un valore che indica se gli elenchi vengono riavviati in ciascuna sezione dopo l'esecuzione di una stampa unione. |
| [RetainFirstSectionStart](../../aspose.words.mailmerging/mailmerge/retainfirstsectionstart/) { get; set; } | Ottiene o imposta un valore che indica se il[`SectionStart`](../../aspose.words/pagesetup/sectionstart/) della prima sezione del documento e le sue copie per le successive righe dell'origine dati vengono conservate durante la stampa unione o aggiornate in base al comportamento di MS Word. |
| [TrimWhitespaces](../../aspose.words.mailmerging/mailmerge/trimwhitespaces/) { get; set; } | Ottiene o imposta un valore che indica se gli spazi finali e iniziali vengono eliminati dai valori di stampa unione. |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/) { get; set; } | Ottiene o imposta un valore che indica se i campi e le aree di unione vengono uniti indipendentemente dalla condizione del campo IF padre. |
| [UseNonMergeFields](../../aspose.words.mailmerging/mailmerge/usenonmergefields/) { get; set; } | Quando`VERO` , specifica che oltre ai campi MERGEFIELD, la stampa unione viene eseguita in alcuni altri tipi di campi e anche nei tag "{{fieldName}}". |
| [UseWholeParagraphAsRegion](../../aspose.words.mailmerging/mailmerge/usewholeparagraphasregion/) { get; set; } | Ottiene o imposta un valore che indica se è presente l'intero paragrafo**Inizio tabella** O**Fine tabella** field o un intervallo particolare compreso tra**Inizio tabella** E**Fine tabella** i campi devono essere inclusi nella regione della stampa unione. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [DeleteFields](../../aspose.words.mailmerging/mailmerge/deletefields/)() | Rimuove i campi relativi alla stampa unione dal documento. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_1)(*DataRow*) | Esegue la stampa unione da a**DataRow** nel documento. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_2)(*DataTable*) | Esegue la stampa unione da un DataTable nel documento. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_3)(*DataView*) | Esegue la stampa unione da a**DataView** nel documento. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_4)(*IDataReader*) | Esegue la stampa unione da**IDataReader** nel documento. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute)(*[IMailMergeDataSource](../imailmergedatasource/)*) | Esegue una stampa unione da un'origine dati personalizzata. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_5)(*string[], object[]*) | Esegue un'operazione di stampa unione per un singolo record. |
| [ExecuteADO](../../aspose.words.mailmerging/mailmerge/executeado/)(*object*) | Esegue la stampa unione da un oggetto ADO Recordset nel documento. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_2)(*DataSet*) | Esegue la stampa unione da a**Set di dati** in un documento con regioni di stampa unione. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_3)(*DataTable*) | Esegue la stampa unione da a**Tabella dati** nel documento con regioni di stampa unione. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_4)(*DataView*) | Esegue la stampa unione da a**DataView** nel documento con regioni di stampa unione. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions)(*[IMailMergeDataSource](../imailmergedatasource/)*) | Esegue una stampa unione da un'origine dati personalizzata con aree di stampa unione. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_1)(*[IMailMergeDataSourceRoot](../imailmergedatasourceroot/)*) | Esegue una stampa unione da un'origine dati personalizzata con aree di stampa unione. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_5)(*IDataReader, string*) | Esegue la stampa unione da**IDataReader** nel documento con regioni di stampa unione. |
| [ExecuteWithRegionsADO](../../aspose.words.mailmerging/mailmerge/executewithregionsado/)(*object, string*) | Esegue la stampa unione da un oggetto ADO Recordset nel documento con aree di stampa unione. |
| [GetFieldNames](../../aspose.words.mailmerging/mailmerge/getfieldnames/)() | Restituisce una raccolta di nomi di campi di stampa unione disponibili nel documento. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion)(*string*) | Restituisce una raccolta di nomi di campi di stampa unione disponibili nella regione. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion_1)(*string, int*) | Restituisce una raccolta di nomi di campi di stampa unione disponibili nella regione. |
| [GetRegionsByName](../../aspose.words.mailmerging/mailmerge/getregionsbyname/)(*string*) | Restituisce una raccolta di regioni di stampa unione con il nome specificato. |
| [GetRegionsHierarchy](../../aspose.words.mailmerging/mailmerge/getregionshierarchy/)() | Restituisce una gerarchia completa di regioni (con campi) disponibili nel documento. |

## Osservazioni

Affinché l'operazione di stampa unione funzioni, il documento deve contenere Word MERGEFIELD e facoltativamente campi NEXT. Durante l'operazione di stampa unione, i campi di unione nel documento vengono sostituiti con i valori dell'origine dati.

Esistono due modi distinti per utilizzare la stampa unione: con aree di stampa unione e senza.

La stampa unione più semplice è senza aree ed è molto simile al funzionamento della stampa unione in Word. UtilizzoEseguire metodi per unire le informazioni da alcune origini dati come**Tabella dati** ,**Set di dati** ,**DataView** ,**IDataReader** o una serie di oggetti nel tuo documento. The `MailMerge` L'oggetto elabora tutti i record dell'origine dati e copia e aggiunge il contenuto dell'intero documento per ciascun record.

Tieni presente che quando`MailMerge` L'oggetto incontra un campo NEXT, seleziona il successivo record nell'origine dati e continua l'unione senza copiare alcun contenuto.

Utilizzo[`ExecuteWithRegions`](./executewithregions/) e altri sovraccarichi per unire le informazioni in un documento con le regioni di stampa unione definite. Puoi usare **Set di dati** ,**Tabella dati** ,**DataView** O**IDataReader** come origini dati per questa operazione.

È necessario utilizzare le regioni di stampa unione se si desidera aumentare dinamicamente le porzioni all'interno del documento . Senza le regioni di stampa unione, l'intero documento verrà ripetuto per ogni record dell' origine dati.

## Esempi

Mostra come eseguire una stampa unione con i dati di un DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Di seguito sono riportati due modi per utilizzare DataTable come origine dati per una stampa unione.
    // 1 - Utilizza l'intera tabella per la stampa unione per creare un documento di stampa unione di output per ogni riga nella tabella:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Utilizza una riga della tabella per creare un documento di stampa unione di output:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Crea un documento di origine per la stampa unione.
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### Guarda anche

* spazio dei nomi [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* assemblea [Aspose.Words](../../)
