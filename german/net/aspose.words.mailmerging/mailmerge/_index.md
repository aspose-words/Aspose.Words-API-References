---
title: MailMerge Class
linktitle: MailMerge
articleTitle: MailMerge
second_title: Aspose.Words für .NET
description: Schalten Sie leistungsstarke Serienbrieffunktionen mit der Klasse Aspose.Words.MailMerging.MailMerge frei. Optimieren Sie die Dokumenterstellung und steigern Sie mühelos die Produktivität!
type: docs
weight: 4530
url: /de/net/aspose.words.mailmerging/mailmerge/
---
## MailMerge class

Stellt die Serienbrieffunktion dar.

Um mehr zu erfahren, besuchen Sie die[Serienbriefe und Berichte](https://docs.aspose.com/words/net/mail-merge-and-reporting/) Dokumentationsartikel.

```csharp
public class MailMerge
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CleanupOptions](../../aspose.words.mailmerging/mailmerge/cleanupoptions/) { get; set; } | Ruft eine Reihe von Flags ab oder legt diese fest, die angeben, welche Elemente während der Seriendruckfunktion entfernt werden sollen. |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der angibt, ob Absätze mit Satzzeichen als leer betrachtet werden und entfernt werden sollen, wenn dieRemoveEmptyParagraphs Option angegeben ist. |
| [FieldMergingCallback](../../aspose.words.mailmerging/mailmerge/fieldmergingcallback/) { get; set; } | Tritt während des Seriendrucks auf, wenn im Dokument ein Seriendruckfeld gefunden wird. |
| [MailMergeCallback](../../aspose.words.mailmerging/mailmerge/mailmergecallback/) { get; set; } | Ermöglicht die Verarbeitung bestimmter Ereignisse während des Seriendrucks. |
| [MappedDataFields](../../aspose.words.mailmerging/mailmerge/mappeddatafields/) { get; } | Gibt eine Sammlung zurück, die zugeordnete Datenfelder für den Seriendruckvorgang darstellt. |
| [MergeDuplicateRegions](../../aspose.words.mailmerging/mailmerge/mergeduplicateregions/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob beim Ausführen eines Seriendrucks mit Regionen für die Datenquelle alle Seriendruckregionen des Dokuments mit dem Namen einer Datenquelle oder nur die erste zusammengeführt werden sollen. |
| [MergeWholeDocument](../../aspose.words.mailmerging/mailmerge/mergewholedocument/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob Felder im gesamten Dokument beim Ausführen eines Seriendrucks mit Regionen aktualisiert werden. |
| [PreserveUnusedTags](../../aspose.words.mailmerging/mailmerge/preserveunusedtags/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob die nicht verwendeten „Mustache“-Tags beibehalten werden sollen. |
| [RegionEndTag](../../aspose.words.mailmerging/mailmerge/regionendtag/) { get; set; } | Ruft ein Endtag für den Seriendruckbereich ab oder legt dieses fest. |
| [RegionStartTag](../../aspose.words.mailmerging/mailmerge/regionstarttag/) { get; set; } | Ruft ein Starttag für den Seriendruckbereich ab oder legt dieses fest. |
| [RestartListsAtEachSection](../../aspose.words.mailmerging/mailmerge/restartlistsateachsection/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob Listen nach der Ausführung eines Seriendrucks in jedem Abschnitt neu gestartet werden. |
| [RetainFirstSectionStart](../../aspose.words.mailmerging/mailmerge/retainfirstsectionstart/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der angibt, ob die[`SectionStart`](../../aspose.words/pagesetup/sectionstart/) des ersten Dokumentabschnitts und seiner Kopien für nachfolgende Datenquellenzeilen werden beim Seriendruck beibehalten oder entsprechend dem Verhalten von MS Word aktualisiert. |
| [TrimWhitespaces](../../aspose.words.mailmerging/mailmerge/trimwhitespaces/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob nachstehende und führende Leerzeichen aus Serienbriefwerten entfernt werden. |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob Zusammenführungsfelder und Zusammenführungsbereiche unabhängig von der Bedingung des übergeordneten IF-Felds zusammengeführt werden. |
| [UseNonMergeFields](../../aspose.words.mailmerging/mailmerge/usenonmergefields/) { get; set; } | Wann`WAHR` , gibt an, dass Serienbriefe zusätzlich zu MERGEFIELD-Feldern auch in einigen anderen Feldtypen und auch in "{{fieldName}}"-Tags ausgeführt werden. |
| [UseWholeParagraphAsRegion](../../aspose.words.mailmerging/mailmerge/usewholeparagraphasregion/) { get; set; } | Ruft einen Wert ab oder setzt ihn, der angibt, ob der ganze Absatz mit**TischStart** oder**Tabellenende** field oder bestimmter Bereich zwischen**TischStart** Und**Tabellenende** Felder sollten in den Serienbriefbereich aufgenommen werden. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [DeleteFields](../../aspose.words.mailmerging/mailmerge/deletefields/)() | Entfernt Serienbrieffelder aus dem Dokument. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_1)(*DataRow*) | Führt Serienbriefe aus einem**Datenzeile** in das Dokument. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_2)(*DataTable*) | Führt einen Serienbrief aus einer DataTable in das Dokument aus. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_3)(*DataView*) | Führt Serienbriefe aus einem**Datenansicht** in das Dokument. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_4)(*IDataReader*) | Führt Serienbriefe aus von**IDataReader** in das Dokument. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute)(*[IMailMergeDataSource](../imailmergedatasource/)*) | Führt einen Serienbrief aus einer benutzerdefinierten Datenquelle aus. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_5)(*string[], object[]*) | Führt einen Serienbriefvorgang für einen einzelnen Datensatz aus. |
| [ExecuteADO](../../aspose.words.mailmerging/mailmerge/executeado/)(*object*) | Führt einen Seriendruck von einem ADO-Recordset-Objekt in das Dokument aus. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_2)(*DataSet*) | Führt Serienbriefe aus einem**Datensatz** in ein Dokument mit Seriendruckbereichen. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_3)(*DataTable*) | Führt Serienbriefe aus einem**Datentabelle** in das Dokument mit Seriendruckbereichen. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_4)(*DataView*) | Führt Serienbriefe aus einem**Datenansicht** in das Dokument mit Seriendruckbereichen. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions)(*[IMailMergeDataSource](../imailmergedatasource/)*) | Führt einen Serienbrief aus einer benutzerdefinierten Datenquelle mit Serienbriefbereichen aus. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_1)(*[IMailMergeDataSourceRoot](../imailmergedatasourceroot/)*) | Führt einen Serienbrief aus einer benutzerdefinierten Datenquelle mit Serienbriefbereichen aus. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_5)(*IDataReader, string*) | Führt Serienbriefe aus von**IDataReader** in das Dokument mit Seriendruckbereichen. |
| [ExecuteWithRegionsADO](../../aspose.words.mailmerging/mailmerge/executewithregionsado/)(*object, string*) | Führt einen Seriendruck von einem ADO-Recordset-Objekt in das Dokument mit Seriendruckbereichen durch. |
| [GetFieldNames](../../aspose.words.mailmerging/mailmerge/getfieldnames/)() | Gibt eine Sammlung der im Dokument verfügbaren Seriendruckfeldnamen zurück. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion)(*string*) | Gibt eine Sammlung von Serienbrieffeldnamen zurück, die in der Region verfügbar sind. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion_1)(*string, int*) | Gibt eine Sammlung von Serienbrieffeldnamen zurück, die in der Region verfügbar sind. |
| [GetRegionsByName](../../aspose.words.mailmerging/mailmerge/getregionsbyname/)(*string*) | Gibt eine Sammlung von Serienbriefbereichen mit dem angegebenen Namen zurück. |
| [GetRegionsHierarchy](../../aspose.words.mailmerging/mailmerge/getregionshierarchy/)() | Gibt eine vollständige Hierarchie der im Dokument verfügbaren Regionen (mit Feldern) zurück. |

## Bemerkungen

Damit der Seriendruck funktioniert, muss das Dokument die Word-Felder MERGEFIELD und optional NEXT enthalten. Beim Seriendruck werden die Seriendruckfelder im Dokument durch Werte aus Ihrer Datenquelle ersetzt.

Es gibt zwei verschiedene Möglichkeiten, Serienbriefe zu verwenden: mit Serienbriefbereichen und ohne.

Der einfachste Serienbrief ist ohne Regionen und ähnelt stark der Funktion von Serienbriefen in Word. Verwenden SieAusführen Methoden zum Zusammenführen von Informationen aus einer Datenquelle wie**Datentabelle** ,**Datensatz** ,**Datenansicht** ,**IDataReader** oder ein Array von Objekten in Ihr Dokument. Das `MailMerge` Das Objekt verarbeitet alle Datensätze der Datenquelle und kopiert und fügt für jeden Datensatz den Inhalt des gesamten Dokuments hinzu.

Beachten Sie, dass wenn`MailMerge`Wenn das Objekt auf ein NEXT-Feld stößt, wählt es den nächsten Datensatz in der Datenquelle aus und fährt mit der Zusammenführung fort, ohne Inhalte zu kopieren.

Verwenden[`ExecuteWithRegions`](./executewithregions/) und andere Überladungen, um Informationen in einem -Dokument mit definierten Serienbriefbereichen zusammenzuführen. Sie können verwenden**Datensatz** ,**Datentabelle** ,**Datenansicht** oder**IDataReader** als Datenquellen für diesen Vorgang.

Sie müssen Seriendruckbereiche verwenden, wenn Sie Teile innerhalb des -Dokuments dynamisch erweitern möchten. Ohne Seriendruckbereiche wird das gesamte Dokument für jeden Datensatz der -Datenquelle wiederholt.

## Beispiele

Zeigt, wie ein Serienbrief mit Daten aus einer DataTable ausgeführt wird.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Nachfolgend finden Sie zwei Möglichkeiten, eine DataTable als Datenquelle für einen Serienbrief zu verwenden.
    // 1 - Verwenden Sie die gesamte Tabelle für den Seriendruck, um für jede Zeile in der Tabelle ein Ausgabe-Seriendruckdokument zu erstellen:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Verwenden Sie eine Zeile der Tabelle, um ein Serienbrief-Ausgabedokument zu erstellen:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Erstellt ein Serienbrief-Quelldokument.
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

### Siehe auch

* namensraum [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../)
