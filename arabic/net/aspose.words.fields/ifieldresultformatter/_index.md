---
title: Interface IFieldResultFormatter
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Fields.IFieldResultFormatter واجهه المستخدم. قم بتنفيذ هذه الواجهة إذا كنت تريد التحكم في كيفية تنسيق نتيجة الحقل.
type: docs
weight: 2530
url: /ar/net/aspose.words.fields/ifieldresultformatter/
---
## IFieldResultFormatter interface

قم بتنفيذ هذه الواجهة إذا كنت تريد التحكم في كيفية تنسيق نتيجة الحقل.

```csharp
public interface IFieldResultFormatter
```

## طُرق

| اسم | وصف |
| --- | --- |
| [Format](../../aspose.words.fields/ifieldresultformatter/format/#format)(double, GeneralFormat) | يتم الاستدعاء عند تطبيق Aspose.Words مفتاح تنسيق رقم ، مثل \ * Ordinal. |
| [Format](../../aspose.words.fields/ifieldresultformatter/format/#format_1)(string, GeneralFormat) | يتم الاستدعاء عند قيام Aspose.Words بتطبيق تبديل تنسيق الأحرف الكبيرة ، أي \ * Upper. |
| [FormatDateTime](../../aspose.words.fields/ifieldresultformatter/formatdatetime/)(DateTime, string, CalendarType) | يتم الاستدعاء عند قيام Aspose.Words بتطبيق تبديل تنسيق التاريخ / الوقت ، على سبيل المثال \ @ "dd.MM.yyyy" . |
| [FormatNumeric](../../aspose.words.fields/ifieldresultformatter/formatnumeric/)(double, string) | يتم الاستدعاء عند قيام Aspose.Words بتطبيق تبديل تنسيق رقمي ، أي \ # "#. ##" . |

### أمثلة

يوضح كيفية تطبيق تنسيق مخصص تلقائيًا على نتائج الحقول أثناء تحديث الحقول.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldResultFormatter formatter = new FieldResultFormatter("${0}", "Date: {0}", "Item # {0}:");
    doc.FieldOptions.ResultFormatter = formatter;

    // يطبق مُنسق النتائج الميدانية الخاص بنا تنسيقًا مخصصًا على الحقول المنشأة حديثًا المكونة من ثلاثة أنواع من التنسيقات.
    // تطبق مُنسِّقات نتائج الحقول تنسيقًا جديدًا للحقول فور تحديثها ،
    // الذي يحدث بمجرد إنشائها باستخدام طريقة InsertField overload.
    // 1 - رقم:
    builder.InsertField(" = 2 + 3 \\# $###");

    Assert.AreEqual("$5", doc.Range.Fields[0].Result);
    Assert.AreEqual(1, formatter.CountFormatInvocations(FieldResultFormatter.FormatInvocationType.Numeric));

    // 2 - التاريخ / الوقت:
    builder.InsertField("DATE \\@ \"d MMMM yyyy\"");

    Assert.IsTrue(doc.Range.Fields[1].Result.StartsWith("Date: "));
    Assert.AreEqual(1, formatter.CountFormatInvocations(FieldResultFormatter.FormatInvocationType.DateTime));

    // 3 - عام:
    builder.InsertField("QUOTE \"2\" \\* Ordinal");

    Assert.AreEqual("Item # 2:", doc.Range.Fields[2].Result);
    Assert.AreEqual(1, formatter.CountFormatInvocations(FieldResultFormatter.FormatInvocationType.General));

    formatter.PrintFormatInvocations();
}

/// <summary>
/// عندما يتم تحديث الحقول ذات التنسيق ، سيتجاوز هذا المنسق تنسيقها
/// بتنسيق مخصص ، أثناء تتبع كل استدعاء.
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

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Fields](../../aspose.words.fields/)
* المجسم [Aspose.Words](../../)


