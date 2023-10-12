---
title: IFieldUpdateCultureProvider.GetCulture
second_title: Aspose.Words لمراجع .NET API
description: IFieldUpdateCultureProvider طريقة. إرجاع أCultureInfoالكائن الذي سيتم استخدامه أثناء تحديث الحقل.
type: docs
weight: 10
url: /ar/net/aspose.words.fields/ifieldupdatecultureprovider/getculture/
---
## IFieldUpdateCultureProvider.GetCulture method

إرجاع أCultureInfoالكائن الذي سيتم استخدامه أثناء تحديث الحقل.

```csharp
public CultureInfo GetCulture(string culture, Field field)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| culture | String | اسم الثقافة المطلوبة للحقل الذي يتم تحديثه. |
| field | Field | يتم تحديث الحقل. |

### قيمة الإرجاع

كائن الثقافة الذي يجب استخدامه لتحديث الحقل.

### أمثلة

يوضح كيفية تحديد ثقافة تقوم بتوزيع تنسيق التاريخ/الوقت لكل حقل.

```csharp
public void DefineDateTimeFormatting()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(FieldType.FieldTime, true);

    doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;

    // قم بتعيين موفر يُرجع كائن ثقافة خاصًا بكل حقل.
    doc.FieldOptions.FieldUpdateCultureProvider = new FieldUpdateCultureProvider();

    FieldTime fieldDate = (FieldTime)doc.Range.Fields[0];
    if (fieldDate.LocaleId != (int)EditingLanguage.Russian)
        fieldDate.LocaleId = (int)EditingLanguage.Russian;

    doc.Save(ArtifactsDir + "FieldOptions.UpdateDateTimeFormatting.pdf");
}

/// <summary>
/// يوفر كائن CultureInfo الذي يجب استخدامه أثناء تحديث الحقل.
/// </summary>
private class FieldUpdateCultureProvider : IFieldUpdateCultureProvider
{
    /// <summary>
    /// يُرجع كائن CultureInfo ليتم استخدامه أثناء تحديث الحقل.
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

### أنظر أيضا

* class [Field](../../field/)
* interface [IFieldUpdateCultureProvider](../)
* مساحة الاسم [Aspose.Words.Fields](../../ifieldupdatecultureprovider/)
* المجسم [Aspose.Words](../../../)


