---
title: MappedDataFieldCollection.Clear
second_title: Aspose.Words für .NET-API-Referenz
description: MappedDataFieldCollection methode. Entfernt alle Elemente aus der Sammlung.
type: docs
weight: 40
url: /de/net/aspose.words.mailmerging/mappeddatafieldcollection/clear/
---
## MappedDataFieldCollection.Clear method

Entfernt alle Elemente aus der Sammlung.

```csharp
public void Clear()
```

### Beispiele

Zeigt, wie Datenspalten und MERGEFIELDs mit unterschiedlichen Namen zugeordnet werden, damit die Daten während eines Seriendrucks zwischen ihnen übertragen werden.

```csharp
public void MappedDataFieldCollection()
{
    Document doc = CreateSourceDocMappedDataFields();
    DataTable dataTable = CreateSourceTableMappedDataFields();

    // Die Tabelle hat eine Spalte namens "Column2", aber es gibt keine MERGEFIELDs mit diesem Namen.
    // Außerdem haben wir ein MERGEFIELD namens "Column3", aber die Datenquelle hat keine Spalte mit diesem Namen.
    // Wenn Daten aus "Spalte2" für das MERGEFIELD "Spalte3" geeignet sind,
    // Wir können diesen Spaltennamen dem MERGEFIELD im Schlüssel/Wert-Paar "MappedDataFields" zuordnen.
    MappedDataFieldCollection mappedDataFields = doc.MailMerge.MappedDataFields;

    // Wir können einen Datenquellen-Spaltennamen wie folgt mit einem MERGEFIELD-Namen verknüpfen.
    mappedDataFields.Add("MergeFieldName", "DataSourceColumnName");

    // Verknüpfen Sie die Datenquellenspalte mit dem Namen "Column2" mit MERGEFIELDs mit dem Namen "Column3".
    mappedDataFields.Add("Column3", "Column2");

    // Der MERGEFIELD-Name ist der "Schlüssel" zum jeweiligen Datenquellen-Spaltennamen "Wert".
    Assert.AreEqual("DataSourceColumnName", mappedDataFields["MergeFieldName"]);
    Assert.True(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.True(mappedDataFields.ContainsValue("DataSourceColumnName"));

    // Wenn wir nun diesen Seriendruck ausführen, nehmen die "Column3" MERGEFIELDs Daten aus "Column2" der Tabelle.
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
/// entsprechende Spalte in der Datentabelle aus der Methode unten.
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

* class [MappedDataFieldCollection](../)
* namensraum [Aspose.Words.MailMerging](../../mappeddatafieldcollection/)
* Montage [Aspose.Words](../../../)


