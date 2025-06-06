---
title: IFieldResultFormatter Interface
linktitle: IFieldResultFormatter
articleTitle: IFieldResultFormatter
second_title: Aspose.Words pour .NET
description: Découvrez l'interface Aspose.Words.Fields.IFieldResultFormatter pour personnaliser et améliorer sans effort la mise en forme des résultats de champ pour vos documents.
type: docs
weight: 3110
url: /fr/net/aspose.words.fields/ifieldresultformatter/
---
## IFieldResultFormatter interface

Implémentez cette interface si vous souhaitez contrôler la façon dont le résultat du champ est formaté.

```csharp
public interface IFieldResultFormatter
```

## Méthodes

| Nom | La description |
| --- | --- |
| [Format](../../aspose.words.fields/ifieldresultformatter/format/#format)(*double, [GeneralFormat](../generalformat/)*) | Appelé lorsque Aspose.Words applique un commutateur de format de nombre, c'est-à-dire \* Ordinal. |
| [Format](../../aspose.words.fields/ifieldresultformatter/format/#format_1)(*string, [GeneralFormat](../generalformat/)*) | Appelé lorsque Aspose.Words applique un changement de format de majuscule, c'est-à-dire \* Upper. |
| [FormatDateTime](../../aspose.words.fields/ifieldresultformatter/formatdatetime/)(*DateTime, string, [CalendarType](../../aspose.words/calendartype/)*) | Appelé lorsque Aspose.Words applique un commutateur de format date/heure, c'est-à-dire \@ "dd.MM.yyyy". |
| [FormatNumeric](../../aspose.words.fields/ifieldresultformatter/formatnumeric/)(*double, string*) | Appelé lorsque Aspose.Words applique un commutateur de format numérique, c'est-à-dire \# "#.##". |

## Exemples

Montre comment appliquer automatiquement un format personnalisé aux résultats des champs lorsque les champs sont mis à jour.

```csharp
public void FieldResultFormatting()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldResultFormatter formatter = new FieldResultFormatter("${0}", "Date: {0}", "Item # {0}:");
    doc.FieldOptions.ResultFormatter = formatter;

    // Notre formateur de résultats de champ applique un format personnalisé aux champs nouvellement créés de trois types de formats.
    // Les formateurs de résultats de champ appliquent une nouvelle mise en forme aux champs au fur et à mesure de leur mise à jour,
    // ce qui se produit dès que nous les créons en utilisant cette surcharge de méthode InsertField.
    // 1 - Numérique :
    builder.InsertField(" = 2 + 3 \\# $###");

    Assert.AreEqual("$5", doc.Range.Fields[0].Result);
    Assert.AreEqual(1, formatter.CountFormatInvocations(FieldResultFormatter.FormatInvocationType.Numeric));

    // 2 - Date/heure :
    builder.InsertField("DATE \\@ \"d MMMM yyyy\"");

    Assert.IsTrue(doc.Range.Fields[1].Result.StartsWith("Date: "));
    Assert.AreEqual(1, formatter.CountFormatInvocations(FieldResultFormatter.FormatInvocationType.DateTime));

    // 3 - Généralités :
    builder.InsertField("QUOTE \"2\" \\* Ordinal");

    Assert.AreEqual("Item # 2:", doc.Range.Fields[2].Result);
    Assert.AreEqual(1, formatter.CountFormatInvocations(FieldResultFormatter.FormatInvocationType.General));

    formatter.PrintFormatInvocations();
}

/// <summary>
/// Lorsque les champs avec mise en forme sont mis à jour, ce formateur remplacera leur mise en forme
/// avec un format personnalisé, tout en suivant chaque invocation.
/// </summary>
private class FieldResultFormatter : IFieldResultFormatter
{
    public FieldResultFormatter(string numberFormat, string dateFormat, string generalFormat)
    {
        mNumberFormat = numberFormat;
        mDateFormat = dateFormat;
        mGeneralFormat = generalFormat;
    }

    public string FormatNumeric(double value, string format)
    {
        if (string.IsNullOrEmpty(mNumberFormat)) 
            return null;

        string newValue = String.Format(mNumberFormat, value);
        FormatInvocations.Add(new FormatInvocation(FormatInvocationType.Numeric, value, format, newValue));
        return newValue;
    }

    public string FormatDateTime(DateTime value, string format, CalendarType calendarType)
    {
        if (string.IsNullOrEmpty(mDateFormat))
            return null;

        string newValue = String.Format(mDateFormat, value);
        FormatInvocations.Add(new FormatInvocation(FormatInvocationType.DateTime, $"{value} ({calendarType})", format, newValue));
        return newValue;
    }

    public string Format(string value, GeneralFormat format)
    {
        return Format((object)value, format);
    }

    public string Format(double value, GeneralFormat format)
    {
        return Format((object)value, format);
    }

    private string Format(object value, GeneralFormat format)
    {
        if (string.IsNullOrEmpty(mGeneralFormat))
            return null;

        string newValue = String.Format(mGeneralFormat, value);
        FormatInvocations.Add(new FormatInvocation(FormatInvocationType.General, value, format.ToString(), newValue));
        return newValue;
    }

    public int CountFormatInvocations(FormatInvocationType formatInvocationType)
    {
        if (formatInvocationType == FormatInvocationType.All)
            return FormatInvocations.Count;
        return FormatInvocations.Count(f => f.FormatInvocationType == formatInvocationType);
    }

    public void PrintFormatInvocations()
    {
        foreach (FormatInvocation f in FormatInvocations)
            Console.WriteLine($"Invocation type:\t{f.FormatInvocationType}\n" +
                              $"\tOriginal value:\t\t{f.Value}\n" +
                              $"\tOriginal format:\t{f.OriginalFormat}\n" +
                              $"\tNew value:\t\t\t{f.NewValue}\n");
    }

    private readonly string mNumberFormat;
    private readonly string mDateFormat;
    private readonly string mGeneralFormat; 
    private List<FormatInvocation> FormatInvocations { get; } = new List<FormatInvocation>();

    private class FormatInvocation
    {
        public FormatInvocationType FormatInvocationType { get; }
        public object Value { get; }
        public string OriginalFormat { get; }
        public string NewValue { get; }

        public FormatInvocation(FormatInvocationType formatInvocationType, object value, string originalFormat, string newValue)
        {
            Value = value;
            FormatInvocationType = formatInvocationType;
            OriginalFormat = originalFormat;
            NewValue = newValue;
        }
    }

    public enum FormatInvocationType
    {
        Numeric, DateTime, General, All
    }
}
```

### Voir également

* espace de noms [Aspose.Words.Fields](../../aspose.words.fields/)
* Assemblée [Aspose.Words](../../)
