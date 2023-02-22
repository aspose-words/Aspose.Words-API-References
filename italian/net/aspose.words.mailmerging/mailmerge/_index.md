---
title: Class MailMerge
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.MailMerging.MailMerge classe. Rappresenta la funzionalità di stampa unione.
type: docs
weight: 3620
url: /it/net/aspose.words.mailmerging/mailmerge/
---
## MailMerge class

Rappresenta la funzionalità di stampa unione.

```csharp
public class MailMerge
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [CleanupOptions](../../aspose.words.mailmerging/mailmerge/cleanupoptions/) { get; set; } | Ottiene o imposta una serie di flag che specificano quali elementi devono essere rimossi durante la stampa unione. |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/) { get; set; } | Ottiene o imposta un valore che indica se i paragrafi con segni di punteggiatura sono considerati vuoti e devono essere rimossi se ilRemoveEmptyParagraphs l'opzione è specificata. |
| [FieldMergingCallback](../../aspose.words.mailmerging/mailmerge/fieldmergingcallback/) { get; set; } | Si verifica durante la stampa unione quando viene rilevato un campo di stampa unione nel documento. |
| [MailMergeCallback](../../aspose.words.mailmerging/mailmerge/mailmergecallback/) { get; set; } | Consente di gestire eventi particolari durante la stampa unione. |
| [MappedDataFields](../../aspose.words.mailmerging/mailmerge/mappeddatafields/) { get; } | Restituisce una raccolta che rappresenta i campi di dati mappati per l'operazione di stampa unione. |
| [MergeDuplicateRegions](../../aspose.words.mailmerging/mailmerge/mergeduplicateregions/) { get; set; } | Ottiene o imposta un valore che indica se tutte le aree di stampa unione documenti con il nome di un'origine dati devono essere unite durante l'esecuzione di una stampa unione con aree rispetto all'origine dati o solo la prima. |
| [MergeWholeDocument](../../aspose.words.mailmerging/mailmerge/mergewholedocument/) { get; set; } | Ottiene o imposta un valore che indica se i campi dell'intero documento vengono aggiornati durante l'esecuzione di una stampa unione con le regioni. |
| [PreserveUnusedTags](../../aspose.words.mailmerging/mailmerge/preserveunusedtags/) { get; set; } | Ottiene o imposta un valore che indica se i tag "baffi" non utilizzati devono essere conservati. |
| [RegionEndTag](../../aspose.words.mailmerging/mailmerge/regionendtag/) { get; set; } | Ottiene o imposta un tag di fine regione per la stampa unione. |
| [RegionStartTag](../../aspose.words.mailmerging/mailmerge/regionstarttag/) { get; set; } | Ottiene o imposta un tag di inizio della regione di stampa unione. |
| [RestartListsAtEachSection](../../aspose.words.mailmerging/mailmerge/restartlistsateachsection/) { get; set; } | Ottiene o imposta un valore che indica se gli elenchi vengono riavviati in ciascuna sezione dopo l'esecuzione di una stampa unione. |
| [RetainFirstSectionStart](../../aspose.words.mailmerging/mailmerge/retainfirstsectionstart/) { get; set; } | Ottiene o imposta un valore che indica se il[`SectionStart`](../../aspose.words/pagesetup/sectionstart/) della prima sezione del documento e le sue copie per l'origine dati successiva, le righe vengono conservate durante la stampa unione o aggiornate in base al comportamento di MS Word. |
| [TrimWhitespaces](../../aspose.words.mailmerging/mailmerge/trimwhitespaces/) { get; set; } | Ottiene o imposta un valore che indica se gli spazi bianchi finali e iniziali vengono tagliati dai valori di stampa unione. |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/) { get; set; } | Ottiene o imposta un valore che indica se i campi di unione e le regioni di unione vengono uniti indipendentemente dalle condizioni del campo IF padre. |
| [UseNonMergeFields](../../aspose.words.mailmerging/mailmerge/usenonmergefields/) { get; set; } | Se true, specifica che oltre ai campi MERGEFIELD, la stampa unione viene eseguita in alcuni altri tipi di campi e anche nei tag "{{fieldName}}". |
| [UseWholeParagraphAsRegion](../../aspose.words.mailmerging/mailmerge/usewholeparagraphasregion/) { get; set; } | Ottiene o imposta un valore che indica se l'intero paragrafo con il campo TableStart o TableEnd o un particolare intervallo tra i campi TableStart e TableEnd deve essere incluso nell'area della stampa unione. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [DeleteFields](../../aspose.words.mailmerging/mailmerge/deletefields/)() | Rimuove i campi relativi alla stampa unione dal documento. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_1)(DataRow) | Esegue la stampa unione da un DataRow nel documento. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_2)(DataTable) | Esegue la stampa unione da una DataTable nel documento. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_3)(DataView) | Esegue la stampa unione da un DataView nel documento. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_4)(IDataReader) | Esegue la stampa unione da IDataReader nel documento. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute)(IMailMergeDataSource) | Esegue una stampa unione da un'origine dati personalizzata. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_5)(string[], object[]) | Esegue un'operazione di stampa unione per un singolo record. |
| [ExecuteADO](../../aspose.words.mailmerging/mailmerge/executeado/)(object) | Esegue la stampa unione da un oggetto Recordset ADO nel documento. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_2)(DataSet) | Esegue la stampa unione da un DataSet in un documento con aree di stampa unione. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_3)(DataTable) | Esegue la stampa unione da una DataTable nel documento con le regioni della stampa unione. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_4)(DataView) | Esegue la stampa unione da un DataView nel documento con le regioni della stampa unione. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions)(IMailMergeDataSource) | Esegue una stampa unione da un'origine dati personalizzata con regioni di stampa unione. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_1)(IMailMergeDataSourceRoot) | Esegue una stampa unione da un'origine dati personalizzata con regioni di stampa unione. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_5)(IDataReader, string) | Esegue la stampa unione da IDataReader nel documento con le regioni della stampa unione. |
| [ExecuteWithRegionsADO](../../aspose.words.mailmerging/mailmerge/executewithregionsado/)(object, string) | Esegue la stampa unione da un oggetto Recordset ADO nel documento con le regioni della stampa unione. |
| [GetFieldNames](../../aspose.words.mailmerging/mailmerge/getfieldnames/)() | Restituisce una raccolta di nomi di campi stampa unione disponibili nel documento. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion)(string) | Restituisce una raccolta di nomi di campi stampa unione disponibili nella regione. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion_1)(string, int) | Restituisce una raccolta di nomi di campi stampa unione disponibili nella regione. |
| [GetRegionsByName](../../aspose.words.mailmerging/mailmerge/getregionsbyname/)(string) | Restituisce una raccolta di regioni di stampa unione con il nome specificato. |
| [GetRegionsHierarchy](../../aspose.words.mailmerging/mailmerge/getregionshierarchy/)() | Restituisce una gerarchia completa di regioni (con campi) disponibili nel documento. |

### Osservazioni

Affinché l'operazione di stampa unione funzioni, il documento deve contenere i campi Word MERGEFIELD e facoltativamente. Durante l'operazione di stampa unione, i campi di unione nel documento vengono sostituiti con valori dall'origine dati.

Esistono due modi distinti per utilizzare la stampa unione: con le regioni della stampa unione e senza.

La stampa unione più semplice è senza aree ed è molto simile a come funziona la stampa unione in Word. UsoEseguire metodi per unire le informazioni da alcune origini dati come **Tabella dati** , **DataSet** , **Vista dati** , **Lettore di dati** o una matrice di oggetti nel documento. Il  **Stampa unione** oggetto elabora tutti i record dell'origine dati e copia e aggiunge contenuto dell'intero documento per ogni record.

Nota che quando **Stampa unione**l'oggetto incontra un campo NEXT, seleziona il record successivo nell'origine dati e continua a unire senza copiare alcun contenuto.

UsoEsegui con le regioni metodi per unire le informazioni in un documento con le regioni di stampa unione definite. Puoi usare  **DataSet** , **Tabella dati** , **Vista dati** o **Lettore di dati** come origini dati per questa operazione.

È necessario utilizzare le regioni di stampa unione se si desidera aumentare dinamicamente le porzioni all'interno del documento . Senza le regioni di stampa unione, l'intero documento verrà ripetuto per ogni record di l'origine dati.

### Esempi

Mostra come eseguire una stampa unione con i dati di un DataTable.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Di seguito sono riportati due modi per utilizzare una DataTable come origine dati per una stampa unione.
    // 1 - Utilizza l'intera tabella per la stampa unione per creare un documento di stampa unione di output per ogni riga della tabella:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Usa una riga della tabella per creare un documento di stampa unione di output:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Crea un documento sorgente di stampa unione.
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


