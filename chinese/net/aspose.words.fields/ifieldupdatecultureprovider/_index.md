---
title: Interface IFieldUpdateCultureProvider
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Fields.IFieldUpdateCultureProvider 界面. 实施时提供一个CultureInfo在更新特定字段期间应使用的对象
type: docs
weight: 2540
url: /zh/net/aspose.words.fields/ifieldupdatecultureprovider/
---
## IFieldUpdateCultureProvider interface

实施时，提供一个CultureInfo在更新特定字段期间应使用的对象。

```csharp
public interface IFieldUpdateCultureProvider
```

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetCulture](../../aspose.words.fields/ifieldupdatecultureprovider/getculture/)(string, Field) | 返回一个CultureInfo在字段更新期间使用的对象。 |

### 例子

演示如何指定一种文化，以解析每个字段的日期/时间格式。

```csharp
[Test]
public void DefineDateTimeFormatting()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(FieldType.FieldTime, true);

    doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;

    // 设置一个提供程序，该提供程序返回特定于每个字段的文化对象。
    doc.FieldOptions.FieldUpdateCultureProvider = new FieldUpdateCultureProvider();

    FieldTime fieldDate = (FieldTime)doc.Range.Fields[0];
    if (fieldDate.LocaleId != (int)EditingLanguage.Russian)
        fieldDate.LocaleId = (int)EditingLanguage.Russian;

    doc.Save(ArtifactsDir + "FieldOptions.UpdateDateTimeFormatting.pdf");
}

/// <summary>
/// 提供在更新字段期间应使用的 CultureInfo 对象。
/// </summary>
private class FieldUpdateCultureProvider : IFieldUpdateCultureProvider
{
    /// <summary>
    /// 返回要在字段更新期间使用的 CultureInfo 对象。
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

* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)


