---
title: IFieldUpdateCultureProvider.GetCulture
linktitle: GetCulture
articleTitle: GetCulture
second_title: Aspose.Words för .NET
description: Upptäck iFieldUpdateCultureProviders GetCulture-metod, som effektivt returnerar ett CultureInfo-objekt för sömlösa fältuppdateringar.
type: docs
weight: 10
url: /sv/net/aspose.words.fields/ifieldupdatecultureprovider/getculture/
---
## IFieldUpdateCultureProvider.GetCulture method

Returnerar enCultureInfo objekt som ska användas under fältuppdateringen.

```csharp
public CultureInfo GetCulture(string culture, Field field)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| culture | String | Namnet på den kultur som begärs för fältet som uppdateras. |
| field | Field | Fältet uppdateras. |

### Returvärde

Kulturobjektet som ska användas för fältets uppdatering.

## Exempel

Visar hur man anger en kultur som tolkar datum-/tidsformatering för varje fält.

```csharp
public void DefineDateTimeFormatting()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(FieldType.FieldTime, true);

    doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;

    // Ange en provider som returnerar ett kulturobjekt specifikt för varje fält.
    doc.FieldOptions.FieldUpdateCultureProvider = new FieldUpdateCultureProvider();

    FieldTime fieldDate = (FieldTime)doc.Range.Fields[0];
    if (fieldDate.LocaleId != (int)EditingLanguage.Russian)
        fieldDate.LocaleId = (int)EditingLanguage.Russian;

    doc.Save(ArtifactsDir + "FieldOptions.UpdateDateTimeFormatting.pdf");
}

/// <summary>
/// Tillhandahåller ett CultureInfo-objekt som ska användas vid uppdatering av ett fält.
/// </summary>
private class FieldUpdateCultureProvider : IFieldUpdateCultureProvider
{
    /// <summary>
    /// Returnerar ett CultureInfo-objekt som ska användas under fältets uppdatering.
    /// </summary>
    public CultureInfo GetCulture(string name, Field field)
    {
        switch (name)
        {
            case "ru-RU":
                CultureInfo culture = new CultureInfo(name, false);
                DateTimeFormatInfo format = culture.DateTimeFormat;

                format.MonthNames = new[] { "месяц 1", "месяц 2", "месяц 3", "месяц 4", "месяц 5", "месяц 6", "месяц 7", "месяц 8", "месяц 9", "месяц 10", "месяц 11", "месяц 12", "" };
                format.MonthGenitiveNames = format.MonthNames;
                format.AbbreviatedMonthNames = new[] { "мес 1", "мес 2", "мес 3", "мес 4", "мес 5", "мес 6", "мес 7", "мес 8", "мес 9", "мес 10", "мес 11", "мес 12", "" };
                format.AbbreviatedMonthGenitiveNames = format.AbbreviatedMonthNames;

                format.DayNames = new[] { "день недели 7", "день недели 1", "день недели 2", "день недели 3", "день недели 4", "день недели 5", "день недели 6" };
                format.AbbreviatedDayNames = new[] { "день 7", "день 1", "день 2", "день 3", "день 4", "день 5", "день 6" };
                format.ShortestDayNames = new[] { "д7", "д1", "д2", "д3", "д4", "д5", "д6" };

                format.AMDesignator = "До полудня";
                format.PMDesignator = "После полудня";

                const string pattern = "yyyy MM (MMMM) dd (dddd) hh:mm:ss tt";
                format.LongDatePattern = pattern;
                format.LongTimePattern = pattern;
                format.ShortDatePattern = pattern;
                format.ShortTimePattern = pattern;

                return culture;
            case "en-US":
                return new CultureInfo(name, false);
            default:
                return null;
        }
    }
}
```

### Se även

* class [Field](../../field/)
* interface [IFieldUpdateCultureProvider](../)
* namnutrymme [Aspose.Words.Fields](../../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../../)
