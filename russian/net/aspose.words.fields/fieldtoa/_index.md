---
title: FieldToa Class
linktitle: FieldToa
articleTitle: FieldToa
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fields.FieldToa для бесшовной реализации поля TOA. Улучшите обработку документов с помощью мощных функций уже сегодня!
type: docs
weight: 2930
url: /ru/net/aspose.words.fields/fieldtoa/
---
## FieldToa class

Реализует поле TOA.

Чтобы узнать больше, посетите[Работа с полями](https://docs.aspose.com/words/net/working-with-fields/) документальная статья.

```csharp
public class FieldToa : Field
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FieldToa](fieldtoa/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [BookmarkName](../../aspose.words.fields/fieldtoa/bookmarkname/) { get; set; } | Возвращает или задает имя закладки, которая отмечает часть документа, используемую для построения таблицы. |
| [DisplayResult](../../aspose.words.fields/field/displayresult/) { get; } | Получает текст, представляющий отображаемый результат поля. |
| [End](../../aspose.words.fields/field/end/) { get; } | Получает узел, представляющий конец поля. |
| [EntryCategory](../../aspose.words.fields/fieldtoa/entrycategory/) { get; set; } | Возвращает или задает интегральную категорию для записей, включенных в таблицу. |
| [EntrySeparator](../../aspose.words.fields/fieldtoa/entryseparator/) { get; set; } | Возвращает или задает последовательность символов, которая используется для разделения записи таблицы авторитетных источников и номера ее страницы. |
| [Format](../../aspose.words.fields/field/format/) { get; } | Получает[`FieldFormat`](../fieldformat/)объект, который обеспечивает типизированный доступ к форматированию поля. |
| [IsDirty](../../aspose.words.fields/field/isdirty/) { get; set; } | Возвращает или задает, является ли текущий результат поля более неверным (устаревшим) из-за других изменений, внесенных в документ. |
| [IsLocked](../../aspose.words.fields/field/islocked/) { get; set; } | Возвращает или задает, заблокировано ли поле (не следует пересчитывать его результат). |
| [LocaleId](../../aspose.words.fields/field/localeid/) { get; set; } | Получает или задает LCID поля. |
| [PageNumberListSeparator](../../aspose.words.fields/fieldtoa/pagenumberlistseparator/) { get; set; } | Возвращает или задает последовательность символов, которая используется для разделения двух номеров страниц в списке номеров страниц. |
| [PageRangeSeparator](../../aspose.words.fields/fieldtoa/pagerangeseparator/) { get; set; } | Возвращает или задает последовательность символов, которая используется для разделения начала и конца диапазона страниц. |
| [RemoveEntryFormatting](../../aspose.words.fields/fieldtoa/removeentryformatting/) { get; set; } | Возвращает или задает, следует ли удалить форматирование текста записи в документе из записи в таблице авторитетных источников. |
| [Result](../../aspose.words.fields/field/result/) { get; set; } | Возвращает или задает текст, который находится между разделителем полей и концом поля. |
| [Separator](../../aspose.words.fields/field/separator/) { get; } | Получает узел, представляющий разделитель полей. Может быть`нулевой` . |
| [SequenceName](../../aspose.words.fields/fieldtoa/sequencename/) { get; set; } | Возвращает или задает имя последовательности, номер которой включен в номер страницы. |
| [SequenceSeparator](../../aspose.words.fields/fieldtoa/sequenceseparator/) { get; set; } | Возвращает или задает последовательность символов, используемую для разделения порядковых номеров и номеров страниц. |
| [Start](../../aspose.words.fields/field/start/) { get; } | Получает узел, представляющий начало поля. |
| virtual [Type](../../aspose.words.fields/field/type/) { get; } | Получает тип поля Microsoft Word. |
| [UseHeading](../../aspose.words.fields/fieldtoa/useheading/) { get; set; } | Возвращает или задает, следует ли включать заголовок категории для записей в таблице авторитетных источников. |
| [UsePassim](../../aspose.words.fields/fieldtoa/usepassim/) { get; set; } | Возвращает или задает, следует ли заменить пять или более различных ссылок на страницы с одним и тем же авторитетным источником на «passim», который используется для указания того, что слово или отрывок часто встречается в цитируемой работе. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)() | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделитель отсутствует). Включаются как код поля, так и результат поля дочерних полей. |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode/)(*bool*) | Возвращает текст между началом поля и разделителем полей (или концом поля, если разделитель отсутствует). |
| [Remove](../../aspose.words.fields/field/remove/)() | Удаляет поле из документа. Возвращает узел сразу после поля. Если конец поля — последний child его родительского узла, возвращает его родительский абзац. Если поле уже удалено, возвращает`нулевой` . |
| [Unlink](../../aspose.words.fields/field/unlink/)() | Выполняет отмену связи поля. |
| [Update](../../aspose.words.fields/field/update/)() | Выполняет обновление поля. Выдает исключение, если поле уже обновляется. |
| [Update](../../aspose.words.fields/field/update/)(*bool*) | Выполняет обновление поля. Выдает исключение, если поле уже обновляется. |

## Примечания

Создает таблицу авторитетных источников (то есть список ссылок в юридическом документе, например, ссылки на дела, уставы и правила, а также номера страниц, на которых эти ссылки появляются), используя записи , указанные в полях TA.

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

* class [Field](../field/)
* пространство имен [Aspose.Words.Fields](../../aspose.words.fields/)
* сборка [Aspose.Words](../../)
