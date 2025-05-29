---
title: IFieldResultFormatter Interface
linktitle: IFieldResultFormatter
articleTitle: IFieldResultFormatter
second_title: Aspose.Words для .NET
description: Откройте для себя интерфейс Aspose.Words.Fields.IFieldResultFormatter, который позволит вам легко настраивать и улучшать форматирование результатов полей для ваших документов.
type: docs
weight: 3110
url: /ru/net/aspose.words.fields/ifieldresultformatter/
---
## IFieldResultFormatter interface

Реализуйте этот интерфейс, если вы хотите контролировать форматирование результата поля.

```csharp
public interface IFieldResultFormatter
```

## Методы

| Имя | Описание |
| --- | --- |
| [Format](../../aspose.words.fields/ifieldresultformatter/format/#format)(*double, [GeneralFormat](../generalformat/)*) | Вызывается, когда Aspose.Words применяет переключатель числового формата, т. е. \* Ordinal. |
| [Format](../../aspose.words.fields/ifieldresultformatter/format/#format_1)(*string, [GeneralFormat](../generalformat/)*) | Вызывается, когда Aspose.Words применяет переключатель формата заглавных букв, т. е. \* Upper. |
| [FormatDateTime](../../aspose.words.fields/ifieldresultformatter/formatdatetime/)(*DateTime, string, [CalendarType](../../aspose.words/calendartype/)*) | Вызывается, когда Aspose.Words применяет переключатель формата даты/времени, т. е. \@ "dd.MM.yyyy". |
| [FormatNumeric](../../aspose.words.fields/ifieldresultformatter/formatnumeric/)(*double, string*) | Вызывается, когда Aspose.Words применяет переключатель числового формата, т. е. \# "#.##". |

## Примеры

Показывает, как автоматически применять пользовательский формат к результатам полей по мере обновления полей.

```csharp
public void FieldResultFormatting()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldResultFormatter formatter = new FieldResultFormatter("${0}", "Date: {0}", "Item # {0}:");
    doc.FieldOptions.ResultFormatter = formatter;

    // Наш форматировщик результатов поля применяет пользовательский формат к вновь созданным полям трех типов форматов.
    // Форматировщики результатов полей применяют новое форматирование к полям по мере их обновления,
    // что происходит, как только мы создаем их с помощью перегрузки метода InsertField.
    // 1 - Числовой:
    builder.InsertField(" = 2 + 3 \\# $###");

    Assert.AreEqual("$5", doc.Range.Fields[0].Result);
    Assert.AreEqual(1, formatter.CountFormatInvocations(FieldResultFormatter.FormatInvocationType.Numeric));

    // 2 - Дата/время:
    builder.InsertField("DATE \\@ \"d MMMM yyyy\"");

    Assert.IsTrue(doc.Range.Fields[1].Result.StartsWith("Date: "));
    Assert.AreEqual(1, formatter.CountFormatInvocations(FieldResultFormatter.FormatInvocationType.DateTime));

    // 3 - Общие сведения:
    builder.InsertField("QUOTE \"2\" \\* Ordinal");

    Assert.AreEqual("Item # 2:", doc.Range.Fields[2].Result);
    Assert.AreEqual(1, formatter.CountFormatInvocations(FieldResultFormatter.FormatInvocationType.General));

    formatter.PrintFormatInvocations();
}

/// <summary>
/// При обновлении полей с форматированием этот форматировщик переопределит их форматирование
/// с пользовательским форматом, отслеживая каждый вызов.
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

### Смотрите также

* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
