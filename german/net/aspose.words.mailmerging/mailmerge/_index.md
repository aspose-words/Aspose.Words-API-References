---
title: Class MailMerge
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.MailMerging.MailMerge klas. Repräsentiert die Seriendruckfunktion.
type: docs
weight: 3620
url: /de/net/aspose.words.mailmerging/mailmerge/
---
## MailMerge class

Repräsentiert die Seriendruckfunktion.

```csharp
public class MailMerge
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [CleanupOptions](../../aspose.words.mailmerging/mailmerge/cleanupoptions/) { get; set; } | Ruft eine Reihe von Flags ab oder legt sie fest, die angeben, welche Elemente beim Seriendruck entfernt werden sollen. |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob Absätze mit Satzzeichen als leer betrachtet und entfernt werden sollten, wenn dieRemoveEmptyParagraphs Option ist angegeben. |
| [FieldMergingCallback](../../aspose.words.mailmerging/mailmerge/fieldmergingcallback/) { get; set; } | Tritt während des Seriendrucks auf, wenn im Dokument ein Serienbrieffeld gefunden wird. |
| [MailMergeCallback](../../aspose.words.mailmerging/mailmerge/mailmergecallback/) { get; set; } | Ermöglicht die Behandlung bestimmter Ereignisse während des Seriendrucks. |
| [MappedDataFields](../../aspose.words.mailmerging/mailmerge/mappeddatafields/) { get; } | Gibt eine Sammlung zurück, die zugeordnete Datenfelder für den Seriendruckvorgang darstellt. |
| [MergeDuplicateRegions](../../aspose.words.mailmerging/mailmerge/mergeduplicateregions/) { get; set; } | Ruft oder setzt einen Wert, der angibt, ob alle Dokument-Seriendruckregionen mit dem Namen einer Datenquelle zusammengeführt werden sollen, wenn ein Seriendruck mit Regionen gegen die Datenquelle ausgeführt wird, oder nur der erste. |
| [MergeWholeDocument](../../aspose.words.mailmerging/mailmerge/mergewholedocument/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob Felder im gesamten Dokument aktualisiert werden, während ein Seriendruck mit Regionen ausgeführt wird. |
| [PreserveUnusedTags](../../aspose.words.mailmerging/mailmerge/preserveunusedtags/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob die nicht verwendeten "Schnurrbart"-Tags beibehalten werden sollen. |
| [RegionEndTag](../../aspose.words.mailmerging/mailmerge/regionendtag/) { get; set; } | Ruft ein End-Tag für die Seriendruckregion ab oder legt es fest. |
| [RegionStartTag](../../aspose.words.mailmerging/mailmerge/regionstarttag/) { get; set; } | Ruft ein Start-Tag für die Seriendruckregion ab oder legt es fest. |
| [RestartListsAtEachSection](../../aspose.words.mailmerging/mailmerge/restartlistsateachsection/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob Listen in jedem Abschnitt nach der Ausführung eines Seriendrucks neu gestartet werden. |
| [RetainFirstSectionStart](../../aspose.words.mailmerging/mailmerge/retainfirstsectionstart/) { get; set; } | Ruft einen Wert ab, der angibt, ob die[`SectionStart`](../../aspose.words/pagesetup/sectionstart/) des ersten Dokumentabschnitts und seiner Kopien für nachfolgende Datenquellenzeilen werden beim Seriendruck beibehalten oder entsprechend dem Verhalten von MS Word aktualisiert. |
| [TrimWhitespaces](../../aspose.words.mailmerging/mailmerge/trimwhitespaces/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob nachgestellte und führende Leerzeichen aus Serienbriefwerten entfernt werden. |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob Zusammenführungsfelder und Zusammenführungsbereiche unabhängig von der Bedingung des übergeordneten IF-Felds zusammengeführt werden. |
| [UseNonMergeFields](../../aspose.words.mailmerging/mailmerge/usenonmergefields/) { get; set; } | Wenn „true“, gibt an, dass der Seriendruck zusätzlich zu MERGEFIELD-Feldern in einigen anderen Feldtypen und auch in „{{fieldName}}“-Tags durchgeführt wird. |
| [UseWholeParagraphAsRegion](../../aspose.words.mailmerging/mailmerge/usewholeparagraphasregion/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der angibt, ob der gesamte Absatz mit TableStart- oder TableEnd-Feld oder ein bestimmter Bereich zwischen TableStart- und TableEnd-Feldern in den Seriendruckbereich aufgenommen werden soll. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [DeleteFields](../../aspose.words.mailmerging/mailmerge/deletefields/)() | Entfernt Serienbrieffelder aus dem Dokument. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_1)(DataRow) | Führt einen Seriendruck von einer DataRow in das Dokument durch. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_2)(DataTable) | Führt einen Seriendruck von einer DataTable in das Dokument durch. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_3)(DataView) | Führt einen Seriendruck von einer DataView in das Dokument durch. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_4)(IDataReader) | Führt den Seriendruck von IDataReader in das Dokument durch. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute)(IMailMergeDataSource) | Führt einen Seriendruck aus einer benutzerdefinierten Datenquelle durch. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_5)(string[], object[]) | Führt einen Seriendruckvorgang für einen einzelnen Datensatz durch. |
| [ExecuteADO](../../aspose.words.mailmerging/mailmerge/executeado/)(object) | Führt einen Seriendruck von einem ADO-Recordset-Objekt in das Dokument durch. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_2)(DataSet) | Führt den Seriendruck aus einem DataSet in ein Dokument mit Seriendruckbereichen durch. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_3)(DataTable) | Führt den Seriendruck aus einer DataTable in das Dokument mit Seriendruckbereichen durch. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_4)(DataView) | Führt den Seriendruck von einer DataView in das Dokument mit Seriendruckbereichen durch. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions)(IMailMergeDataSource) | Führt einen Seriendruck aus einer benutzerdefinierten Datenquelle mit Seriendruckregionen durch. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_1)(IMailMergeDataSourceRoot) | Führt einen Seriendruck aus einer benutzerdefinierten Datenquelle mit Seriendruckregionen durch. |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_5)(IDataReader, string) | Führt den Seriendruck von IDataReader in das Dokument mit Seriendruckbereichen durch. |
| [ExecuteWithRegionsADO](../../aspose.words.mailmerging/mailmerge/executewithregionsado/)(object, string) | Führt den Seriendruck von einem ADO-Recordset-Objekt in das Dokument mit Seriendruckbereichen durch. |
| [GetFieldNames](../../aspose.words.mailmerging/mailmerge/getfieldnames/)() | Gibt eine Sammlung von Serienbrieffeldnamen zurück, die im Dokument verfügbar sind. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion)(string) | Gibt eine Sammlung von Serienbrieffeldnamen zurück, die in der Region verfügbar sind. |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion_1)(string, int) | Gibt eine Sammlung von Serienbrieffeldnamen zurück, die in der Region verfügbar sind. |
| [GetRegionsByName](../../aspose.words.mailmerging/mailmerge/getregionsbyname/)(string) | Gibt eine Sammlung von Seriendruckregionen mit dem angegebenen Namen zurück. |
| [GetRegionsHierarchy](../../aspose.words.mailmerging/mailmerge/getregionshierarchy/)() | Gibt eine vollständige Hierarchie von Regionen (mit Feldern) zurück, die im Dokument verfügbar sind. |

### Bemerkungen

Damit der Seriendruckvorgang funktioniert, sollte das Dokument Word-MERGEFIELD- und -optionale NEXT-Felder enthalten. Während des Seriendruckvorgangs werden Seriendruckfelder im Dokument durch Werte aus Ihrer Datenquelle ersetzt.

Es gibt zwei verschiedene Möglichkeiten, den Seriendruck zu verwenden: mit Seriendruckbereichen und ohne.

Der einfachste Seriendruck ist ohne Bereiche und ähnelt sehr der Funktionsweise von Seriendruck in Word. VerwendenAusführen Methoden zum Zusammenführen von Informationen aus einigen Datenquellen wie z **Datentabelle** , **Datensatz** , **Datenansicht** , **IDataReader** oder ein Array von Objekten in Ihr Dokument. Die  **Seriendruck** Objekt verarbeitet alle Datensätze der Datenquelle und kopiert und fügt Inhalt des gesamten Dokuments für jeden Datensatz hinzu.

Beachten Sie, wann **Seriendruck**Objekt auf ein NEXT-Feld trifft, wählt es den nächsten Datensatz in der Datenquelle aus und fährt mit der Zusammenführung fort, ohne Inhalte zu kopieren.

VerwendenExecuteWithRegions Methoden zum Zusammenführen von Informationen in einem -Dokument mit definierten Seriendruckbereichen. Sie können verwenden **Datensatz** , **Datentabelle** , **Datenansicht** oder **IDataReader** als Datenquellen für diesen Vorgang.

Sie müssen Seriendruckbereiche verwenden, wenn Sie Teile innerhalb des -Dokuments dynamisch vergrößern möchten. Ohne Seriendruckbereiche wird das gesamte Dokument für jeden Datensatz von der Datenquelle wiederholt.

### Beispiele

Zeigt, wie ein Seriendruck mit Daten aus einer DataTable ausgeführt wird.

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // Im Folgenden finden Sie zwei Möglichkeiten, eine DataTable als Datenquelle für einen Seriendruck zu verwenden.
    // 1 - Verwenden Sie die gesamte Tabelle für den Seriendruck, um ein Ausgabe-Seriendruckdokument für jede Zeile in der Tabelle zu erstellen:
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - Verwenden Sie eine Zeile der Tabelle, um ein Seriendruckdokument zu erstellen:
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// Erstellt ein Seriendruck-Quelldokument.
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


