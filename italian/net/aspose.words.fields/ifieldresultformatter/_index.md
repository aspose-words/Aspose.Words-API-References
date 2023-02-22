---
title: Interface IFieldResultFormatter
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Fields.IFieldResultFormatter interfaccia. Implementa questa interfaccia se vuoi controllare come è formattato il risultato del campo.
type: docs
weight: 2530
url: /it/net/aspose.words.fields/ifieldresultformatter/
---
## IFieldResultFormatter interface

Implementa questa interfaccia se vuoi controllare come è formattato il risultato del campo.

```csharp
public interface IFieldResultFormatter
```

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Format](../../aspose.words.fields/ifieldresultformatter/format/#format)(double, GeneralFormat) | Chiamato quando Aspose.Words applica un cambio di formato numerico, ad esempio \* Ordinal. |
| [Format](../../aspose.words.fields/ifieldresultformatter/format/#format_1)(string, GeneralFormat) | Chiamato quando Aspose.Words applica un cambio di formato delle maiuscole, ad esempio \* Upper. |
| [FormatDateTime](../../aspose.words.fields/ifieldresultformatter/formatdatetime/)(DateTime, string, CalendarType) | Chiamato quando Aspose.Words applica un cambio di formato data/ora, ad esempio \@ "gg.MM.aaaa". |
| [FormatNumeric](../../aspose.words.fields/ifieldresultformatter/formatnumeric/)(double, string) | Chiamato quando Aspose.Words applica un cambio di formato numerico, ad esempio \# "#.##". |

### Esempi

Mostra come applicare automaticamente un formato personalizzato ai risultati dei campi man mano che i campi vengono aggiornati.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldResultFormatter formatter = new FieldResultFormatter("${0}", "Date: {0}", "Item # {0}:");
    doc.FieldOptions.ResultFormatter = formatter;

    // Il nostro formattatore dei risultati dei campi applica un formato personalizzato ai campi appena creati di tre tipi di formati.
    // I formattatori dei risultati dei campi applicano una nuova formattazione ai campi man mano che vengono aggiornati,
    // che si verifica non appena li creiamo utilizzando questo overload del metodo InsertField.
    // 1 - Numerico:
    builder.InsertField(" = 2 + 3 \\# $###");

    Assert.AreEqual("$5", doc.Range.Fields[0].Result);
    Assert.AreEqual(1, formatter.CountFormatInvocations(FieldResultFormatter.FormatInvocationType.Numeric));

    // 2 - Data/ora:
    builder.InsertField("DATE \\@ \"d MMMM yyyy\"");

    Assert.IsTrue(doc.Range.Fields[1].Result.StartsWith("Date: "));
    Assert.AreEqual(1, formatter.CountFormatInvocations(FieldResultFormatter.FormatInvocationType.DateTime));

    // 3 - Generale:
    builder.InsertField("QUOTE \"2\" \\* Ordinal");

    Assert.AreEqual("Item # 2:", doc.Range.Fields[2].Result);
    Assert.AreEqual(1, formatter.CountFormatInvocations(FieldResultFormatter.FormatInvocationType.General));

    formatter.PrintFormatInvocations();
}

/// <summary>
/// Quando i campi con formattazione vengono aggiornati, questo formattatore sovrascriverà la loro formattazione
/// con un formato personalizzato, tenendo traccia di ogni chiamata.
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

### Guarda anche

* spazio dei nomi [Aspose.Words.Fields](../../aspose.words.fields/)
* assemblea [Aspose.Words](../../)


