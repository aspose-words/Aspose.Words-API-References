---
title: IFieldResultFormatter Interface
linktitle: IFieldResultFormatter
articleTitle: IFieldResultFormatter
second_title: Aspose.Words för .NET
description: Aspose.Words.Fields.IFieldResultFormatter gränssnitt. Implementera detta gränssnitt om du vill styra hur fältresultatet formateras i C#.
type: docs
weight: 2700
url: /sv/net/aspose.words.fields/ifieldresultformatter/
---
## IFieldResultFormatter interface

Implementera detta gränssnitt om du vill styra hur fältresultatet formateras.

```csharp
public interface IFieldResultFormatter
```

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Format](../../aspose.words.fields/ifieldresultformatter/format/#format)(*double, [GeneralFormat](../generalformat/)*) | Anropas när Aspose.Words använder en sifferformatsväxling, dvs. \* Ordinal. |
| [Format](../../aspose.words.fields/ifieldresultformatter/format/#format_1)(*string, [GeneralFormat](../generalformat/)*) | Anropas när Aspose.Words använder en byte av versalformat, dvs. \* Upper. |
| [FormatDateTime](../../aspose.words.fields/ifieldresultformatter/formatdatetime/)(*DateTime, string, [CalendarType](../../aspose.words/calendartype/)*) | Anropas när Aspose.Words använder en ändring av datum/tid-format, dvs. \@ "dd.MM.åååå". |
| [FormatNumeric](../../aspose.words.fields/ifieldresultformatter/formatnumeric/)(*double, string*) | Anropas när Aspose.Words använder en numerisk formatväxling, dvs. \# "#.##". |

## Exempel

Visar hur man automatiskt tillämpar ett anpassat format på fältresultat när fälten uppdateras.

```csharp
public void FieldResultFormatting()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldResultFormatter formatter = new FieldResultFormatter("${0}", "Date: {0}", "Item # {0}:");
    doc.FieldOptions.ResultFormatter = formatter;

    // Vår fältresultatformaterare tillämpar ett anpassat format på nyskapade fält av tre typer av format.
    // Fältresultatformaterare tillämpar ny formatering på fält när de uppdateras,
    // vilket händer så fort vi skapar dem med den här InsertField-metoden överbelastning.
    // 1 - Numerisk:
    builder.InsertField(" = 2 + 3 \\# $###");

    Assert.AreEqual("$5", doc.Range.Fields[0].Result);
    Assert.AreEqual(1, formatter.CountFormatInvocations(FieldResultFormatter.FormatInvocationType.Numeric));

    // 2 - Datum/tid:
    builder.InsertField("DATE \\@ \"d MMMM yyyy\"");

    Assert.IsTrue(doc.Range.Fields[1].Result.StartsWith("Date: "));
    Assert.AreEqual(1, formatter.CountFormatInvocations(FieldResultFormatter.FormatInvocationType.DateTime));

    // 3 - Allmänt:
    builder.InsertField("QUOTE \"2\" \\* Ordinal");

    Assert.AreEqual("Item # 2:", doc.Range.Fields[2].Result);
    Assert.AreEqual(1, formatter.CountFormatInvocations(FieldResultFormatter.FormatInvocationType.General));

    formatter.PrintFormatInvocations();
}

/// <summary>
/// När fält med formatering uppdateras kommer denna formatterare att åsidosätta deras formatering
/// med ett anpassat format, samtidigt som du spårar varje anrop.
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

### Se även

* namnutrymme [Aspose.Words.Fields](../../aspose.words.fields/)
* hopsättning [Aspose.Words](../../)
