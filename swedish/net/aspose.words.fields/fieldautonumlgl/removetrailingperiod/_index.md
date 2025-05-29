---
title: FieldAutoNumLgl.RemoveTrailingPeriod
linktitle: RemoveTrailingPeriod
articleTitle: RemoveTrailingPeriod
second_title: Aspose.Words för .NET
description: Hantera egenskapen RemoveTrailingPeriod i FieldAutoNumLgl för att anpassa talvisning – eliminera efterföljande punkter för en renare och professionellare formatering.
type: docs
weight: 20
url: /sv/net/aspose.words.fields/fieldautonumlgl/removetrailingperiod/
---
## FieldAutoNumLgl.RemoveTrailingPeriod property

Hämtar eller anger om talet ska visas utan en avslutande punkt.

```csharp
public bool RemoveTrailingPeriod { get; set; }
```

## Exempel

Visar hur man organiserar ett dokument med hjälp av AUTONUMLGL-fält.

```csharp
public void FieldAutoNumLgl()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    const string fillerText = "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
                              "\nUt enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. ";

    // AUTONUMLGL-fält visar ett tal som ökar vid varje AUTONUMLGL-fält inom dess aktuella rubriknivå.
    // Dessa fält har en separat räkning för varje rubriknivå,
     // och varje fält visar även AUTONUMLGL-fältets antal för alla rubriknivåer under det egna.
    // Om du ändrar antalet för en rubriknivå återställs antalet för alla nivåer ovanför den nivån till 1.
    // Detta låter oss organisera vårt dokument i form av en dispositionslista.
    // Detta är det första AUTONUMLGL-fältet på rubriknivå 1, som visar "1." i dokumentet.
    InsertNumberedClause(builder, "\tHeading 1", fillerText, StyleIdentifier.Heading1);

    // Detta är det andra AUTONUMLGL-fältet på rubriknivå 1, så det kommer att visa "2.".
    InsertNumberedClause(builder, "\tHeading 2", fillerText, StyleIdentifier.Heading1);

    // Detta är det första AUTONUMLGL-fältet på rubriknivå 2,
    // och AUTONUMLGL-räkningen för rubriknivån under den är "2", så den kommer att visa "2.1.".
    InsertNumberedClause(builder, "\tHeading 3", fillerText, StyleIdentifier.Heading2);

     // Detta är det första AUTONUMLGL-fältet på rubriknivå 3.
    // Genom att arbeta på samma sätt som fältet ovan kommer det att visa "2.1.1.".
    InsertNumberedClause(builder, "\tHeading 4", fillerText, StyleIdentifier.Heading3);

    // Det här fältet har rubriknivå 2, och dess respektive AUTONUMLGL-antal är 2, så fältet kommer att visa "2.2.".
    InsertNumberedClause(builder, "\tHeading 5", fillerText, StyleIdentifier.Heading2);

    // Ökar antalet AUTONUMLGL för en rubriknivå under denna
    // har återställt räknaren för denna nivå så att det här fältet visar "2.2.1.".
    InsertNumberedClause(builder, "\tHeading 6", fillerText, StyleIdentifier.Heading3);

    foreach (FieldAutoNumLgl field in doc.Range.Fields.Where(f => f.Type == FieldType.FieldAutoNumLegal).ToList())
    {
        // Avgränsartecknet, som visas i fältresultatet omedelbart efter numret,
        // är en punkt som standard. Om vi lämnar den här egenskapen null,
        // vårt sista AUTONUMLGL-fält kommer att visa "2.2.1." i dokumentet.
        Assert.IsNull(field.SeparatorCharacter);

        // Ställa in ett anpassat avgränsningstecken och ta bort den avslutande punkten
        // ändrar fältets utseende från "2.2.1." till "2:2:1".
        // Vi kommer att tillämpa detta på alla fält som vi har skapat.
        field.SeparatorCharacter = ":";
        field.RemoveTrailingPeriod = true;
        Assert.AreEqual(" AUTONUMLGL  \\s : \\e", field.GetFieldCode());
    }

    doc.Save(ArtifactsDir + "Field.AUTONUMLGL.docx");
}

/// <summary>
/// Använder en dokumentbyggare för att infoga en klausul numrerad av ett AUTONUMLGL-fält.
/// </summary>
private static void InsertNumberedClause(DocumentBuilder builder, string heading, string contents, StyleIdentifier headingStyle)
{
    builder.InsertField(FieldType.FieldAutoNumLegal, true);
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = headingStyle;
    builder.Writeln(heading);

    // Denna text kommer att tillhöra fältet auto num legal ovanför.
    // Den kommer att fällas ihop när vi klickar på pilen bredvid motsvarande AUTONUMLGL-fält i Microsoft Word.
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = StyleIdentifier.BodyText;
    builder.Writeln(contents);
}
```

### Se även

* class [FieldAutoNumLgl](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
