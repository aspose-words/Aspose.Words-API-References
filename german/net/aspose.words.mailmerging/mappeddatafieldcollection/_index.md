---
title: MappedDataFieldCollection Class
linktitle: MappedDataFieldCollection
articleTitle: MappedDataFieldCollection
second_title: Aspose.Words für .NET
description: Aspose.Words.MailMerging.MappedDataFieldCollection klas. Ermöglicht die automatische Zuordnung zwischen Namen von Feldern in Ihrer Datenquelle und Namen von Serienbrieffeldern im Dokument in C#.
type: docs
weight: 3870
url: /de/net/aspose.words.mailmerging/mappeddatafieldcollection/
---
## MappedDataFieldCollection class

Ermöglicht die automatische Zuordnung zwischen Namen von Feldern in Ihrer Datenquelle und Namen von Serienbrieffeldern im Dokument.

Um mehr zu erfahren, besuchen Sie die[Serienbrief und Berichterstellung](https://docs.aspose.com/words/net/mail-merge-and-reporting/) Dokumentationsartikel.

```csharp
public class MappedDataFieldCollection : IEnumerable<KeyValuePair<string, string>>
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [Count](../../aspose.words.mailmerging/mappeddatafieldcollection/count/) { get; } | Ruft die Anzahl der in der Sammlung enthaltenen Elemente ab. |
| [Item](../../aspose.words.mailmerging/mappeddatafieldcollection/item/) { get; set; } | Ruft den Namen des Felds in der Datenquelle ab, die dem angegebenen Serienbrieffeld zugeordnet ist, oder legt diesen fest. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Add](../../aspose.words.mailmerging/mappeddatafieldcollection/add/)(*string, string*) | Fügt eine neue Feldzuordnung hinzu. |
| [Clear](../../aspose.words.mailmerging/mappeddatafieldcollection/clear/)() | Entfernt alle Elemente aus der Sammlung. |
| [ContainsKey](../../aspose.words.mailmerging/mappeddatafieldcollection/containskey/)(*string*) | Bestimmt, ob eine Zuordnung aus dem angegebenen Feld im Dokument in der Sammlung vorhanden ist. |
| [ContainsValue](../../aspose.words.mailmerging/mappeddatafieldcollection/containsvalue/)(*string*) | Bestimmt, ob eine Zuordnung aus dem angegebenen Feld in der Datenquelle in der Sammlung vorhanden ist. |
| [GetEnumerator](../../aspose.words.mailmerging/mappeddatafieldcollection/getenumerator/)() | Gibt ein Wörterbuch-Enumeratorobjekt zurück, das zum Durchlaufen aller Elemente in der Sammlung verwendet werden kann. |
| [Remove](../../aspose.words.mailmerging/mappeddatafieldcollection/remove/)(*string*) | Entfernt eine Feldzuordnung. |

## Bemerkungen

Dies wird als Sammlung von Zeichenfolgenschlüsseln in Zeichenfolgenwerte implementiert. Die Schlüssel sind die Namen der Serienbrieffelder im Dokument und die Werte sind die Namen der Felder in Ihrer Datenquelle.

## Beispiele

Zeigt, wie Datenspalten und MERGEFIELDs mit unterschiedlichen Namen zugeordnet werden, damit die Daten während eines Seriendrucks zwischen ihnen übertragen werden.

```csharp
public void MappedDataFieldCollection()
{
    Document doc = CreateSourceDocMappedDataFields();
    DataTable dataTable = CreateSourceTableMappedDataFields();

    // Die Tabelle hat eine Spalte mit dem Namen „Column2“, aber es gibt keine MERGEFIELDs mit diesem Namen.
    // Außerdem haben wir ein MERGEFIELD namens „Column3“, aber die Datenquelle hat keine Spalte mit diesem Namen.
    // Wenn Daten aus „Spalte2“ für das MERGEFIELD „Spalte3“ geeignet sind,
    // Wir können diesen Spaltennamen dem MERGEFIELD im Schlüssel/Wert-Paar „MappedDataFields“ zuordnen.
    MappedDataFieldCollection mappedDataFields = doc.MailMerge.MappedDataFields;

    // Wir können den Namen einer Datenquellenspalte wie folgt mit einem MERGEFIELD-Namen verknüpfen.
    mappedDataFields.Add("MergeFieldName", "DataSourceColumnName");

    // Verknüpfen Sie die Datenquellenspalte mit dem Namen „Column2“ mit MERGEFIELDs mit dem Namen „Column3“.
    mappedDataFields.Add("Column3", "Column2");

    // Der MERGEFIELD-Name ist der „Schlüssel“ zum jeweiligen Datenquellenspaltennamen „Wert“.
    Assert.AreEqual("DataSourceColumnName", mappedDataFields["MergeFieldName"]);
    Assert.True(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.True(mappedDataFields.ContainsValue("DataSourceColumnName"));

    // Wenn wir nun diesen Serienbrief ausführen, übernehmen die MERGEFIELDs „Spalte3“ Daten aus „Spalte2“ der Tabelle.
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.MappedDataFieldCollection.docx");

    // Wir können die Elemente in dieser Sammlung durchlaufen.
    Assert.AreEqual(2, mappedDataFields.Count);

    using (IEnumerator<KeyValuePair<string, string>> enumerator = mappedDataFields.GetEnumerator())
        while (enumerator.MoveNext())
            Console.WriteLine(
                $"Column named {enumerator.Current.Value} is mapped to MERGEFIELDs named {enumerator.Current.Key}");

    // Wir können auch Elemente aus der Sammlung entfernen.
    mappedDataFields.Remove("MergeFieldName");

    Assert.False(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.False(mappedDataFields.ContainsValue("DataSourceColumnName"));

    mappedDataFields.Clear();

    Assert.AreEqual(0, mappedDataFields.Count);
}

/// <summary>
/// Erstellen Sie ein Dokument mit 2 MERGEFIELDs, von denen eines kein hat
/// entsprechende Spalte in der Datentabelle aus der folgenden Methode.
/// </summary>
private static Document CreateSourceDocMappedDataFields()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD Column1");
    builder.Write(", ");
    builder.InsertField(" MERGEFIELD Column3");

    return doc;
}

/// <summary>
/// Erstellen Sie eine Datentabelle mit 2 Spalten, von denen eine keine hat
/// entsprechendes MERGEFIELD im Quelldokument aus der obigen Methode.
/// </summary>
private static DataTable CreateSourceTableMappedDataFields()
{
    DataTable dataTable = new DataTable("MyTable");
    dataTable.Columns.Add("Column1");
    dataTable.Columns.Add("Column2");
    dataTable.Rows.Add(new object[] { "Value1", "Value2" });

    return dataTable;
}
```

### Siehe auch

* namensraum [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../)
