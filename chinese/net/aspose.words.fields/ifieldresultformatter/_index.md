---
title: IFieldResultFormatter Interface
linktitle: IFieldResultFormatter
articleTitle: IFieldResultFormatter
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Fields.IFieldResultFormatter 接口，轻松定制和增强文档的字段结果格式。
type: docs
weight: 3110
url: /zh/net/aspose.words.fields/ifieldresultformatter/
---
## IFieldResultFormatter interface

如果您想控制字段结果的格式，请实现此接口。

```csharp
public interface IFieldResultFormatter
```

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Format](../../aspose.words.fields/ifieldresultformatter/format/#format)(*double, [GeneralFormat](../generalformat/)*) | 当 Aspose.Words 应用数字格式切换时调用，即 \* Ordinal. |
| [Format](../../aspose.words.fields/ifieldresultformatter/format/#format_1)(*string, [GeneralFormat](../generalformat/)*) | 当 Aspose.Words 应用大写格式切换时调用，即 \* Upper. |
| [FormatDateTime](../../aspose.words.fields/ifieldresultformatter/formatdatetime/)(*DateTime, string, [CalendarType](../../aspose.words/calendartype/)*) | 当 Aspose.Words 应用日期/时间格式切换时调用，即 \@ "dd.MM.yyyy". |
| [FormatNumeric](../../aspose.words.fields/ifieldresultformatter/formatnumeric/)(*double, string*) | 当 Aspose.Words 应用数字格式开关时调用，即 \# "#.##". |

## 例子

展示如何在字段更新时自动将自定义格式应用于字段结果。

```csharp
public void FieldResultFormatting()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldResultFormatter formatter = new FieldResultFormatter("${0}", "Date: {0}", "Item # {0}:");
    doc.FieldOptions.ResultFormatter = formatter;

    // 我们的字段结果格式化程序将自定义格式应用于三种格式的新创建的字段。
    // 字段结果格式化程序在字段更新时将新格式应用于字段，
    // 当我们使用此 InsertField 方法重载创建它们时就会发生这种情况。
    // 1 - 数字：
    builder.InsertField(" = 2 + 3 \\# $###");

    Assert.AreEqual("$5", doc.Range.Fields[0].Result);
    Assert.AreEqual(1, formatter.CountFormatInvocations(FieldResultFormatter.FormatInvocationType.Numeric));

    // 2 - 日期/时间：
    builder.InsertField("DATE \\@ \"d MMMM yyyy\"");

    Assert.IsTrue(doc.Range.Fields[1].Result.StartsWith("Date: "));
    Assert.AreEqual(1, formatter.CountFormatInvocations(FieldResultFormatter.FormatInvocationType.DateTime));

    // 3 - 一般：
    builder.InsertField("QUOTE \"2\" \\* Ordinal");

    Assert.AreEqual("Item # 2:", doc.Range.Fields[2].Result);
    Assert.AreEqual(1, formatter.CountFormatInvocations(FieldResultFormatter.FormatInvocationType.General));

    formatter.PrintFormatInvocations();
}

/// <summary>
/// 当带有格式的字段更新时，此格式化程序将覆盖其格式
/// 使用自定义格式，同时跟踪每次调用。
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

### 也可以看看

* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
