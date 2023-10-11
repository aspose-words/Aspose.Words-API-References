---
title: Class MailMerge
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.MailMerging.MailMerge klass. Representerar funktionen för sammankoppling av brev.
type: docs
weight: 3840
url: /sv/net/aspose.words.mailmerging/mailmerge/
---
## MailMerge class

Representerar funktionen för sammankoppling av brev.

För att lära dig mer, besök[Mail Merge och rapportering](https://docs.aspose.com/words/net/mail-merge-and-reporting/) dokumentationsartikel.

```csharp
public class MailMerge
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [CleanupOptions](../../aspose.words.mailmerging/mailmerge/cleanupoptions/) { get; set; } | Hämtar eller ställer in en uppsättning flaggor som anger vilka objekt som ska tas bort under kopplingen. |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/) { get; set; } | Hämtar eller ställer in ett värde som anger om stycken med skiljetecken anses vara tomma och bör tas bort omRemoveEmptyParagraphs alternativet är specificerat. |
| [FieldMergingCallback](../../aspose.words.mailmerging/mailmerge/fieldmergingcallback/) { get; set; } | Förekommer under sammankoppling när ett sammanslagningsfält påträffas i dokumentet. |
| [MailMergeCallback](../../aspose.words.mailmerging/mailmerge/mailmergecallback/) { get; set; } | Tillåter att hantera särskilda händelser under sammanslagningen. |
| [MappedDataFields](../../aspose.words.mailmerging/mailmerge/mappeddatafields/) { get; } | Returnerar en samling som representerar mappade datafält för kopplingsoperationen. |
| [MergeDuplicateRegions](../../aspose.words.mailmerging/mailmerge/mergeduplicateregions/) { get; set; } | Hämtar eller ställer in ett värde som indikerar om alla dokumentkopplingsregioner med namnet på en datakälla ska slås samman under körning av en brevkoppling med regioner mot datakällan eller bara den första. |
| [MergeWholeDocument](../../aspose.words.mailmerging/mailmerge/mergewholedocument/) { get; set; } | Hämtar eller ställer in ett värde som indikerar om fält i hela dokumentet uppdateras under körning av en sammankoppling med regioner. |
| [PreserveUnusedTags](../../aspose.words.mailmerging/mailmerge/preserveunusedtags/) { get; set; } | Hämtar eller ställer in ett värde som anger om de oanvända "mustasch"-taggarna ska bevaras. |
| [RegionEndTag](../../aspose.words.mailmerging/mailmerge/regionendtag/) { get; set; } | Hämtar eller ställer in en sluttagg för kopplingsregion. |
| [RegionStartTag](../../aspose.words.mailmerging/mailmerge/regionstarttag/) { get; set; } | Hämtar eller ställer in en starttagg för kopplingsregion. |
| [RestartListsAtEachSection](../../aspose.words.mailmerging/mailmerge/restartlistsateachsection/) { get; set; } | Hämtar eller ställer in ett värde som anger om listor startas om vid varje sektion efter körning av en e-postsammanfogning. |
| [RetainFirstSectionStart](../../aspose.words.mailmerging/mailmerge/retainfirstsectionstart/) { get; set; } | Hämtar eller ställer in ett värde som indikerar om[`SectionStart`](../../aspose.words/pagesetup/sectionstart/) av det första dokumentavsnittet och dess kopior för efterföljande datakälla rows bevaras under sammankoppling eller uppdateras enligt MS Word-beteende. |
| [TrimWhitespaces](../../aspose.words.mailmerging/mailmerge/trimwhitespaces/) { get; set; } | Hämtar eller ställer in ett värde som anger om efterföljande och inledande blanksteg beskärs från sammanslagningsvärden. |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/) { get; set; } | Hämtar eller ställer in ett värde som anger om sammanslagningsfält och sammanslagningsregioner slås samman oavsett det överordnade IF-fältets tillstånd. |
| [UseNonMergeFields](../../aspose.words.mailmerging/mailmerge/usenonmergefields/) { get; set; } | När`Sann` , anger att förutom MERGEFIELD-fält utförs e-postsammankoppling till vissa andra typer av fält och även i "{{fieldName}}"-taggar. |
| [UseWholeParagraphAsRegion](../../aspose.words.mailmerging/mailmerge/usewholeparagraphasregion/) { get; set; } | Hämtar eller ställer in ett värde som anger om hela stycket med **TableStart** eller **TableEnd** field eller särskilt intervall mellan **TableStart** och **TableEnd** fält ska inkluderas i kopplingsområdet. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [DeleteFields](../../aspose.words.mailmerging/mailmerge/deletefields/)() | Tar bort sammanslagningsrelaterade fält från dokumentet. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_1)(DataRow) | Utför sammanslagning från en **DataRow** in i dokumentet. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_2)(DataTable) | Utför e-postkoppling från en datatabell till dokumentet. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_3)(DataView) | Utför sammanslagning från en **DataView** in i dokumentet. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_4)(IDataReader) | Utför sammanslagning från **IDataReader** in i dokumentet. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute)(IMailMergeDataSource) | Utför en e-postsammanfogning från en anpassad datakälla. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_5)(string[], object[]) | Utför en kopplingsoperation för en enskild post. |
| [ExecuteADO](../../aspose.words.mailmerging/mailmerge/executeado/)(object) | Utför e-postkoppling från ett ADO Recordset-objekt till dokumentet. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_2)(DataSet) | Utför sammanslagning från en **Dataset** till ett dokument med kopplingsregioner. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_3)(DataTable) | Utför sammanslagning från en **Datatabell** in i dokumentet med kopplingsregioner. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_4)(DataView) | Utför sammanslagning från en **DataView** in i dokumentet med kopplingsregioner. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions)(IMailMergeDataSource) | Utför en koppling av e-post från en anpassad datakälla med kopplingsregioner. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_1)(IMailMergeDataSourceRoot) | Utför en koppling av e-post från en anpassad datakälla med kopplingsregioner. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_5)(IDataReader, string) | Utför sammanslagning från **IDataReader** in i dokumentet med kopplingsregioner. |
| [ExecuteWithRegionsADO](../../aspose.words.mailmerging/mailmerge/executewithregionsado/)(object, string) | Utför koppling från ett ADO Recordset-objekt till dokumentet med kopplingsregioner. |
| [GetFieldNames](../../aspose.words.mailmerging/mailmerge/getfieldnames/)() | Returnerar en samling av kopplingsfältnamn som är tillgängliga i dokumentet. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion)(string) | Returnerar en samling av kopplingsfältnamn som är tillgängliga i regionen. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion_1)(string, int) | Returnerar en samling av kopplingsfältnamn som är tillgängliga i regionen. |
| [GetRegionsByName](../../aspose.words.mailmerging/mailmerge/getregionsbyname/)(string) | Returnerar en samling kopplingsregioner med det angivna namnet. |
| [GetRegionsHierarchy](../../aspose.words.mailmerging/mailmerge/getregionshierarchy/)() | Returnerar en fullständig hierarki av regioner (med fält) tillgängliga i dokumentet. |

### Anmärkningar

För att kopplingen ska fungera bör dokumentet innehålla Word MERGEFIELD och valfritt NEXT-fält. Under kopplingsoperationen ersätts kopplingsfälten i dokumentet med värden från din datakälla.

Det finns två distinkta sätt att använda koppling av e-post: med kopplingsregioner och utan.

Den enklaste kopplingen är utan regioner och den är väldigt lik hur e-postsammankoppling fungerar i Word. Använda sig avKör metoder för att slå samman information från some datakälla som t.ex **Datatabell** , **Dataset** , **DataView** , **IDataReader** eller en mängd objekt i ditt dokument. The `MailMerge` objekt bearbetar alla poster i datakällan och kopierar och lägger till innehållet i hela dokumentet för varje post.

Observera att när`MailMerge` objektet stöter på ett NEXT-fält, väljer det nästa post i datakällan och fortsätter att slås samman utan att kopiera något innehåll.

Använda sig av[`ExecuteWithRegions`](./executewithregions/) och andra överbelastningar för att sammanfoga information till a dokument med kopplingsregioner definierade. Du kan använda  **Dataset** , **Datatabell** , **DataView** eller **IDataReader** som datakällor för denna operation.

Du måste använda kopplingsregioner om du dynamiskt vill växa delar inuti dokumentet . Utan sammanslagningsregioner kommer hela dokumentet att upprepas för varje post av datakällan.

### Exempel

Visar hur man kör en e-postsammanfogning med data från en datatabell.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Nedan finns två sätt att använda en datatabell som datakälla för en e-postkoppling.
    // 1 - Använd hela tabellen för kopplingen för att skapa ett kopplingsdokument för varje rad i tabellen:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Använd en rad i tabellen för att skapa ett dokument för utmatning av dokument:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Skapar ett källdokument för sammankoppling av brev.
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


