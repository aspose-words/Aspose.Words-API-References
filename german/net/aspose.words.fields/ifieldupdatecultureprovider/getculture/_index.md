---
title: IFieldUpdateCultureProvider.GetCulture
linktitle: GetCulture
articleTitle: GetCulture
second_title: Aspose.Words für .NET
description: IFieldUpdateCultureProvider GetCulture methode. Gibt a zurückCultureInfoObjekt das während der Feldaktualisierung verwendet werden soll in C#.
type: docs
weight: 10
url: /de/net/aspose.words.fields/ifieldupdatecultureprovider/getculture/
---
## IFieldUpdateCultureProvider.GetCulture method

Gibt a zurückCultureInfoObjekt, das während der Feldaktualisierung verwendet werden soll.

```csharp
public CultureInfo GetCulture(string culture, Field field)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| culture | String | Der Name der Kultur, die für das zu aktualisierende Feld angefordert wurde. |
| field | Field | Das Feld, das aktualisiert wird. |

### Rückgabewert

Das Kulturobjekt, das für die Aktualisierung des Feldes verwendet werden soll.

## Beispiele

Zeigt, wie man eine Kultur angibt, die die Datums-/Uhrzeitformatierung für jedes Feld analysiert.

```csharp
public void DefineDateTimeFormatting()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(FieldType.FieldTime, true);

    doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;

    // Legen Sie einen Anbieter fest, der ein für jedes Feld spezifisches Kulturobjekt zurückgibt.
    doc.FieldOptions.FieldUpdateCultureProvider = new FieldUpdateCultureProvider();

    FieldTime fieldDate = (FieldTime)doc.Range.Fields[0];
    if (fieldDate.LocaleId != (int)EditingLanguage.Russian)
        fieldDate.LocaleId = (int)EditingLanguage.Russian;

    doc.Save(ArtifactsDir + "FieldOptions.UpdateDateTimeFormatting.pdf");
}

/// <summary>
/// Stellt ein CultureInfo-Objekt bereit, das während der Aktualisierung eines Felds verwendet werden soll.
/// </summary>
private class FieldUpdateCultureProvider : IFieldUpdateCultureProvider
{
    /// <summary>
    /// Gibt ein CultureInfo-Objekt zurück, das während der Aktualisierung des Felds verwendet wird.
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

### Siehe auch

* class [Field](../../field/)
* interface [IFieldUpdateCultureProvider](../)
* namensraum [Aspose.Words.Fields](../../../aspose.words.fields/)
* Montage [Aspose.Words](../../../)
