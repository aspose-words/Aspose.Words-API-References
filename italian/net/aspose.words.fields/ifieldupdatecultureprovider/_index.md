---
title: IFieldUpdateCultureProvider Interface
linktitle: IFieldUpdateCultureProvider
articleTitle: IFieldUpdateCultureProvider
second_title: Aspose.Words per .NET
description: Scopri l'interfaccia Aspose.Words.Fields.IFieldUpdateCultureProvider. Migliora gli aggiornamenti dei campi con un oggetto CultureInfo personalizzabile per una localizzazione precisa.
type: docs
weight: 3120
url: /it/net/aspose.words.fields/ifieldupdatecultureprovider/
---
## IFieldUpdateCultureProvider interface

Quando implementato, fornisce unCultureInfo oggetto che dovrebbe essere utilizzato durante l'aggiornamento di un campo particolare.

```csharp
public interface IFieldUpdateCultureProvider
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| [GetCulture](../../aspose.words.fields/ifieldupdatecultureprovider/getculture/)(*string, [Field](../field/)*) | Restituisce unCultureInfo oggetto da utilizzare durante l'aggiornamento del campo. |

## Esempi

Mostra come specificare una cultura che analizza la formattazione di data/ora per ogni campo.

```csharp
public void DefineDateTimeFormatting()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(FieldType.FieldTime, true);

    doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;

    // Imposta un provider che restituisce un oggetto cultura specifico per ciascun campo.
    doc.FieldOptions.FieldUpdateCultureProvider = new FieldUpdateCultureProvider();

    FieldTime fieldDate = (FieldTime)doc.Range.Fields[0];
    if (fieldDate.LocaleId != (int)EditingLanguage.Russian)
        fieldDate.LocaleId = (int)EditingLanguage.Russian;

    doc.Save(ArtifactsDir + "FieldOptions.UpdateDateTimeFormatting.pdf");
}

/// <summary>
/// Fornisce un oggetto CultureInfo che dovrebbe essere utilizzato durante l'aggiornamento di un campo.
/// </summary>
private class FieldUpdateCultureProvider : IFieldUpdateCultureProvider
{
    /// <summary>
    /// Restituisce un oggetto CultureInfo da utilizzare durante l'aggiornamento del campo.
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

### Guarda anche

* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)
