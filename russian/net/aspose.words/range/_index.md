---
title: Range Class
linktitle: Range
articleTitle: Range
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Range, ваш ключ к управлению разделами документа без усилий. Улучшите обработку документов с помощью бесшовного контроля и гибкости.
type: docs
weight: 5250
url: /ru/net/aspose.words/range/
---
## Range class

Представляет непрерывную область в документе.

Чтобы узнать больше, посетите[Работа с диапазонами](https://docs.aspose.com/words/net/working-with-ranges/) документальная статья.

```csharp
public class Range : IEnumerable<Node>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Bookmarks](../../aspose.words/range/bookmarks/) { get; } | Возвращает[`Bookmarks`](./bookmarks/) коллекция, представляющая все закладки в диапазоне . |
| [Fields](../../aspose.words/range/fields/) { get; } | Возвращает[`Fields`](./fields/) коллекция, представляющая все поля в диапазоне. |
| [FormFields](../../aspose.words/range/formfields/) { get; } | Возвращает[`FormFields`](./formfields/) коллекция, представляющая все поля формы в диапазоне . |
| [Revisions](../../aspose.words/range/revisions/) { get; } | Получает коллекцию ревизий (отслеживаемых изменений), которые существуют в этом диапазоне. |
| [StructuredDocumentTags](../../aspose.words/range/structureddocumenttags/) { get; } | Возвращает[`StructuredDocumentTags`](./structureddocumenttags/) коллекция, представляющая все структурированные теги документов в диапазоне . |
| [Text](../../aspose.words/range/text/) { get; } | Получает текст диапазона. |

## Методы

| Имя | Описание |
| --- | --- |
| [Delete](../../aspose.words/range/delete/)() | Удаляет все символы диапазона. |
| [GetEnumerator](../../aspose.words/range/getenumerator/)() |  |
| [NormalizeFieldTypes](../../aspose.words/range/normalizefieldtypes/)() | Изменяет значения типа поля[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype/) из[`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../aspose.words.fields/fieldend/) в этом диапазоне, чтобы они соответствовали типам полей, содержащимся в кодах полей. |
| [Replace](../../aspose.words/range/replace/#replace_2)(*Regex, string*) | Заменяет все вхождения шаблона символа, заданного регулярным выражением, на другую строку. |
| [Replace](../../aspose.words/range/replace/#replace)(*string, string*) | Заменяет все вхождения указанного шаблона строки символов на заменяющую строку. |
| [Replace](../../aspose.words/range/replace/#replace_3)(*Regex, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | Заменяет все вхождения шаблона символа, заданного регулярным выражением, на другую строку. |
| [Replace](../../aspose.words/range/replace/#replace_1)(*string, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | Заменяет все вхождения указанного шаблона строки символов на заменяющую строку. |
| [ToDocument](../../aspose.words/range/todocument/)() | Создает новый полностью сформированный документ, содержащий диапазон. |
| [UnlinkFields](../../aspose.words/range/unlinkfields/)() | Отменяет связь полей в этом диапазоне. |
| [UpdateFields](../../aspose.words/range/updatefields/)() | Обновляет значения полей документа в этом диапазоне. |

## Примечания

Документ представлен деревом узлов, а узлы предоставляют operations для работы с деревом, но некоторые операции выполнять проще, если document рассматривать как непрерывную последовательность текста.

`Range` представляет собой «фасадный» интерфейс, предоставляющий методы, которые обрабатывают document или части документа как «плоский» текст, независимо от того, что узлы document хранятся в древовидной объектной модели.

`Range` не содержит текста или узлов, это просто вид или «окно» над фрагментом документа.

## Примеры

Показывает, как получить текстовое содержимое всех узлов, охватываемых диапазоном.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.Range.Text.Trim());
```

### Смотрите также

* class [Node](../node/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
