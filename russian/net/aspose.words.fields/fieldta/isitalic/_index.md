---
title: FieldTA.IsItalic
linktitle: IsItalic
articleTitle: IsItalic
second_title: Aspose.Words для .NET
description: FieldTA IsItalic свойство. Получает или задает необходимость применения курсива к номеру страницы для записи на С#.
type: docs
weight: 40
url: /ru/net/aspose.words.fields/fieldta/isitalic/
---
## FieldTA.IsItalic property

Получает или задает необходимость применения курсива к номеру страницы для записи.

```csharp
public bool IsItalic { get; set; }
```

## Примеры

Показывает, как построить и настроить таблицу авторитетов, используя поля TOA и TA.

```csharp
public void FieldTOA()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Вставьте поле TOA, которое создаст запись для каждого поля TA в документе,
    // отображение длинных цитат и номеров страниц для каждой записи.
    FieldToa fieldToa = (FieldToa)builder.InsertField(FieldType.FieldTOA, false);

    // Устанавливаем категорию записи для нашей таблицы. Это TOA теперь будет включать только поля TA.
    // которые имеют соответствующее значение в свойстве EntryCategory.
    fieldToa.EntryCategory = "1";

    // Более того, категория «Таблица полномочий» с индексом 1 — «Случаи»,
    // который будет отображаться как заголовок нашей таблицы, если мы установим для этой переменной значение true.
    fieldToa.UseHeading = true;

    // Мы можем дополнительно фильтровать поля TA, назвав закладку, которая должна находиться в пределах границ TOA.
    fieldToa.BookmarkName = "MyBookmark";

    // По умолчанию между цитатой поля TA отображается пунктирная вкладка на всю страницу.
    // и номер его страницы. Мы можем заменить его любым текстом, который мы поместили в это свойство.
    // Вставка символа табуляции сохранит исходную табуляцию.
    fieldToa.EntrySeparator = " \t p.";

    // Если у нас есть несколько записей ТА с одной и той же длинной цитатой,
    // все соответствующие номера страниц будут отображаться в одной строке.
    // Мы можем использовать это свойство, чтобы указать строку, которая будет разделять номера страниц.
    fieldToa.PageNumberListSeparator = " & p. ";

    // Мы можем установить значение true, чтобы в нашей таблице отображалось слово «passim»
    // если в одной строке пять и более номеров страниц.
    fieldToa.UsePassim = true;

    // Одно поле TA может относиться к диапазону страниц.
    // Здесь мы можем указать строку, которая будет отображаться между номерами начальной и конечной страниц для таких диапазонов.
    fieldToa.PageRangeSeparator = " to ";

    // Формат полей TA будет перенесен в нашу таблицу.
    // Мы можем отключить это, установив флаг RemoveEntryFormatting.
    fieldToa.RemoveEntryFormatting = true;
    builder.Font.Color = Color.Green;
    builder.Font.Name = "Arial Black";

    Assert.AreEqual(" TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f", fieldToa.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // Это поле TA не будет отображаться как запись в TOA, поскольку оно находится за пределами
    // границы закладки, указанные в свойстве BookmarkName TOA.
    FieldTA fieldTA = InsertToaEntry(builder, "1", "Source 1");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 1\"", fieldTA.GetFieldCode());

    // Это поле TA находится внутри закладки,
    // но категория записи не соответствует категории таблицы, поэтому поле TA не будет ее включать.
    builder.StartBookmark("MyBookmark");
    fieldTA = InsertToaEntry(builder, "2", "Source 2");

    // Эта запись появится в таблице.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");

    // Таблица TOA не отображает краткие цитаты,
    // но мы можем использовать их как сокращение для обозначения громоздких имен источников, на которые ссылаются несколько полей TA.
    fieldTA.ShortCitation = "S.3";

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\s S.3", fieldTA.GetFieldCode());

    // Мы можем отформатировать номер страницы, чтобы сделать его жирным/курсивным, используя следующие свойства.
    // Мы все равно увидим эти эффекты, если настроим нашу таблицу на игнорирование форматирования.
    fieldTA = InsertToaEntry(builder, "1", "Source 2");
    fieldTA.IsBold = true;
    fieldTA.IsItalic = true;

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 2\" \\b \\i", fieldTA.GetFieldCode());

    // Мы можем настроить поля TA так, чтобы их записи TOA ссылались на диапазон страниц, через которые проходит закладка.
    // Обратите внимание, что эта запись относится к тому же источнику, что и приведенная выше, и использует одну строку в нашей таблице.
    // Эта строка будет содержать номер страницы записи выше и диапазон страниц этой записи,
    // со списком страниц таблицы и разделителями диапазона номеров страниц между номерами страниц.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");
    fieldTA.PageRangeBookmarkName = "MyMultiPageBookmark";

    builder.StartBookmark("MyMultiPageBookmark");
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.InsertBreak(BreakType.PageBreak);
    builder.EndBookmark("MyMultiPageBookmark");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\r MyMultiPageBookmark", fieldTA.GetFieldCode());

    // Если мы включили функцию «Passim» в нашей таблице, наличие 5 или более записей TA с одним и тем же источником вызовет ее.
    for (int i = 0; i < 5; i++)
    {
        InsertToaEntry(builder, "1", "Source 4");
    }

    builder.EndBookmark("MyBookmark");

    doc.UpdateFields();
    doc.Save(ArtifactsDir + "Field.TOA.TA.docx");
}

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

* class [FieldTA](../)
* пространство имен [Aspose.Words.Fields](../../../aspose.words.fields/)
* сборка [Aspose.Words](../../../)
