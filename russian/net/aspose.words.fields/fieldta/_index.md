---
title: Class FieldTA
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Fields.FieldTA сорт. Реализует поле TA.
type: docs
weight: 2470
url: /ru/net/aspose.words.fields/fieldta/
---
## FieldTA class

Реализует поле TA.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) статья документации.

```csharp
public class FieldTA : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldTA](fieldta/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Получает текст, представляющий результат отображаемого поля. |
| [End](../../aspose.words.fields/field/end/) { get; } | Получает узел, представляющий конец поля. |
| [EntryCategory](../../aspose.words.fields/fieldta/entrycategory/) { get; set; } | Получает или задает целочисленную категорию записи, которая представляет собой число, соответствующее порядку категорий . |
| [Format](../../aspose.words.fields/field/format/) { get; } | Получает[`FieldFormat`](../fieldformat/) объект, обеспечивающий типизированный доступ к форматированию поля. |
| [IsBold](../../aspose.words.fields/fieldta/isbold/) { get; set; } | Получает или задает необходимость применения жирного форматирования к номеру страницы для записи. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Получает или устанавливает, является ли текущий результат поля более неправильным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsItalic](../../aspose.words.fields/fieldta/isitalic/) { get; set; } | Получает или задает необходимость применения курсива к номеру страницы для записи. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Получает или задает, заблокировано ли поле (не следует пересчитывать результат). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Получает или задает LCID поля. |
| [LongCitation](../../aspose.words.fields/fieldta/longcitation/) { get; set; } | Получает или задает длинную ссылку на запись. |
| [PageRangeBookmarkName](../../aspose.words.fields/fieldta/pagerangebookmarkname/) { get; set; } | Получает или задает имя закладки, которая отмечает диапазон страниц, вставленных в качестве номера страницы записи. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Получает или задает текст, расположенный между разделителем полей и концом поля. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Получает узел, представляющий разделитель полей. Возможно`нулевой` . |
| [ShortCitation](../../aspose.words.fields/fieldta/shortcitation/) { get; set; } | Получает или задает краткую ссылку на запись. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Получает узел, представляющий начало поля. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Получает тип поля Microsoft Word. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Возвращает текст между началом поля и разделителем поля (или концом поля, если разделителя нет). Включены как код поля, так и результат поля дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(bool) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделителя нет). |
| [Remove](../../aspose.words.fields/field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля является последним дочерним его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращается`нулевой` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Выполняет отсоединение поля. |
| [Update](../../aspose.words.fields/field/update/)() | Выполняет обновление поля. Выдает, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update/)(bool) | Выполняет обновление поля. Выдает, если поле уже обновляется. |

### Примечания

Определяет текст и номер страницы для записи таблицы полномочий, которая используется полем TOA.

### Примеры

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

* class [Field](../field/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)


