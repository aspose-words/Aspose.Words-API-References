---
title: StructuredDocumentTagCollection Class
linktitle: StructuredDocumentTagCollection
articleTitle: StructuredDocumentTagCollection
second_title: Aspose.Words для .NET
description: Изучите класс Aspose.Words.Markup.StructuredDocumentTagCollection для эффективного управления структурированными тегами документов, расширяя возможности обработки документов.
type: docs
weight: 4760
url: /ru/net/aspose.words.markup/structureddocumenttagcollection/
---
## StructuredDocumentTagCollection class

Коллекция[`IStructuredDocumentTag`](../istructureddocumenttag/) экземпляры, представляющие структурированные теги документа в указанном диапазоне.

Чтобы узнать больше, посетите[Структурированные теги документов или контроль содержимого](https://docs.aspose.com/words/net/working-with-content-control-sdt/) документальная статья.

```csharp
public class StructuredDocumentTagCollection : IEnumerable<IStructuredDocumentTag>
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words.markup/structureddocumenttagcollection/count/) { get; } | Возвращает количество структурированных тегов документа в коллекции. |
| [Item](../../aspose.words.markup/structureddocumenttagcollection/item/) { get; } | Возвращает структурированный тег документа по указанному индексу. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetById](../../aspose.words.markup/structureddocumenttagcollection/getbyid/)(*int*) | Возвращает структурированный тег документа по идентификатору. |
| [GetByTag](../../aspose.words.markup/structureddocumenttagcollection/getbytag/)(*string*) | Возвращает первый структурированный тег документа, обнаруженный в коллекции с указанным тегом. |
| [GetByTitle](../../aspose.words.markup/structureddocumenttagcollection/getbytitle/)(*string*) | Возвращает первый структурированный тег документа, обнаруженный в коллекции с указанным заголовком. |
| [GetEnumerator](../../aspose.words.markup/structureddocumenttagcollection/getenumerator/)() | Возвращает объект перечислителя. |
| [Remove](../../aspose.words.markup/structureddocumenttagcollection/remove/)(*int*) | Удаляет структурированный тег документа с указанным идентификатором. |
| [RemoveAt](../../aspose.words.markup/structureddocumenttagcollection/removeat/)(*int*) | Удаляет структурированный тег документа по указанному индексу. |

## Примеры

Показывает, как получить структурированный тег документа.

```csharp
Document doc = new Document(MyDir + "Structured document tags by id.docx");

// Получить структурированный тег документа по идентификатору.
IStructuredDocumentTag sdt = doc.Range.StructuredDocumentTags.GetById(1160505028);
Console.WriteLine(sdt.IsMultiSection);
Console.WriteLine(sdt.Title);

// Получить структурированный тег документа или ранжированный тег по заголовку.
sdt = doc.Range.StructuredDocumentTags.GetByTitle("Alias4");
Console.WriteLine(sdt.Id);
```

### Смотрите также

* interface [IStructuredDocumentTag](../istructureddocumenttag/)
* пространство имен [Aspose.Words.Markup](../../aspose.words.markup/)
* сборка [Aspose.Words](../../)
