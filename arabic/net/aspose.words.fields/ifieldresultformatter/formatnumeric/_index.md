---
title: IFieldResultFormatter.FormatNumeric
second_title: Aspose.Words لمراجع .NET API
description: IFieldResultFormatter طريقة. يتم استدعاؤه عندما يقوم Aspose.Words بتطبيق مفتاح تنسيق رقمي على سبيل المثال  ..
type: docs
weight: 30
url: /ar/net/aspose.words.fields/ifieldresultformatter/formatnumeric/
---
## IFieldResultFormatter.FormatNumeric method

يتم استدعاؤه عندما يقوم Aspose.Words بتطبيق مفتاح تنسيق رقمي، على سبيل المثال \# "#.##".

```csharp
public string FormatNumeric(double value, string format)
```

### ملاحظات

يجب أن يعود التنفيذ`باطل` للإشارة إلى ضرورة تطبيق التنسيق الافتراضي.

### أمثلة

يوضح كيفية تطبيق تنسيق مخصص تلقائيًا على نتائج الحقول عندما يتم تحديث الحقول.

```csharp
public void FieldResultFormatting()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldResultFormatter formatter = new FieldResultFormatter("${0}", "Date: {0}", "Item # {0}:");
    doc.FieldOptions.ResultFormatter = formatter;

    // يطبق منسق نتيجة الحقل الخاص بنا تنسيقًا مخصصًا على الحقول التي تم إنشاؤها حديثًا والتي تتكون من ثلاثة أنواع من التنسيقات.
    // يطبق منسقو نتائج الحقول تنسيقًا جديدًا على الحقول عند تحديثها،
    // والذي يحدث بمجرد إنشائها باستخدام التحميل الزائد لطريقة InsertField.
    // 1 - رقمي:
    builder.InsertField(" = 2 + 3 \\# $###");

    Assert.AreEqual("$5", doc.Range.Fields[0].Result);
    Assert.AreEqual(1, formatter.CountFormatInvocations(FieldResultFormatter.FormatInvocationType.Numeric));

    // 2 - التاريخ/الوقت:
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
/// عندما يتم تحديث الحقول ذات التنسيق، سيتجاوز هذا المنسق تنسيقها
/// بتنسيق مخصص، أثناء تتبع كل استدعاء.
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

* interface [IFieldResultFormatter](../)
* مساحة الاسم [Aspose.Words.Fields](../../ifieldresultformatter/)
* المجسم [Aspose.Words](../../../)


