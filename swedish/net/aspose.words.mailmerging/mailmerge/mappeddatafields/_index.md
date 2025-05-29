---
title: MailMerge.MappedDataFields
linktitle: MappedDataFields
articleTitle: MappedDataFields
second_title: Aspose.Words för .NET
description: Upptäck egenskapen MailMerge MappedDataFields och få tillgång till en kraftfull samling mappade datafält för att enkelt förbättra dina dokumentkopplingsåtgärder.
type: docs
weight: 50
url: /sv/net/aspose.words.mailmerging/mailmerge/mappeddatafields/
---
## MailMerge.MappedDataFields property

Returnerar en samling som representerar mappade datafält för dokumentkopplingsoperationen.

```csharp
public MappedDataFieldCollection MappedDataFields { get; }
```

## Anmärkningar

Mappade datafält gör det möjligt att automatiskt mappa mellan namn på fält i din datakälla och namn på fält för koppling av dokument i dokumentet.

## Exempel

Visar hur man mappar datakolumner och MERGEFIELD-fält med olika namn så att data överförs mellan dem under en dokumentkoppling.

```csharp
public void MappedDataFieldCollection()
{
    Document doc = CreateSourceDocMappedDataFields();
    DataTable dataTable = CreateSourceTableMappedDataFields();

    // Tabellen har en kolumn med namnet "Kolumn2", men det finns inga MERGEFIELDS med det namnet.
    // Vi har också ett MERGEFIELD-fält med namnet "Kolumn3", men datakällan har ingen kolumn med det namnet.
    // Om data från "Kolumn2" passar för MERGEFIELD i "Kolumn3",
    // vi kan mappa det kolumnnamnet till MERGEFIELD i nyckel/värdeparet "MappedDataFields".
    MappedDataFieldCollection mappedDataFields = doc.MailMerge.MappedDataFields;

    // Vi kan länka ett kolumnnamn för en datakälla till ett MERGEFIELD-namn så här.
    mappedDataFields.Add("MergeFieldName", "DataSourceColumnName");

    // Länka datakällkolumnen med namnet "Kolumn2" till MERGEFIELDS med namnet "Kolumn3".
    mappedDataFields.Add("Column3", "Column2");

    // MERGEFIELD-namnet är "nyckeln" till respektive datakällkolumnnamn "värde".
    Assert.AreEqual("DataSourceColumnName", mappedDataFields["MergeFieldName"]);
    Assert.True(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.True(mappedDataFields.ContainsValue("DataSourceColumnName"));

    // Om vi nu kör denna koppling av dokument, kommer "Kolumn3" MERGEFIELDS att hämta data från "Kolumn2" i tabellen.
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.MappedDataFieldCollection.docx");

    // Vi kan iterera över elementen i den här samlingen.
    Assert.AreEqual(2, mappedDataFields.Count);

    using (IEnumerator<KeyValuePair<string, string>> enumerator = mappedDataFields.GetEnumerator())
        while (enumerator.MoveNext())
            Console.WriteLine(
                $"Column named {enumerator.Current.Value} is mapped to MERGEFIELDs named {enumerator.Current.Key}");

    // Vi kan också ta bort element från samlingen.
    mappedDataFields.Remove("MergeFieldName");

    Assert.False(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.False(mappedDataFields.ContainsValue("DataSourceColumnName"));

    mappedDataFields.Clear();

    Assert.AreEqual(0, mappedDataFields.Count);
}

/// <summary>
/// Skapa ett dokument med 2 MERGEFIELDS, varav en saknar en
/// motsvarande kolumn i datatabellen från metoden nedan.
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
/// Skapa en datatabell med 2 kolumner, varav en saknar
/// motsvarande MERGEFIELD i källdokumentet från metoden ovan.
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

### Se även

* class [MappedDataFieldCollection](../../mappeddatafieldcollection/)
* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)
