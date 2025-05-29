---
title: FieldTA.LongCitation
linktitle: LongCitation
articleTitle: LongCitation
second_title: Aspose.Words для .NET
description: Управляйте своим свойством FieldTA LongCitation без усилий. Легко получайте или устанавливайте длинные цитаты для записей, улучшая организацию и доступность данных.
type: docs
weight: 50
url: /ru/net/aspose.words.fields/fieldta/longcitation/
---
## FieldTA.LongCitation property

Получает или задает длинную цитату для записи.

```csharp
public string LongCitation { get; set; }
```

## Примеры

Показывает, как создать и настроить таблицу авторитетных источников с использованием полей TOA и TA.

```csharp
public void FieldTOA()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Вставьте поле TOA, которое создаст запись для каждого поля TA в документе,
    // отображение длинных цитат и номеров страниц для каждой записи.
    FieldToa fieldToa = (FieldToa)builder.InsertField(FieldType.FieldTOA, false);

    // Задайте категорию записи для нашей таблицы. Этот TOA теперь будет включать только поля TA
    // имеющие совпадающее значение в свойстве EntryCategory.
    fieldToa.EntryCategory = "1";

    // Более того, категория Таблицы авторитетов по индексу 1 — «Дела»,
    // который будет отображаться в качестве заголовка нашей таблицы, если мы установим эту переменную в значение true.
    fieldToa.UseHeading = true;

    // Мы можем дополнительно отфильтровать поля TA, указав закладку, которая должна будет находиться в пределах границ TOA.
    fieldToa.BookmarkName = "MyBookmark";

    // По умолчанию между цитированием поля TA отображается пунктирная линия на всю страницу
    // и номер страницы. Мы можем заменить его любым текстом, который мы поместим в это свойство.
    // Вставка символа табуляции сохранит исходную табуляцию.
    fieldToa.EntrySeparator = " \t p.";

    // Если у нас есть несколько записей ТА, которые имеют одну и ту же длинную цитату,
    // все соответствующие им номера страниц будут отображаться в одной строке.
    // Мы можем использовать это свойство, чтобы указать строку, которая будет разделять номера страниц.
    fieldToa.PageNumberListSeparator = " & p. ";

    // Мы можем установить это значение в true, чтобы наша таблица отображала слово "passim"
    // если в одной строке пять или более номеров страниц.
    fieldToa.UsePassim = true;

    // Одно поле TA может ссылаться на диапазон страниц.
    // Здесь мы можем указать строку, которая будет отображаться между начальным и конечным номерами страниц для таких диапазонов.
    fieldToa.PageRangeSeparator = " to ";

    // Формат из полей TA будет перенесен в нашу таблицу.
    // Мы можем отключить это, установив флаг RemoveEntryFormatting.
    fieldToa.RemoveEntryFormatting = true;
    builder.Font.Color = Color.Green;
    builder.Font.Name = "Arial Black";

    Assert.AreEqual(" TOA  \\c 1 \\h \\b MyBookmark \\e \" \t p.\" \\l \" & p. \" \\p \\g \" to \" \\f", fieldToa.GetFieldCode());

    builder.InsertBreak(BreakType.PageBreak);

    // Это поле TA не будет отображаться как запись в TOA, поскольку оно находится за пределами
    // границы закладки, которые определяет свойство BookmarkName TOA.
    FieldTA fieldTA = InsertToaEntry(builder, "1", "Source 1");

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 1\"", fieldTA.GetFieldCode());

    // Это поле TA находится внутри закладки,
    // но категория записи не соответствует категории таблицы, поэтому поле TA не будет ее включать.
    builder.StartBookmark("MyBookmark");
    fieldTA = InsertToaEntry(builder, "2", "Source 2");

    // Эта запись появится в таблице.
    fieldTA = InsertToaEntry(builder, "1", "Source 3");

    // Таблица TOA не отображает краткие цитаты,
    // но мы можем использовать их в качестве сокращения для ссылки на громоздкие имена источников, на которые ссылаются несколько полей TA.
    fieldTA.ShortCitation = "S.3";

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 3\" \\s S.3", fieldTA.GetFieldCode());

    // Мы можем отформатировать номер страницы, сделав его жирным/курсивным, используя следующие свойства.
    // Мы все равно увидим эти эффекты, если настроим нашу таблицу на игнорирование форматирования.
    fieldTA = InsertToaEntry(builder, "1", "Source 2");
    fieldTA.IsBold = true;
    fieldTA.IsItalic = true;

    Assert.AreEqual(" TA  \\c 1 \\l \"Source 2\" \\b \\i", fieldTA.GetFieldCode());

    // Мы можем настроить поля TA так, чтобы их записи TOA ссылались на диапазон страниц, которые охватывает закладка.
    // Обратите внимание, что эта запись ссылается на тот же источник, что и указанная выше, чтобы разделить одну строку в нашей таблице.
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

    // Если мы включили функцию «Passim» для нашей таблицы, наличие 5 или более записей TA с одним и тем же источником приведет к ее вызову.
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
