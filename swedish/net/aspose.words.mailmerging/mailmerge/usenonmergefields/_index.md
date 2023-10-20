---
title: MailMerge.UseNonMergeFields
linktitle: UseNonMergeFields
articleTitle: UseNonMergeFields
second_title: Aspose.Words för .NET
description: MailMerge UseNonMergeFields fast egendom. NärSann  anger att förutom MERGEFIELDfält utförs epostsammankoppling till vissa andra typer av fält och även i fieldNametaggar i C#.
type: docs
weight: 150
url: /sv/net/aspose.words.mailmerging/mailmerge/usenonmergefields/
---
## MailMerge.UseNonMergeFields property

När`Sann` , anger att förutom MERGEFIELD-fält utförs e-postsammankoppling till vissa andra typer av fält och även i "{{fieldName}}"-taggar.

```csharp
public bool UseNonMergeFields { get; set; }
```

## Anmärkningar

Normalt utförs brevkoppling endast i MERGEFIELD-fält, men flera kunder hade sin reporting byggd med andra fält och hade många dokument skapade på detta sätt. För att förenkla migreringen (och eftersom detta tillvägagångssätt användes oberoende av flera kunder) introducerades möjligheten att sammanfoga e-post till andra fält.

När`UseNonMergeFields` är satt till`Sann`, kommer Aspose.Words att utföra e-postsammanfogning i följande fält:

MERGEFIELD Fältnamn

MACROBUTTON NOMACRO Fältnamn

OM 0 = 0 "{FieldName}" ""

Även när`UseNonMergeFields` är satt till`Sann`, Aspose.Words kommer att utföra e-postsammanfogning till texttaggar "{{fieldName}}". Det här är inte fält, utan bara texttaggar.

## Exempel

Visar hur man bevarar utseendet på alternativa kopplingsetiketter som inte används under en koppling.

```csharp
public void PreserveUnusedTags(bool preserveUnusedTags)
{
    Document doc = CreateSourceDocWithAlternativeMergeFields();
    DataTable dataTable = CreateSourceTablePreserveUnusedTags();

     // Som standard placerar en brevkoppling data från varje rad i en tabell i MERGEFIELDs, vilka namnger kolumner i den tabellen.
    // Vårt dokument har inga sådana fält, men det har klartext-taggar omgivna av hängslen.
    // Om vi ställer in flaggan "PreserveUnusedTags" till "true", kan vi behandla dessa taggar som MERGEFIELDs
    // för att tillåta vår e-postsammanfogning för att infoga data från datakällan vid dessa taggar.
    // Om vi sätter "PreserveUnusedTags"-flaggan till "false",
    // sammanslagningen kommer att konvertera dessa taggar till MERGEFIELDs och lämna dem ofyllda.
    doc.MailMerge.PreserveUnusedTags = preserveUnusedTags;
    doc.MailMerge.Execute(dataTable);

    doc.Save(ArtifactsDir + "MailMerge.PreserveUnusedTags.docx");

    // Vårt dokument har en tagg för en kolumn som heter "Column2", som inte finns i tabellen.
    // Om vi sätter "PreserveUnusedTags"-flaggan till "false", then the mail merge will convert this tag into a MERGEFIELD.
    Assert.AreEqual(doc.GetText().Contains("{{ Column2 }}"), preserveUnusedTags);

    if (preserveUnusedTags)
        Assert.AreEqual(0, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
    else
        Assert.AreEqual(1, doc.Range.Fields.Count(f => f.Type == FieldType.FieldMergeField));
}

/// <summary>
/// Skapa ett dokument och lägg till två klartext-taggar som kan fungera som MERGEFIELDs under en e-postkoppling.
/// </summary>
private static Document CreateSourceDocWithAlternativeMergeFields()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("{{ Column1 }}");
    builder.Writeln("{{ Column2 }}");

    // Våra taggar registreras som destinationer för kopplingsdata endast om vi ställer in detta på sant.
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
