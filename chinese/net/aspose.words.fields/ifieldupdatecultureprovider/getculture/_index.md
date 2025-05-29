---
title: IFieldUpdateCultureProvider.GetCulture
linktitle: GetCulture
articleTitle: GetCulture
second_title: Aspose.Words for .NET
description: 探索 IFieldUpdateCultureProvider 的 GetCulture 方法，该方法可有效返回 CultureInfo 对象以实现无缝字段更新。
type: docs
weight: 10
url: /zh/net/aspose.words.fields/ifieldupdatecultureprovider/getculture/
---
## IFieldUpdateCultureProvider.GetCulture method

返回CultureInfo字段更新期间要使用的对象。

```csharp
public CultureInfo GetCulture(string culture, Field field)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| culture | String | 正在更新的字段所请求的文化名称。 |
| field | Field | 正在更新的字段。 |

### 返回值

应该用于字段更新的文化对象。

## 例子

展示如何指定一种解析每个字段的日期/时间格式的文化。

```csharp
public void DefineDateTimeFormatting()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(FieldType.FieldTime, true);

    doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;

    // 设置一个返回特定于每个字段的文化对象的提供程序。
    doc.FieldOptions.FieldUpdateCultureProvider = new FieldUpdateCultureProvider();

    FieldTime fieldDate = (FieldTime)doc.Range.Fields[0];
    if (fieldDate.LocaleId != (int)EditingLanguage.Russian)
        fieldDate.LocaleId = (int)EditingLanguage.Russian;

    doc.Save(ArtifactsDir + "FieldOptions.UpdateDateTimeFormatting.pdf");
}

/// <summary>
/// 提供一个在字段更新期间应该使用的 CultureInfo 对象。
/// </summary>
private class FieldUpdateCultureProvider : IFieldUpdateCultureProvider
{
    /// <summary>
    /// 返回在字段更新期间要使用的 CultureInfo 对象。
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

### 也可以看看

* class [Field](../../field/)
* interface [IFieldUpdateCultureProvider](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
