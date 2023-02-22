---
title: Class Range
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Range сорт. Представляет непрерывную область в документе.
type: docs
weight: 4270
url: /ru/net/aspose.words/range/
---
## Range class

Представляет непрерывную область в документе.

```csharp
public class Range
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Bookmarks](../../aspose.words/range/bookmarks/) { get; } | Возвращает[`Bookmarks`](./bookmarks/) коллекция, представляющая все закладки в диапазоне. |
| [Fields](../../aspose.words/range/fields/) { get; } | Возвращает[`Fields`](./fields/) коллекция, представляющая все поля в диапазоне. |
| [FormFields](../../aspose.words/range/formfields/) { get; } | Возвращает[`FormFields`](./formfields/) коллекция, представляющая все поля формы в диапазоне. |
| [StructuredDocumentTags](../../aspose.words/range/structureddocumenttags/) { get; } | Возвращает[`StructuredDocumentTags`](./structureddocumenttags/) коллекция, которая представляет все теги структурированного документа в диапазоне. |
| [Text](../../aspose.words/range/text/) { get; } | Получает текст диапазона. |

## Методы

| Имя | Описание |
| --- | --- |
| [Delete](../../aspose.words/range/delete/)() | Удаляет все символы диапазона. |
| [NormalizeFieldTypes](../../aspose.words/range/normalizefieldtypes/)() | Изменяет значения типа поля[`FieldType`](../../aspose.words.fields/fieldchar/fieldtype/) из[`FieldStart`](../../aspose.words.fields/fieldstart/) ,[`FieldSeparator`](../../aspose.words.fields/fieldseparator/) ,[`FieldEnd`](../../aspose.words.fields/fieldend/) в этом диапазоне, чтобы они соответствовали типам полей, содержащимся в кодах полей. |
| [Replace](../../aspose.words/range/replace/#replace_2)(Regex, string) | Заменяет все вхождения шаблона символов, заданного регулярным выражением, другой строкой. |
| [Replace](../../aspose.words/range/replace/#replace)(string, string) | Заменяет все вхождения указанного шаблона строки символов замещающей строкой. |
| [Replace](../../aspose.words/range/replace/#replace_3)(Regex, string, FindReplaceOptions) | Заменяет все вхождения шаблона символов, заданного регулярным выражением, другой строкой. |
| [Replace](../../aspose.words/range/replace/#replace_1)(string, string, FindReplaceOptions) | Заменяет все вхождения указанного шаблона строки символов замещающей строкой. |
| [ToDocument](../../aspose.words/range/todocument/)() | Создает новый полностью сформированный документ, содержащий диапазон. |
| [UnlinkFields](../../aspose.words/range/unlinkfields/)() | Разъединяет поля в этом диапазоне. |
| [UpdateFields](../../aspose.words/range/updatefields/)() | Обновляет значения полей документа в этом диапазоне. |

### Примечания

Документ представлен деревом узлов, а узлы предоставляют операции для работы с деревом, но некоторые операции проще выполнять, если документ рассматривать как непрерывную последовательность текста.

**Диапазон** представляет собой «фасадный» интерфейс, предоставляющий методы, обрабатывающие document или части документа как «плоский» текст, независимо от того факта, что узлы document хранятся в древовидной объектной модели.

**Диапазон** не содержит текста или узлов, это просто вид или "окно" над фрагментом документа.

### Примеры

Показывает, как получить текстовое содержимое всех узлов, которые охватывает диапазон.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.Range.Text.Trim());
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


