---
title: MappedDataFieldCollection.ContainsKey
linktitle: ContainsKey
articleTitle: ContainsKey
second_title: Aspose.Words für .NET
description: Ermitteln Sie mit der ContainsKey-Methode, ob eine bestimmte Dokumentfeldzuordnung in MappedDataFieldCollection vorhanden ist. Optimieren Sie mühelos Ihr Datenmanagement!
type: docs
weight: 50
url: /de/net/aspose.words.mailmerging/mappeddatafieldcollection/containskey/
---
## MappedDataFieldCollection.ContainsKey method

Bestimmt, ob eine Zuordnung des angegebenen Felds im Dokument in der Sammlung vorhanden ist.

```csharp
public bool ContainsKey(string documentFieldName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| documentFieldName | String | Groß- und Kleinschreibung beachtender Name des Serienbrieffelds im Dokument. |

### Rückgabewert

`WAHR`wenn das Element in der Sammlung gefunden wird; andernfalls`FALSCH`.

## Beispiele

Zeigt, wie Datenspalten und MERGEFIELDs mit unterschiedlichen Namen zugeordnet werden, sodass die Daten während eines Seriendrucks zwischen ihnen übertragen werden.

```csharp
public void MappedDataFieldCollection()
{
    Document doc = CreateSourceDocMappedDataFields();
    DataTable dataTable = CreateSourceTableMappedDataFields();

    // Die Tabelle hat eine Spalte mit dem Namen „Column2“, aber es gibt keine MERGEFIELDs mit diesem Namen.
    // Außerdem haben wir ein MERGEFIELD mit dem Namen „Column3“, aber die Datenquelle hat keine Spalte mit diesem Namen.
    // Wenn Daten aus "Column2" für das MERGEFIELD "Column3" geeignet sind,
    // Wir können diesen Spaltennamen dem MERGEFIELD im Schlüssel-/Wertpaar „MappedDataFields“ zuordnen.
    MappedDataFieldCollection mappedDataFields = doc.MailMerge.MappedDataFields;

    // Wir können einen Datenquellenspaltennamen wie folgt mit einem MERGEFIELD-Namen verknüpfen.
    mappedDataFields.Add("MergeFieldName", "DataSourceColumnName");

    // Verknüpfen Sie die Datenquellenspalte mit dem Namen „Column2“ mit MERGEFIELDs mit dem Namen „Column3“.
    mappedDataFields.Add("Column3", "Column2");

    // Der MERGEFIELD-Name ist der „Schlüssel“ zum jeweiligen Datenquellenspaltennamen „Wert“.
    Assert.AreEqual("DataSourceColumnName", mappedDataFields["MergeFieldName"]);
    Assert.True(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.True(mappedDataFields.ContainsValue("DataSourceColumnName"));

    // Wenn wir jetzt diesen Seriendruck ausführen, übernehmen die MERGEFIELDs „Spalte3“ Daten aus „Spalte2“ der Tabelle.
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
/// Erstellen Sie ein Dokument mit 2 MERGEFIELDs, von denen eines kein
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
/// Erstellen Sie eine Datentabelle mit 2 Spalten, von denen eine keine
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

* class [MappedDataFieldCollection](../)
* namensraum [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* Montage [Aspose.Words](../../../)
