---
title: FieldAutoNumLgl.SeparatorCharacter
second_title: Aspose.Words för .NET API Referens
description: FieldAutoNumLgl fast egendom. Hämtar eller ställer in avgränsningstecknet som ska användas.
type: docs
weight: 30
url: /sv/net/aspose.words.fields/fieldautonumlgl/separatorcharacter/
---
## FieldAutoNumLgl.SeparatorCharacter property

Hämtar eller ställer in avgränsningstecknet som ska användas.

```csharp
public string SeparatorCharacter { get; set; }
```

### Exempel

Visar hur man organiserar ett dokument med AUTONUMLGL-fält.

```csharp
public void FieldAutoNumLgl()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    const string fillerText = "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
                              "\nUt enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. ";

    // AUTONUMLGL-fält visar ett tal som ökar vid varje AUTONUMLGL-fält inom dess aktuella rubriknivå.
    // Dessa fält har en separat räkning för varje rubriknivå,
     // och varje fält visar också AUTONUMLGL-fältantalet för alla rubriknivåer under sina egna.
    // Genom att ändra räkningen för någon rubriknivå återställs räkningen för alla nivåer över den nivån till 1.
    // Detta gör att vi kan organisera vårt dokument i form av en översiktslista.
    // Detta är det första AUTONUMLGL-fältet på en rubriknivå på 1, som visar "1." i dokumentet.
    InsertNumberedClause(builder, "\tHeading 1", fillerText, StyleIdentifier.Heading1);

    // Detta är det andra AUTONUMLGL-fältet på en rubriknivå på 1, så det kommer att visa "2.".
    InsertNumberedClause(builder, "\tHeading 2", fillerText, StyleIdentifier.Heading1);

    // Detta är det första AUTONUMLGL-fältet på en rubriknivå på 2,
    // och AUTONUMLGL-räkningen för rubriknivån under den är "2", så det kommer att visa "2.1.".
    InsertNumberedClause(builder, "\tHeading 3", fillerText, StyleIdentifier.Heading2);

     // Detta är det första AUTONUMLGL-fältet på en rubriknivå på 3.
    // Arbetar på samma sätt som fältet ovan kommer det att visa "2.1.1.".
    InsertNumberedClause(builder, "\tHeading 4", fillerText, StyleIdentifier.Heading3);

    // Detta fält har en rubriknivå på 2, och dess respektive AUTONUMLGL-antal är på 2, så fältet kommer att visa "2.2.".
    InsertNumberedClause(builder, "\tHeading 5", fillerText, StyleIdentifier.Heading2);

    // Öka antalet AUTONUMLGL för en rubriknivå under denna
    // har återställt räkningen för denna nivå så att detta fält kommer att visa "2.2.1.".
    InsertNumberedClause(builder, "\tHeading 6", fillerText, StyleIdentifier.Heading3);

    foreach (FieldAutoNumLgl field in doc.Range.Fields.Where(f => f.Type == FieldType.FieldAutoNumLegal))
    {
        // Skiljetecknet, som visas i fältresultatet omedelbart efter numret,
        // är ett punkt som standard. Om vi lämnar denna egenskap null,
        // vårt senaste AUTONUMLGL-fält kommer att visa "2.2.1." i dokumentet.
        Assert.IsNull(field.SeparatorCharacter);

        // Ställa in en anpassad separator och ta bort den avslutande perioden
        // kommer att ändra fältets utseende från "2.2.1." till "2:2:1".
        // Vi kommer att tillämpa detta på alla fält som vi har skapat.
        field.SeparatorCharacter = ":";
        field.RemoveTrailingPeriod = true;
        Assert.AreEqual(" AUTONUMLGL  \\s : \\e", field.GetFieldCode());
    }

    doc.Save(ArtifactsDir + "Field.AUTONUMLGL.docx");
}

/// <summary>
/// Använder en dokumentbyggare för att infoga en sats numrerad med ett AUTONUMLGL-fält.
/// </summary>
private static void InsertNumberedClause(DocumentBuilder builder, string heading, string contents, StyleIdentifier headingStyle)
{
    builder.InsertField(FieldType.FieldAutoNumLegal, true);
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = headingStyle;
    builder.Writeln(heading);

    // Den här texten kommer att tillhöra det juridiska autonummerfältet ovanför.
    // Det kommer att kollapsa när vi klickar på pilen bredvid motsvarande AUTONUMLGL-fält i Microsoft Word.
    builder.CurrentParagraph.ParagraphFormat.StyleIdentifier = StyleIdentifier.BodyText;
    builder.Writeln(contents);
}
```

### Se även

* class [FieldAutoNumLgl](../)
* namnutrymme [Aspose.Words.Fields](../../fieldautonumlgl/)
* hopsättning [Aspose.Words](../../../)


