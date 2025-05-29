---
title: MailMerge Class
linktitle: MailMerge
articleTitle: MailMerge
second_title: Aspose.Words för .NET
description: Lås upp kraftfulla funktioner för dokumentkoppling med klassen Aspose.Words.MailMerging.MailMerge. Effektivisera dokumentskapandet och öka produktiviteten utan ansträngning!
type: docs
weight: 4530
url: /sv/net/aspose.words.mailmerging/mailmerge/
---
## MailMerge class

Representerar funktionen för dokumentkoppling.

För att lära dig mer, besök[Koppla dokument och rapportering](https://docs.aspose.com/words/net/mail-merge-and-reporting/) dokumentationsartikel.

```csharp
public class MailMerge
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CleanupOptions](../../aspose.words.mailmerging/mailmerge/cleanupoptions/) { get; set; } | Hämtar eller anger en uppsättning flaggor som anger vilka objekt som ska tas bort under dokumentkoppling. |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/) { get; set; } | Hämtar eller anger ett värde som anger om stycken med skiljetecken ska betraktas som tomma och ska tas bort omRemoveEmptyParagraphs alternativet är angivet. |
| [FieldMergingCallback](../../aspose.words.mailmerging/mailmerge/fieldmergingcallback/) { get; set; } | Inträffar under koppling av dokument när ett fält för koppling av dokument påträffas i dokumentet. |
| [MailMergeCallback](../../aspose.words.mailmerging/mailmerge/mailmergecallback/) { get; set; } | Tillåter hantering av specifika händelser under dokumentkoppling. |
| [MappedDataFields](../../aspose.words.mailmerging/mailmerge/mappeddatafields/) { get; } | Returnerar en samling som representerar mappade datafält för dokumentkopplingsoperationen. |
| [MergeDuplicateRegions](../../aspose.words.mailmerging/mailmerge/mergeduplicateregions/) { get; set; } | Hämtar eller anger ett värde som anger om alla dokumentkopplingsområden med namnet på en datakälla ska slås samman vid utskriftskoppling med regioner mot datakällan eller bara den första. |
| [MergeWholeDocument](../../aspose.words.mailmerging/mailmerge/mergewholedocument/) { get; set; } | Hämtar eller anger ett värde som anger om fält i hela dokumentet uppdateras när en dokumentkoppling med regioner utförs. |
| [PreserveUnusedTags](../../aspose.words.mailmerging/mailmerge/preserveunusedtags/) { get; set; } | Hämtar eller anger ett värde som anger om de oanvända "mustasch"-taggarna ska bevaras. |
| [RegionEndTag](../../aspose.words.mailmerging/mailmerge/regionendtag/) { get; set; } | Hämtar eller ställer in en sluttagg för ett regionsavsnitt för dokumentkoppling. |
| [RegionStartTag](../../aspose.words.mailmerging/mailmerge/regionstarttag/) { get; set; } | Hämtar eller ställer in en starttagg för en region för dokumentkoppling. |
| [RestartListsAtEachSection](../../aspose.words.mailmerging/mailmerge/restartlistsateachsection/) { get; set; } | Hämtar eller anger ett värde som anger om listor startas om i varje avsnitt efter att en dokumentkoppling har utförts. |
| [RetainFirstSectionStart](../../aspose.words.mailmerging/mailmerge/retainfirstsectionstart/) { get; set; } | Hämtar eller ställer in ett värde som anger om[`SectionStart`](../../aspose.words/pagesetup/sectionstart/) av det första dokumentavsnittet och dess kopior för efterföljande datakällrader behålls under dokumentkoppling eller uppdateras enligt MS Words beteende. |
| [TrimWhitespaces](../../aspose.words.mailmerging/mailmerge/trimwhitespaces/) { get; set; } | Hämtar eller anger ett värde som anger om efterföljande och inledande blanksteg ska tas bort från värden för koppling av dokument. |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/) { get; set; } | Hämtar eller anger ett värde som anger om sammanslagningsfält och sammanslagningsområden slås samman oavsett det överordnade OM-fältets villkor. |
| [UseNonMergeFields](../../aspose.words.mailmerging/mailmerge/usenonmergefields/) { get; set; } | När`sann` , anger att utöver MERGEFIELD-fält utförs dokumentkoppling i vissa andra typer av fält och även i "{{fieldName}}"-taggar. |
| [UseWholeParagraphAsRegion](../../aspose.words.mailmerging/mailmerge/usewholeparagraphasregion/) { get; set; } | Hämtar eller anger ett värde som anger om hela stycket med**Tabellstart** eller**Bordände** field eller ett visst intervall mellan**Tabellstart** och**Bordände** fält ska inkluderas i området för koppling av dokument. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [DeleteFields](../../aspose.words.mailmerging/mailmerge/deletefields/)() | Tar bort fält relaterade till koppling av dokument från dokumentet. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_1)(*DataRow*) | Utför koppling av dokument från en**DataRod** in i dokumentet. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_2)(*DataTable*) | Utför koppling av dokument från en datatabell till dokumentet. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_3)(*DataView*) | Utför koppling av dokument från en**Datavy** in i dokumentet. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_4)(*IDataReader*) | Utför koppling av dokument från**IDataläsare** in i dokumentet. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute)(*[IMailMergeDataSource](../imailmergedatasource/)*) | Utför en dokumentkoppling från en anpassad datakälla. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_5)(*string[], object[]*) | Utför en dokumentkopplingsåtgärd för en enskild post. |
| [ExecuteADO](../../aspose.words.mailmerging/mailmerge/executeado/)(*object*) | Utför dokumentkoppling från ett ADO Recordset-objekt till dokumentet. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_2)(*DataSet*) | Utför koppling av dokument från en**Dataset** till ett dokument med områden för koppling av dokument. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_3)(*DataTable*) | Utför koppling av dokument från en**Datatabell** i dokumentet med områden för koppling av dokument. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_4)(*DataView*) | Utför koppling av dokument från en**Datavy** i dokumentet med områden för koppling av dokument. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions)(*[IMailMergeDataSource](../imailmergedatasource/)*) | Utför en dokumentkoppling från en anpassad datakälla med områden för dokumentkoppling. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_1)(*[IMailMergeDataSourceRoot](../imailmergedatasourceroot/)*) | Utför en dokumentkoppling från en anpassad datakälla med områden för dokumentkoppling. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_5)(*IDataReader, string*) | Utför koppling av dokument från**IDataläsare** i dokumentet med områden för koppling av dokument. |
| [ExecuteWithRegionsADO](../../aspose.words.mailmerging/mailmerge/executewithregionsado/)(*object, string*) | Utför dokumentkoppling från ett ADO Recordset-objekt till dokumentet med områden för dokumentkoppling. |
| [GetFieldNames](../../aspose.words.mailmerging/mailmerge/getfieldnames/)() | Returnerar en samling namn på fält för kopplingsmeddelanden som finns tillgängliga i dokumentet. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion)(*string*) | Returnerar en samling namn på fält för kopplingsmeddelanden som är tillgängliga i regionen. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion_1)(*string, int*) | Returnerar en samling namn på fält för kopplingsmeddelanden som är tillgängliga i regionen. |
| [GetRegionsByName](../../aspose.words.mailmerging/mailmerge/getregionsbyname/)(*string*) | Returnerar en samling av kopplingsområden för dokument med det angivna namnet. |
| [GetRegionsHierarchy](../../aspose.words.mailmerging/mailmerge/getregionshierarchy/)() | Returnerar en fullständig hierarki av regioner (med fält) som finns tillgängliga i dokumentet. |

## Anmärkningar

För att kopplingsfunktionen ska fungera måste dokumentet innehålla Word-fälten MERGEFIELD och , eventuellt NEXT. Under kopplingsfunktionen ersätts kopplingsfälten i dokumentet med värden från din datakälla.

Det finns två olika sätt att använda dokumentkoppling: med och utan områden för dokumentkoppling.

Den enklaste dokumentkopplingen är utan regioner och den är väldigt lik hur dokumentkoppling fungerar i Word.Utföra metoder för att sammanfoga information från någon datakälla såsom**Datatabell** ,**Dataset** ,**Datavy** ,**IDataläsare** eller en array av objekt i ditt dokument. The `MailMerge` objektet bearbetar alla poster i datakällan och kopierar och lägger till innehåll i hela dokumentet för varje post.

Observera att när`MailMerge`Om objektet stöter på ett NEXT-fält väljer det nästa record i datakällan och fortsätter sammanfogningen utan att kopiera något innehåll.

Använda[`ExecuteWithRegions`](./executewithregions/) och andra överbelastningar för att sammanfoga information till ett -dokument med definierade områden för dokumentkoppling. Du kan använda **Dataset** ,**Datatabell** ,**Datavy** eller**IDataläsare** som datakällor för den här operationen.

Du behöver använda områden för koppling av dokument om du vill dynamiskt utöka delar inom dokumentet . Utan områden för koppling av dokument kommer hela dokumentet att upprepas för varje post i datakällan .

## Exempel

Visar hur man utför en dokumentkoppling med data från en datatabell.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Nedan följer två sätt att använda en datatabell som datakälla för en dokumentkoppling.
    // 1 - Använd hela tabellen för dokumentkopplingen för att skapa ett utgående dokumentkopplingsdokument för varje rad i tabellen:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Använd en rad i tabellen för att skapa ett enda dokument för koppling av dokument:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Skapar ett källdokument för dokumentkoppling.
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

### Se även

* namnutrymme [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../)
