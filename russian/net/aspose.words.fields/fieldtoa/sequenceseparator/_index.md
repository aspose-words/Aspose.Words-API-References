---
title: FieldToa.SequenceSeparator
second_title: Справочник по API Aspose.Words для .NET
description: FieldToa свойство. Получает или задает последовательность символов используемую для разделения порядковых номеров и номеров страниц.
type: docs
weight: 90
url: /ru/net/aspose.words.fields/fieldtoa/sequenceseparator/
---
## FieldToa.SequenceSeparator property

Получает или задает последовательность символов, используемую для разделения порядковых номеров и номеров страниц.

```csharp
public string SequenceSeparator { get; set; }
```

### Примеры

Показывает, как построить и настроить таблицу полномочий, используя поля TOA и TA.

```csharp
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Вставьте поле TOA, которое создаст запись для каждого поля TA в документе,
    // отображение длинных цитат и номеров страниц для каждой записи.
    FieldToa fieldToa = (FieldToa)builder.InsertField(FieldType.FieldTOA, false);

    // Установить категорию записи для нашей таблицы. Этот TOA теперь будет включать только поля TA.
    // которые имеют соответствующее значение в свойстве EntryCategory.
    fieldToa.EntryCategory = "1";

    // Более того, категория "Таблица авторитетов" по индексу 1 - "Дела",
    // который будет отображаться как заголовок нашей таблицы, если мы установим для этой переменной значение true.
    fieldToa.UseHeading = true;

    // Мы можем дополнительно отфильтровать поля TA, назвав закладку, которая должна быть в пределах границ TOA.
    fieldToa.BookmarkName = "MyBookmark";

    // По умолчанию между цитированием поля TA появляется пунктирная линия на всю страницу
    // и его номер страницы. Мы можем заменить его любым текстом, который поместим в это свойство.
    // Вставка символа табуляции сохранит исходную табуляцию.
    fieldToa.EntrySeparator = " \t p.";

    // Если у нас есть несколько записей TA, которые имеют одну и ту же длинную цитату,
    // все их соответствующие номера страниц будут отображаться в одной строке.
    // Мы можем использовать это свойство, чтобы указать строку, которая будет разделять их номера страниц.
    fieldToa.PageNumberListSeparator = " & p. ";

    // Мы можем установить значение true, чтобы наша таблица отображала слово "passim"
    // если в одной строке пять и более номеров страниц.
    fieldToa.UsePassim = true;

    // Одно поле ТА может относиться к диапазону страниц.
    // Здесь мы можем указать строку, которая будет отображаться между номерами начальной и конечной страниц для таких диапазонов.
    fieldToa.PageRangeSeparator = " to ";

    // Формат полей ТА будет перенесен в нашу таблицу.
    // Мы можем отключить это, установив флаг RemoveEntryFormatting.
    fieldToa.RemoveEntryFormatting = true;
    builder.Font.Color = Color.Green;
    builder.Font.Name = "Arial Black";

    Assert.AreEqual(" TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f", fieldToa.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // Это поле ТА не будет отображаться как запись в TOA, так как оно находится за пределами
    // границы закладки, указанные в свойстве BookmarkName TOA.
    FieldTA fieldTA = InsertToaEntry(builder, "1", "Source 1");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 1\"", fieldTA.GetFieldCode());

    // Это поле ТА находится внутри закладки,
    // но категория записи не совпадает с категорией таблицы, поэтому поле TA не будет включать ее.
    builder.StartBookmark("MyBookmark");
    fieldTA = InsertToaEntry(builder, "2", "Source 2");

    // Эта запись появится в таблице.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");

    // Таблица TOA не отображает короткие цитаты,
    // но мы можем использовать их как сокращение для обозначения громоздких имен источников, на которые ссылаются несколько полей ТА.
    fieldTA.ShortCitation = "S.3";

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\s S.3", fieldTA.GetFieldCode());

    // Мы можем отформатировать номер страницы, чтобы сделать его полужирным/курсивом, используя следующие свойства.
    // Мы по-прежнему увидим эти эффекты, если настроим нашу таблицу на игнорирование форматирования.
    fieldTA = InsertToaEntry(builder, "1", "Source 2");
    fieldTA.IsBold = true;
    fieldTA.IsItalic = true;

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 2\" \\b \\i", fieldTA.GetFieldCode());

    // Мы можем настроить поля TA так, чтобы их записи TOA ссылались на диапазон страниц, через которые проходит закладка.
    // Обратите внимание, что эта запись относится к тому же источнику, что и запись выше, чтобы разделить одну строку в нашей таблице.
    // Эта строка будет иметь номер страницы записи выше и диапазон страниц этой записи,
    // со списком страниц таблицы и разделителями диапазонов номеров страниц между номерами страниц.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");
    fieldTA.PageRangeBookmarkName = "MyMultiPageBookmark";

    builder.StartBookmark("MyMultiPageBookmark");
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.EndBookmark("MyMultiPageBookmark");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark", fieldTA.GetFieldCode());

    // Если мы включили функцию "Passim" для нашей таблицы, наличие 5 или более записей TA с одним и тем же источником вызовет ее.
    for (int i = 0; i < 5; i++)
    {
        InsertToaEntry(builder, "1", "Source 4");
    }

    builder.EndBookmark("MyBookmark");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOA.TA.docx");

private static FieldTA InsertToaEntry(DocumentBuilder builder, string entryCategory, string longCitation)
{
    FieldTA field = (FieldTA)builder.InsertField(FieldType.FieldTOAEntry, false);
    field.EntryCategory = entryCategory;
    field.LongCitation = longCitation;

    builder.InsertBreak(BreakType.PageBreak);

    return field;
}
```

### Смотрите также

* class [FieldToa](../)
* пространство имен [Aspose.Words.Fields](../../fieldtoa/)
* сборка [Aspose.Words](../../../)


