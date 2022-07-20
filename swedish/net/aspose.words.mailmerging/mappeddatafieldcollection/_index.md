---
title: MappedDataFieldCollection
second_title: Aspose.Words för .NET API Referens
description: Gör det möjligt att automatiskt mappa mellan namn på fält i din datakälla och namn på sammanslagningsfält i dokumentet.
type: docs
weight: 3650
url: /sv/net/aspose.words.mailmerging/mappeddatafieldcollection/
---
## MappedDataFieldCollection class

Gör det möjligt att automatiskt mappa mellan namn på fält i din datakälla och namn på sammanslagningsfält i dokumentet.

```csharp
public class MappedDataFieldCollection : IEnumerable<KeyValuePair<string, string>>
```

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [Count](../../aspose.words.mailmerging/mappeddatafieldcollection/count) { get; } | Hämtar antalet element som finns i samlingen. |
| [Item](../../aspose.words.mailmerging/mappeddatafieldcollection/item) { get; set; } | Hämtar eller ställer in namnet på fältet i datakällan som är kopplad till det angivna kopplingsfältet. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Add](../../aspose.words.mailmerging/mappeddatafieldcollection/add)(string, string) | Lägger till en ny fältmappning. |
| [Clear](../../aspose.words.mailmerging/mappeddatafieldcollection/clear)() | Tar bort alla element från samlingen. |
| [ContainsKey](../../aspose.words.mailmerging/mappeddatafieldcollection/containskey)(string) | Bestämmer om en mappning från det angivna fältet i dokumentet finns i samlingen. |
| [ContainsValue](../../aspose.words.mailmerging/mappeddatafieldcollection/containsvalue)(string) | Bestämmer om en mappning från det angivna fältet i datakällan finns i samlingen. |
| [GetEnumerator](../../aspose.words.mailmerging/mappeddatafieldcollection/getenumerator)() | Returnerar ett ordboksuppräkningsobjekt som kan användas för att iterera över alla objekt i samlingen. |
| [Remove](../../aspose.words.mailmerging/mappeddatafieldcollection/remove)(string) | Tar bort en fältmappning. |

### Anmärkningar

Detta implementeras som en samling strängnycklar i strängvärden. Nycklarna är namnen på kopplingsfälten i dokumentet och värdena är namnen på fälten i din datakälla.

### Exempel

Visar hur man mappar datakolumner och MERGEFIELDs med olika namn så att data överförs mellan dem under en sammankoppling.

```csharp
public void MappedDataFieldCollection()
{
    Document doc = CreateSourceDocMappedDataFields();
    DataTable dataTable = CreateSourceTableMappedDataFields();

    // Tabellen har en kolumn som heter "Column2", men det finns inga MERGEFIELDs med det namnet.
    // Dessutom har vi ett MERGEFIELD som heter "Column3", men datakällan har inte en kolumn med det namnet.
    // Om data från "Column2" är lämplig för "Column3" MERGEFIELD,
    // vi kan mappa det kolumnnamnet till MERGEFIELD i nyckel/värdeparet "MappedDataFields".
    MappedDataFieldCollection mappedDataFields = doc.MailMerge.MappedDataFields;

    // Vi kan länka ett datakällas kolumnnamn till ett MERGEFIELD-namn som detta.
    mappedDataFields.Add("MergeFieldName", "DataSourceColumnName");

    // Länka datakällans kolumn med namnet "Column2" till MERGEFIELDs med namnet "Column3".
    mappedDataFields.Add("Column3", "Column2");

    // MERGEFIELD-namnet är "nyckeln" till respektive datakällas kolumnnamn "värde".
    Assert.AreEqual("DataSourceColumnName", mappedDataFields["MergeFieldName"]);
    Assert.True(mappedDataFields.ContainsKey("MergeFieldName"));
    Assert.True(mappedDataFields.ContainsValue("DataSourceColumnName"));

    // Om vi nu kör den här kopplingen, kommer "Column3" MERGEFIELDs att ta data från "Column2" i tabellen.
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.MappedDataFieldCollection.docx");

    // Vi kan iterera över elementen i denna samling.
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
/// Skapa ett dokument med 2 MERGEFIELDs, varav ett inte har en
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
/// Skapa en datatabell med 2 kolumner, varav en inte har en
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

* namnutrymme [Aspose.Words.MailMerging](../../aspose.words.mailmerging)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
