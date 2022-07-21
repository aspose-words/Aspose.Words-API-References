---
title: FormatDateTime
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words bir tarih/saat formatı anahtarı uyguladığında çağrılır yani  dd.MM.yyyy.
type: docs
weight: 20
url: /tr/net/aspose.words.fields/ifieldresultformatter/formatdatetime/
---
## IFieldResultFormatter.FormatDateTime method

Aspose.Words bir tarih/saat formatı anahtarı uyguladığında çağrılır, yani \@ "dd.MM.yyyy".

```csharp
public string FormatDateTime(DateTime value, string format, CalendarType calendarType)
```

### Notlar

Uygulama geri dönmelidir **hükümsüz** varsayılan biçimlendirmenin uygulanması gerektiğini belirtmek için.

### Örnekler

Alanlar güncellenirken alan sonuçlarına otomatik olarak özel bir biçimin nasıl uygulanacağını gösterir.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);
    FieldResultFormatter formatter = new FieldResultFormatter("${0}", "Date: {0}", "Item # {0}:");
    doc.FieldOptions.ResultFormatter = formatter;

    // Alan sonucu biçimlendiricimiz, yeni oluşturulan alanlara üç tür biçimde özel bir biçim uygular.
    // Alan sonucu biçimlendiricileri, güncellendikçe alanlara yeni biçimlendirme uygular,
    // bu InsertField yöntemi aşırı yüklemesini kullanarak onları oluşturur oluşturmaz gerçekleşir.
    // 1 - Sayısal:
    builder.InsertField(" = 2 + 3 \\# $###");

    Assert.AreEqual("$5", doc.Range.Fields[0].Result);
    Assert.AreEqual(1, formatter.CountFormatInvocations(FieldResultFormatter.FormatInvocationType.Numeric));

    // 2 - Tarih/saat:
    builder.InsertField("DATE \\@ \"d MMMM yyyy\"");

    Assert.IsTrue(doc.Range.Fields[1].Result.StartsWith("Date: "));
    Assert.AreEqual(1, formatter.CountFormatInvocations(FieldResultFormatter.FormatInvocationType.DateTime));

    // 3 - Genel:
    builder.InsertField("QUOTE \"2\" \\* Ordinal");

    Assert.AreEqual("Item # 2:", doc.Range.Fields[2].Result);
    Assert.AreEqual(1, formatter.CountFormatInvocations(FieldResultFormatter.FormatInvocationType.General));

    formatter.PrintFormatInvocations();
}

/// <summary>
/// Biçimlendirmeye sahip alanlar güncellendiğinde, bu biçimlendirici onların biçimlendirmesini geçersiz kılar
/// her çağrıyı izlerken özel bir formatla.
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

### Ayrıca bakınız

* enum [CalendarType](../../../aspose.words/calendartype)
* interface [IFieldResultFormatter](../../ifieldresultformatter)
* ad alanı [Aspose.Words.Fields](../../ifieldresultformatter)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
