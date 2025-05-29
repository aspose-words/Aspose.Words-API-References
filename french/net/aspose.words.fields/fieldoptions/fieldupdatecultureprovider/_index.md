---
title: FieldOptions.FieldUpdateCultureProvider
linktitle: FieldUpdateCultureProvider
articleTitle: FieldUpdateCultureProvider
second_title: Aspose.Words pour .NET
description: Découvrez la propriété FieldOptions FieldUpdateCultureProvider, permettant des objets de culture personnalisés pour chaque champ afin d'améliorer l'expérience utilisateur et la localisation.
type: docs
weight: 100
url: /fr/net/aspose.words.fields/fieldoptions/fieldupdatecultureprovider/
---
## FieldOptions.FieldUpdateCultureProvider property

Obtient ou définit un fournisseur qui renvoie un objet de culture spécifique pour chaque champ particulier.

```csharp
public IFieldUpdateCultureProvider FieldUpdateCultureProvider { get; set; }
```

## Remarques

Le fournisseur est sollicité lorsque la valeur de[`FieldUpdateCultureSource`](../fieldupdateculturesource/) estFieldCode.

Si le fournisseur est présent, l'objet de culture qu'il renvoie est utilisé pour la mise à jour du champ. Sinon, une culture système est utilisée.

## Exemples

Montre comment spécifier une culture qui analyse le formatage de date/heure pour chaque champ.

```csharp
public void DefineDateTimeFormatting()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(FieldType.FieldTime, true);

    doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;

    // Définissez un fournisseur qui renvoie un objet de culture spécifique à chaque champ.
    doc.FieldOptions.FieldUpdateCultureProvider = new FieldUpdateCultureProvider();

    FieldTime fieldDate = (FieldTime)doc.Range.Fields[0];
    if (fieldDate.LocaleId != (int)EditingLanguage.Russian)
        fieldDate.LocaleId = (int)EditingLanguage.Russian;

    doc.Save(ArtifactsDir + "FieldOptions.UpdateDateTimeFormatting.pdf");
}

/// <summary>
/// Fournit un objet CultureInfo qui doit être utilisé lors de la mise à jour d'un champ.
/// </summary>
private class FieldUpdateCultureProvider : IFieldUpdateCultureProvider
{
    /// <summary>
    /// Renvoie un objet CultureInfo à utiliser lors de la mise à jour du champ.
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

### Voir également

* interface [IFieldUpdateCultureProvider](../../ifieldupdatecultureprovider/)
* class [FieldOptions](../)
* espace de noms [Aspose.Words.Fields](../../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../../)
