---
title: Range Class
linktitle: Range
articleTitle: Range
second_title: Aspose.Words для .NET
description: Aspose.Words.Range сорт. Представляет непрерывную область документа на С#.
type: docs
weight: 4520
url: /ru/net/aspose.words/range/
---
## Range class

Представляет непрерывную область документа.

Чтобы узнать больше, посетите[Работа с диапазонами](https://docs.aspose.com/words/net/working-with-ranges/) статья документации.

```csharp
public class Range
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Bookmarks](../../aspose.words/range/bookmarks/) { get; } | Возвращает[`Bookmarks`](./bookmarks/) коллекция, представляющая все закладки в диапазоне. |
| [Fields](../../aspose.words/range/fields/) { get; } | Возвращает[`Fields`](./fields/) коллекция, представляющая все поля в диапазоне. |
| [FormFields](../../aspose.words/range/formfields/) { get; } | Возвращает[`FormFields`](./formfields/) коллекция, представляющая все поля формы в диапазоне. |
| [Revisions](../../aspose.words/range/revisions/) { get; } | Получает коллекцию редакций (отслеживаемых изменений), существующих в этом диапазоне. |
| [StructuredDocumentTags](../../aspose.words/range/structureddocumenttags/) { get; } | Возвращает[`StructuredDocumentTags`](./structureddocumenttags/) коллекция, представляющая все теги структурированных документов в диапазоне. |
| [Text](../../aspose.words/range/text/) { get; } | Получает текст диапазона. |

## Методы

| Имя | Описание |
| --- | --- |
| [Delete](../../aspose.words/range/delete/)() | Удаляет все символы диапазона. |
| [NormalizeFieldTypes](../../aspose.words/range/normalizefieldtypes/)() | Изменяет значения типов полей.[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype/) из[`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../aspose.words.fields/fieldend/) в этом диапазоне, чтобы они соответствовали типам полей, содержащимся в кодах полей. |
| [Replace](../../aspose.words/range/replace/#replace_2)(*Regex, string*) | Заменяет все вхождения шаблона символов, указанного в регулярном выражении, другой строкой. |
| [Replace](../../aspose.words/range/replace/#replace)(*string, string*) | Заменяет все вхождения указанного шаблона строки символов заменяющей строкой. |
| [Replace](../../aspose.words/range/replace/#replace_3)(*Regex, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | Заменяет все вхождения шаблона символов, указанного в регулярном выражении, другой строкой. |
| [Replace](../../aspose.words/range/replace/#replace_1)(*string, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | Заменяет все вхождения указанного шаблона строки символов заменяющей строкой. |
| [ToDocument](../../aspose.words/range/todocument/)() | Создает новый полностью сформированный документ, содержащий диапазон. |
| [UnlinkFields](../../aspose.words/range/unlinkfields/)() | Отменяет связь полей в этом диапазоне. |
| [UpdateFields](../../aspose.words/range/updatefields/)() | Обновляет значения полей документа в этом диапазоне. |

## Примечания

Документ представлен деревом узлов, и узлы предоставляют Operations для работы с деревом, но некоторые операции легче выполнить, если document рассматривается как непрерывная последовательность текста.

`Range`— это «фасадный» интерфейс, который предоставляет методы, обрабатывающие document или части документа как «плоский» текст, независимо от того, что узлы document хранятся в древовидной объектной модели.

`Range` не содержит никакого текста или узлов, это просто представление или «окно» над фрагментом документа.

## Примеры

Показывает, как получить текстовое содержимое всех узлов, охватываемых диапазоном.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.Range.Text.Trim());
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
