---
title: FieldOptions.FieldUpdateCultureProvider
linktitle: FieldUpdateCultureProvider
articleTitle: FieldUpdateCultureProvider
second_title: .NET için Aspose.Words
description: Kullanıcı deneyimini ve yerelleştirmeyi geliştirmek için her alan için özel kültür nesneleri sağlayan FieldOptions FieldUpdateCultureProvider özelliğini keşfedin.
type: docs
weight: 100
url: /tr/net/aspose.words.fields/fieldoptions/fieldupdatecultureprovider/
---
## FieldOptions.FieldUpdateCultureProvider property

Her belirli alan için belirli bir kültür nesnesi döndüren bir sağlayıcı alır veya ayarlar.

```csharp
public IFieldUpdateCultureProvider FieldUpdateCultureProvider { get; set; }
```

## Notlar

Sağlayıcı, değeri talep edildiğinde[`FieldUpdateCultureSource`](../fieldupdateculturesource/) dırFieldCode.

Sağlayıcı mevcutsa, döndürdüğü kültür nesnesi alan güncellemesi için kullanılır. Aksi takdirde, bir sistem kültürü kullanılır.

## Örnekler

Her alan için tarih/saat biçimlendirmesini ayrıştıran bir kültürün nasıl belirtileceğini gösterir.

```csharp
public void DefineDateTimeFormatting()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(FieldType.FieldTime, true);

    doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;

    // Her alana özgü bir kültür nesnesi döndüren bir sağlayıcı ayarlayın.
    doc.FieldOptions.FieldUpdateCultureProvider = new FieldUpdateCultureProvider();

    FieldTime fieldDate = (FieldTime)doc.Range.Fields[0];
    if (fieldDate.LocaleId != (int)EditingLanguage.Russian)
        fieldDate.LocaleId = (int)EditingLanguage.Russian;

    doc.Save(ArtifactsDir + "FieldOptions.UpdateDateTimeFormatting.pdf");
}

/// <summary>
/// Bir alanın güncellenmesi sırasında kullanılması gereken bir CultureInfo nesnesi sağlar.
/// </summary>
private class FieldUpdateCultureProvider : IFieldUpdateCultureProvider
{
    /// <summary>
    /// Alanın güncellenmesi sırasında kullanılacak bir CultureInfo nesnesi döndürür.
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

### Ayrıca bakınız

* interface [IFieldUpdateCultureProvider](../../ifieldupdatecultureprovider/)
* class [FieldOptions](../)
* ad alanı [Aspose.Words.Fields](../../../aspose.words.fields/)
* toplantı [Aspose.Words](../../../)
