---
title: MailMerge Class
linktitle: MailMerge
articleTitle: MailMerge
second_title: Aspose.Words für .NET
description: Aspose.Words.MailMerging.MailMerge klas. Stellt die Serienbrieffunktion dar in C#.
type: docs
weight: 3840
url: /de/net/aspose.words.mailmerging/mailmerge/
---
## MailMerge class

Stellt die Serienbrieffunktion dar.

Um mehr zu erfahren, besuchen Sie die[Serienbrief und Berichterstellung](https://docs.aspose.com/words/net/mail-merge-and-reporting/) Dokumentationsartikel.

```csharp
public class MailMerge
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CleanupOptions](../../aspose.words.mailmerging/mailmerge/cleanupoptions/) { get; set; } | Ruft eine Reihe von Flags ab, die angeben, welche Elemente beim Seriendruck entfernt werden sollen, oder legt diese fest. |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der angibt, ob Absätze mit Satzzeichen als leer betrachtet werden und entfernt werden sollten, wenn dieRemoveEmptyParagraphs Option ist angegeben. |
| [FieldMergingCallback](../../aspose.words.mailmerging/mailmerge/fieldmergingcallback/) { get; set; } | Tritt beim Serienbrief auf, wenn im Dokument ein Serienbrieffeld gefunden wird. |
| [MailMergeCallback](../../aspose.words.mailmerging/mailmerge/mailmergecallback/) { get; set; } | Ermöglicht die Verarbeitung bestimmter Ereignisse während des Seriendrucks. |
| [MappedDataFields](../../aspose.words.mailmerging/mailmerge/mappeddatafields/) { get; } | Gibt eine Sammlung zurück, die zugeordnete Datenfelder für den Seriendruckvorgang darstellt. |
| [MergeDuplicateRegions](../../aspose.words.mailmerging/mailmerge/mergeduplicateregions/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der angibt, ob alle Dokument-Seriendruckbereiche mit dem Namen einer Datenquelle beim Ausführen eines Seriendrucks mit Bereichen für die Datenquelle zusammengeführt werden sollen oder nur der erste. |
| [MergeWholeDocument](../../aspose.words.mailmerging/mailmerge/mergewholedocument/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der angibt, ob Felder im gesamten Dokument beim Ausführen eines Seriendrucks mit Regionen aktualisiert werden. |
| [PreserveUnusedTags](../../aspose.words.mailmerging/mailmerge/preserveunusedtags/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der angibt, ob die nicht verwendeten „Mustache“-Tags beibehalten werden sollen. |
| [RegionEndTag](../../aspose.words.mailmerging/mailmerge/regionendtag/) { get; set; } | Ruft ein End-Tag für den Seriendruckbereich ab oder legt es fest. |
| [RegionStartTag](../../aspose.words.mailmerging/mailmerge/regionstarttag/) { get; set; } | Ruft ein Start-Tag für den Seriendruckbereich ab oder legt es fest. |
| [RestartListsAtEachSection](../../aspose.words.mailmerging/mailmerge/restartlistsateachsection/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der angibt, ob Listen in jedem Abschnitt nach der Ausführung eines Seriendrucks neu gestartet werden. |
| [RetainFirstSectionStart](../../aspose.words.mailmerging/mailmerge/retainfirstsectionstart/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der angibt, ob die[`SectionStart`](../../aspose.words/pagesetup/sectionstart/) des ersten Dokumentabschnitts und seiner Kopien für nachfolgende Datenquellenzeilen bleiben beim Seriendruck erhalten oder werden entsprechend dem Verhalten von MS Word aktualisiert. |
| [TrimWhitespaces](../../aspose.words.mailmerging/mailmerge/trimwhitespaces/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der angibt, ob nachgestellte und führende Leerzeichen aus Serienbriefwerten entfernt werden. |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der angibt, ob Zusammenführungsfelder und Zusammenführungsbereiche unabhängig von der Bedingung des übergeordneten IF-Felds zusammengeführt werden. |
| [UseNonMergeFields](../../aspose.words.mailmerging/mailmerge/usenonmergefields/) { get; set; } | Wann`WAHR` , gibt an, dass der Seriendruck zusätzlich zu MERGEFIELD-Feldern auch in einigen anderen Feldtypen und auch in „{{fieldName}}“-Tags durchgeführt wird. |
| [UseWholeParagraphAsRegion](../../aspose.words.mailmerging/mailmerge/usewholeparagraphasregion/) { get; set; } | Ruft einen Wert ab oder legt diesen fest, der angibt, ob ein ganzer Absatz vorhanden ist**TableStart** oder**TableEnd** field oder ein bestimmter Bereich dazwischen**TableStart** Und**TableEnd** Felder sollten in den Serienbriefbereich aufgenommen werden. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [DeleteFields](../../aspose.words.mailmerging/mailmerge/deletefields/)() | Entfernt Serienbrieffelder aus dem Dokument. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_1)(*DataRow*) | Führt einen Serienbrief von einem aus**Datenzeile** in das Dokument. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_2)(*DataTable*) | Führt einen Serienbrief von einer Datentabelle in das Dokument durch. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_3)(*DataView*) | Führt einen Serienbrief von einem aus**Datenansicht** in das Dokument. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_4)(*IDataReader*) | Führt einen Serienbrief durch**IDataReader** in das Dokument. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute)(*[IMailMergeDataSource](../imailmergedatasource/)*) | Führt einen Seriendruck aus einer benutzerdefinierten Datenquelle durch. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_5)(*string[], object[]*) | Führt einen Seriendruckvorgang für einen einzelnen Datensatz durch. |
| [ExecuteADO](../../aspose.words.mailmerging/mailmerge/executeado/)(*object*) | Führt einen Serienbrief von einem ADO-Recordset-Objekt in das Dokument durch. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_2)(*DataSet*) | Führt einen Serienbrief von einem aus**Datensatz** in ein Dokument mit Seriendruckbereichen. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_3)(*DataTable*) | Führt einen Serienbrief von einem aus**Datentabelle** in das Dokument mit Seriendruckbereichen. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_4)(*DataView*) | Führt einen Serienbrief von einem aus**Datenansicht** in das Dokument mit Seriendruckbereichen. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions)(*[IMailMergeDataSource](../imailmergedatasource/)*) | Führt einen Serienbrief aus einer benutzerdefinierten Datenquelle mit Serienbriefbereichen durch. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_1)(*[IMailMergeDataSourceRoot](../imailmergedatasourceroot/)*) | Führt einen Serienbrief aus einer benutzerdefinierten Datenquelle mit Serienbriefbereichen durch. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_5)(*IDataReader, string*) | Führt einen Serienbrief durch**IDataReader** in das Dokument mit Seriendruckbereichen. |
| [ExecuteWithRegionsADO](../../aspose.words.mailmerging/mailmerge/executewithregionsado/)(*object, string*) | Führt einen Serienbrief von einem ADO-Recordset-Objekt in das Dokument mit Serienbriefbereichen durch. |
| [GetFieldNames](../../aspose.words.mailmerging/mailmerge/getfieldnames/)() | Gibt eine Sammlung von im Dokument verfügbaren Serienbrieffeldnamen zurück. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion)(*string*) | Gibt eine Sammlung von Serienbrieffeldnamen zurück, die in der Region verfügbar sind. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion_1)(*string, int*) | Gibt eine Sammlung von Serienbrieffeldnamen zurück, die in der Region verfügbar sind. |
| [GetRegionsByName](../../aspose.words.mailmerging/mailmerge/getregionsbyname/)(*string*) | Gibt eine Sammlung von Serienbriefregionen mit dem angegebenen Namen zurück. |
| [GetRegionsHierarchy](../../aspose.words.mailmerging/mailmerge/getregionshierarchy/)() | Gibt eine vollständige Hierarchie der im Dokument verfügbaren Regionen (mit Feldern) zurück. |

## Bemerkungen

Damit der Seriendruckvorgang funktioniert, sollte das Dokument Word-Felder MERGEFIELD und (optional NEXT) enthalten. Während des Serienbriefvorgangs werden die Briefvorlagenfelder im Dokument durch Werte aus Ihrer Datenquelle ersetzt.

Es gibt zwei unterschiedliche Möglichkeiten, den Seriendruck zu verwenden: mit Seriendruckbereichen und ohne.

Der einfachste Seriendruck erfolgt ohne Regionen und ähnelt stark der Funktionsweise von Serienbrief in Word. VerwendenAusführen Methoden zum Zusammenführen von Informationen aus einer -Datenquelle, z. B**Datentabelle** ,**Datensatz** ,**Datenansicht** ,**IDataReader** oder ein Array von Objekten in Ihr Dokument. The `MailMerge` Das Objekt verarbeitet alle Datensätze der Datenquelle und kopiert und hängt den Inhalt des gesamten Dokuments für jeden Datensatz an.

Beachten Sie, wann`MailMerge` Wenn das Objekt auf ein NEXT-Feld trifft, wählt es den nächsten Datensatz in der Datenquelle aus und setzt die Zusammenführung fort, ohne Inhalte zu kopieren.

Verwenden[`ExecuteWithRegions`](./executewithregions/) und andere Überladungen zum Zusammenführen von Informationen in einem -Dokument mit definierten Seriendruckbereichen. Sie können verwenden**Datensatz** ,**Datentabelle** ,**Datenansicht** oder**IDataReader** als Datenquellen für diesen Vorgang.

Sie müssen Serienbriefbereiche verwenden, wenn Sie Teile innerhalb des -Dokuments dynamisch vergrößern möchten. Ohne Seriendruckbereiche wird das gesamte Dokument für jeden Datensatz der Datenquelle wiederholt.

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
    // 1 – Verwenden Sie die gesamte Tabelle für den Serienbrief, um für jede Zeile in der Tabelle ein Ausgabe-Serienbriefdokument zu erstellen:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 – Verwenden Sie eine Zeile der Tabelle, um ein Ausgabe-Serienbriefdokument zu erstellen:
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
