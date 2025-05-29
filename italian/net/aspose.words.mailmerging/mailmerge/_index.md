---
title: MailMerge Class
linktitle: MailMerge
articleTitle: MailMerge
second_title: Aspose.Words per .NET
description: Sblocca potenti funzionalità di stampa unione con la classe Aspose.Words.MailMerging.MailMerge. Semplifica la creazione di documenti e aumenta la produttività senza sforzo!
type: docs
weight: 4530
url: /it/net/aspose.words.mailmerging/mailmerge/
---
## MailMerge class

Rappresenta la funzionalità di unione di posta.

Per saperne di più, visita il[Unione di posta e creazione di report](https://docs.aspose.com/words/net/mail-merge-and-reporting/) articolo di documentazione.

```csharp
public class MailMerge
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [CleanupOptions](../../aspose.words.mailmerging/mailmerge/cleanupoptions/) { get; set; } | Ottiene o imposta un set di flag che specificano quali elementi devono essere rimossi durante la stampa unione. |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/) { get; set; } | Ottiene o imposta un valore che indica se i paragrafi con segni di punteggiatura sono considerati vuoti e dovrebbero essere rimossi seRemoveEmptyParagraphs l'opzione è specificata. |
| [FieldMergingCallback](../../aspose.words.mailmerging/mailmerge/fieldmergingcallback/) { get; set; } | Si verifica durante la stampa unione quando nel documento viene rilevato un campo di stampa unione. |
| [MailMergeCallback](../../aspose.words.mailmerging/mailmerge/mailmergecallback/) { get; set; } | Consente di gestire eventi particolari durante la stampa unione. |
| [MappedDataFields](../../aspose.words.mailmerging/mailmerge/mappeddatafields/) { get; } | Restituisce una raccolta che rappresenta i campi dati mappati per l'operazione di unione di posta. |
| [MergeDuplicateRegions](../../aspose.words.mailmerging/mailmerge/mergeduplicateregions/) { get; set; } | Ottiene o imposta un valore che indica se tutte le aree di unione di documenti con il nome di un'origine dati devono essere unite durante l'esecuzione di un'unione di documenti con aree relative all'origine dati o solo la prima. |
| [MergeWholeDocument](../../aspose.words.mailmerging/mailmerge/mergewholedocument/) { get; set; } | Ottiene o imposta un valore che indica se i campi dell'intero documento vengono aggiornati durante l'esecuzione di una stampa unione con regioni. |
| [PreserveUnusedTags](../../aspose.words.mailmerging/mailmerge/preserveunusedtags/) { get; set; } | Ottiene o imposta un valore che indica se i tag "baffi" non utilizzati devono essere conservati. |
| [RegionEndTag](../../aspose.words.mailmerging/mailmerge/regionendtag/) { get; set; } | Ottiene o imposta un tag di fine regione di unione di posta. |
| [RegionStartTag](../../aspose.words.mailmerging/mailmerge/regionstarttag/) { get; set; } | Ottiene o imposta un tag di inizio regione di unione di posta. |
| [RestartListsAtEachSection](../../aspose.words.mailmerging/mailmerge/restartlistsateachsection/) { get; set; } | Ottiene o imposta un valore che indica se gli elenchi vengono riavviati a ogni sezione dopo l'esecuzione di una stampa unione. |
| [RetainFirstSectionStart](../../aspose.words.mailmerging/mailmerge/retainfirstsectionstart/) { get; set; } | Ottiene o imposta un valore che indica se il[`SectionStart`](../../aspose.words/pagesetup/sectionstart/) della prima sezione del documento e le sue copie per le righe successive della sorgente dati vengono conservate durante la stampa unione o aggiornate in base al comportamento di MS Word. |
| [TrimWhitespaces](../../aspose.words.mailmerging/mailmerge/trimwhitespaces/) { get; set; } | Ottiene o imposta un valore che indica se gli spazi vuoti iniziali e finali vengono tagliati dai valori di unione di posta. |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/) { get; set; } | Ottiene o imposta un valore che indica se i campi di unione e le regioni di unione vengono uniti indipendentemente dalla condizione del campo IF padre. |
| [UseNonMergeFields](../../aspose.words.mailmerging/mailmerge/usenonmergefields/) { get; set; } | Quando`VERO` , specifica che oltre ai campi MERGEFIELD, la stampa unione viene eseguita in alcuni altri tipi di campi e anche nei tag "{{fieldName}}". |
| [UseWholeParagraphAsRegion](../../aspose.words.mailmerging/mailmerge/usewholeparagraphasregion/) { get; set; } | Ottiene o imposta un valore che indica se l'intero paragrafo con**TableStart** O**TableEnd** field o intervallo particolare tra**TableStart** E**TableEnd** i campi dovrebbero essere inclusi nell'area di unione della stampa. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [DeleteFields](../../aspose.words.mailmerging/mailmerge/deletefields/)() | Rimuove i campi relativi alla stampa unione dal documento. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_1)(*DataRow*) | Esegue la stampa unione da un**Riga di dati** nel documento. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_2)(*DataTable*) | Esegue la stampa unione da una tabella dati nel documento. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_3)(*DataView*) | Esegue la stampa unione da un**Visualizzazione dati** nel documento. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_4)(*IDataReader*) | Esegue la stampa unione da**Lettore di dati IData** nel documento. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute)(*[IMailMergeDataSource](../imailmergedatasource/)*) | Esegue una stampa unione da una fonte dati personalizzata. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_5)(*string[], object[]*) | Esegue un'operazione di unione di posta per un singolo record. |
| [ExecuteADO](../../aspose.words.mailmerging/mailmerge/executeado/)(*object*) | Esegue la stampa unione da un oggetto ADO Recordset nel documento. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_2)(*DataSet*) | Esegue la stampa unione da un**Insieme di dati** in un documento con aree di unione di stampa. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_3)(*DataTable*) | Esegue la stampa unione da un**Tabella dati** nel documento con aree di unione. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_4)(*DataView*) | Esegue la stampa unione da un**Visualizzazione dati** nel documento con aree di unione. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions)(*[IMailMergeDataSource](../imailmergedatasource/)*) | Esegue una stampa unione da un'origine dati personalizzata con regioni di stampa unione. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_1)(*[IMailMergeDataSourceRoot](../imailmergedatasourceroot/)*) | Esegue una stampa unione da un'origine dati personalizzata con regioni di stampa unione. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_5)(*IDataReader, string*) | Esegue la stampa unione da**Lettore di dati IData** nel documento con aree di unione. |
| [ExecuteWithRegionsADO](../../aspose.words.mailmerging/mailmerge/executewithregionsado/)(*object, string*) | Esegue la stampa unione da un oggetto ADO Recordset nel documento con aree di stampa unione. |
| [GetFieldNames](../../aspose.words.mailmerging/mailmerge/getfieldnames/)() | Restituisce una raccolta di nomi di campi di unione di posta disponibili nel documento. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion)(*string*) | Restituisce una raccolta di nomi di campi di unione di posta disponibili nella regione. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion_1)(*string, int*) | Restituisce una raccolta di nomi di campi di unione di posta disponibili nella regione. |
| [GetRegionsByName](../../aspose.words.mailmerging/mailmerge/getregionsbyname/)(*string*) | Restituisce una raccolta di aree di unione di stampa con il nome specificato. |
| [GetRegionsHierarchy](../../aspose.words.mailmerging/mailmerge/getregionshierarchy/)() | Restituisce una gerarchia completa delle regioni (con campi) disponibili nel documento. |

## Osservazioni

Affinché l'operazione di stampa unione funzioni, il documento deve contenere i campi MERGEFIELD e (opzionale) di Word. Durante l'operazione di stampa unione, i campi unione nel documento vengono sostituiti con i valori provenienti dall'origine dati.

Esistono due modi distinti per utilizzare la stampa unione: con le aree di stampa unione e senza.

La stampa unione più semplice è senza regioni ed è molto simile al funzionamento di stampa unione in Word. UsaEseguire metodi per unire informazioni da una sorgente dati some come**Tabella dati** ,**Insieme di dati** ,**Visualizzazione dati** ,**Lettore di dati IData** o un array di oggetti nel tuo documento. The `MailMerge` L'oggetto elabora tutti i record dell'origine dati e copia e aggiunge il contenuto dell'intero documento per ciascun record.

Nota che quando`MailMerge`l'oggetto incontra un campo NEXT, seleziona il record successivo record nell'origine dati e continua l'unione senza copiare alcun contenuto.

Utilizzo[`ExecuteWithRegions`](./executewithregions/) e altri sovraccarichi per unire le informazioni in un documento con aree di stampa unione definite. Puoi usare **Insieme di dati** ,**Tabella dati** ,**Visualizzazione dati** O**Lettore di dati IData** come origini dati per questa operazione.

È necessario utilizzare le aree di stampa unione se si desidera espandere dinamicamente le porzioni all'interno del documento . Senza le aree di stampa unione, l'intero documento verrà ripetuto per ogni record di , l'origine dati.

## Esempi

Mostra come eseguire una stampa unione con i dati di una DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Di seguito sono riportati due modi per utilizzare una DataTable come origine dati per una stampa unione.
    // 1 - Utilizza l'intera tabella per la stampa unione per creare un documento di stampa unione in output per ogni riga della tabella:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Utilizzare una riga della tabella per creare un documento di stampa unione in output:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Crea un documento sorgente per la stampa unione.
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
