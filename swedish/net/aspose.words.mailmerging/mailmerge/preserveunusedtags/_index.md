---
title: MailMerge.PreserveUnusedTags
linktitle: PreserveUnusedTags
articleTitle: PreserveUnusedTags
second_title: Aspose.Words för .NET
description: Upptäck egenskapen PreserveUnusedTags i MailMerge för att hantera oanvända mustaschtaggar effektivt och förbättra din dokumentautomatiseringsprocess.
type: docs
weight: 80
url: /sv/net/aspose.words.mailmerging/mailmerge/preserveunusedtags/
---
## MailMerge.PreserveUnusedTags property

Hämtar eller anger ett värde som anger om de oanvända "mustasch"-taggarna ska bevaras.

```csharp
public bool PreserveUnusedTags { get; set; }
```

## Anmärkningar

Standardvärdet är`falsk` .

## Exempel

Visar hur man bevarar utseendet på alternativa dokumentkopplingstaggar som inte används under en dokumentkoppling.

```csharp
public void PreserveUnusedTags(bool preserveUnusedTags)
{
    Document doc = CreateSourceDocWithAlternativeMergeFields();
    DataTable dataTable = CreateSourceTablePreserveUnusedTags();

     // Som standard placerar en dokumentkoppling data från varje rad i en tabell i MERGEFIELDS, som namnger kolumner i tabellen.
    // Vårt dokument har inga sådana fält, men det har klartexttaggar omgivna av klammerparenteser.
    // Om vi ställer in flaggan "PreserveUnusedTags" till "true" kan vi behandla dessa taggar som MERGEFIELDS
    // för att tillåta att vår dokumentkoppling infogar data från datakällan vid dessa taggar.
    // Om vi sätter flaggan "PreserveUnusedTags" till "false",
    // dokumentkopplingen konverterar dessa taggar till MERGEFIELDS och lämnar dem ofyllda.
    doc.MailMerge.PreserveUnusedTags = preserveUnusedTags;
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.PreserveUnusedTags.docx");

    // Vårt dokument har en tagg för en kolumn med namnet "Kolumn2", som inte finns i tabellen.
    // Om vi sätter flaggan "PreserveUnusedTags" till "false", then the mail merge will convert this tag into a MERGEFIELD.
    Assert.AreEqual(doc.GetText().Contains("{{ Column2 }}"), preserveUnusedTags);

    if (preserveUnusedTags)
        Assert.AreEqual(0, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
    else
        Assert.AreEqual(1, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
}

/// <summary>
/// Skapa ett dokument och lägg till två klartexttaggar som kan fungera som MERGEFIELDS under en dokumentkoppling.
/// </summary>
private static Document CreateSourceDocWithAlternativeMergeFields()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("{{ Column1 }}");
    builder.Writeln("{{ Column2 }}");

    // Våra taggar registreras endast som destinationer för dokumentkopplingsdata om vi ställer in detta till sant.
    doc.MailMerge.UseNonMergeFields = true;

    return doc;
}

/// <summary>
/// Skapa en enkel datatabell med en kolumn.
/// </summary>
private static DataTable CreateSourceTablePreserveUnusedTags()
{
    DataTable dataTable = new DataTable("MyTable");
    dataTable.Columns.Add("Column1");
    dataTable.Rows.Add(new object[] { "Value1" });

    return dataTable;
}
```

### Se även

* property [UseNonMergeFields](../usenonmergefields/)
* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)
