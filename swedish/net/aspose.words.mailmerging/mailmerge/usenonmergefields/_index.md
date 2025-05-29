---
title: MailMerge.UseNonMergeFields
linktitle: UseNonMergeFields
articleTitle: UseNonMergeFields
second_title: Aspose.Words för .NET
description: Släpp lös kraften i MailMerge! Använd egenskapen UseNonMergeFields för att förbättra dina dokument genom att sömlöst sammanfoga dem till olika fälttyper.
type: docs
weight: 150
url: /sv/net/aspose.words.mailmerging/mailmerge/usenonmergefields/
---
## MailMerge.UseNonMergeFields property

När`sann` , anger att utöver MERGEFIELD-fält utförs dokumentkoppling i vissa andra typer av fält och även i "{{fieldName}}"-taggar.

```csharp
public bool UseNonMergeFields { get; set; }
```

## Anmärkningar

Normalt sett utförs dokumentkoppling endast i MERGEFIELD-fält, men flera kunder har byggt sina reporting med hjälp av andra fält och har skapat många dokument på det här sättet. För att förenkla migreringen (och eftersom denna -metod användes oberoende av varandra av flera kunder) introducerades möjligheten att koppla dokument till andra fält.

När`UseNonMergeFields` är inställd på`sann`Aspose.Words kommer att utföra dokumentkopplingar i följande fält:

MERGEFIELD Fältnamn

MAKROKNAPP NOMACRO Fältnamn

OM 0 = 0 "{Fältnamn}" ""

Även när`UseNonMergeFields` är inställd på`sann`Aspose.Words kommer att utföra dokumentkoppling till text tags "{{fieldName}}". Dessa är inte fält, utan bara texttaggar.

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

* class [MailMerge](../)
* namnutrymme [Aspose.Words.MailMerging](../../../aspose.words.mailmerging/)
* hopsättning [Aspose.Words](../../../)
