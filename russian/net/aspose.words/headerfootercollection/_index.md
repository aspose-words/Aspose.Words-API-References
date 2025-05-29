---
title: HeaderFooterCollection Class
linktitle: HeaderFooterCollection
articleTitle: HeaderFooterCollection
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.HeaderFooterCollection для простого типизированного доступа к узлам Section HeaderFooter, оптимизируя управление документами и улучшая рабочий процесс.
type: docs
weight: 3540
url: /ru/net/aspose.words/headerfootercollection/
---
## HeaderFooterCollection class

Предоставляет типизированный доступ к[`HeaderFooter`](../headerfooter/) узлы[`Section`](../section/) .

Чтобы узнать больше, посетите[Работа с верхними и нижними колонтитулами](https://docs.aspose.com/words/net/working-with-headers-and-footers/) документальная статья.

```csharp
public class HeaderFooterCollection : NodeCollection
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Получает количество узлов в коллекции. |
| [Item](../../aspose.words/headerfootercollection/item/) { get; } | Извлекает[`HeaderFooter`](../headerfooter/) по данному индексу. (3 indexers) |

## Методы

| Имя | Описание |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Добавляет узел в конец коллекции. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Удаляет все узлы из этой коллекции и из документа. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Определяет, находится ли узел в коллекции. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Обеспечивает простую итерацию в стиле «foreach» по коллекции узлов. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Возвращает индекс указанного узла, отсчитываемый от нуля. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Вставляет узел в коллекцию по указанному индексу. |
| [LinkToPrevious](../../aspose.words/headerfootercollection/linktoprevious/#linktoprevious_1)(*bool*) | Связывает или отменяет связь всех верхних и нижних колонтитулов с соответствующими верхними и нижними колонтитулами в предыдущем разделе. |
| [LinkToPrevious](../../aspose.words/headerfootercollection/linktoprevious/#linktoprevious)(*[HeaderFooterType](../headerfootertype/), bool*) | Связывает или отменяет связь указанного верхнего или нижнего колонтитула с соответствующим верхним или нижним колонтитулом в предыдущем разделе. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Удаляет узел из коллекции и из документа. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Удаляет узел с указанным индексом из коллекции и из документа. |
| [ToArray](../../aspose.words/headerfootercollection/toarray/#toarray)() | Копирует все`ЗаголовокНижний колонтитул` s из коллекции в новый массив`ЗаголовокНижний колонтитул` с. (2 methods) |

## Примечания

Может быть максимум один[`HeaderFooter`](../headerfooter/)

каждого[`HeaderFooterType`](../headerfootertype/) per [`Section`](../section/) .

[`HeaderFooter`](../headerfooter/) Объекты могут располагаться в коллекции в любом порядке.

## Примеры

Показывает, как удалить все нижние колонтитулы из документа.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Проходим по каждому разделу и удаляем нижние колонтитулы всех видов.
foreach (Section section in doc.OfType<Section>())
{
    // Существует три типа нижних и верхних колонтитулов.
    // 1 — «Первый» верхний/нижний колонтитул, который отображается только на первой странице раздела.
    HeaderFooter footer = section.HeadersFooters[HeaderFooterType.FooterFirst];
    footer?.Remove();

    // 2 — «Основной» верхний/нижний колонтитул, который отображается на нечетных страницах.
    footer = section.HeadersFooters[HeaderFooterType.FooterPrimary];
    footer?.Remove();

     // 3 - «Четный» верхний/нижний колонтитул, который отображается на четных страницах.
    footer = section.HeadersFooters[HeaderFooterType.FooterEven];
    footer?.Remove();

    Assert.AreEqual(0, section.HeadersFooters.Count(hf => !((HeaderFooter)hf).IsHeader));
}

doc.Save(ArtifactsDir + "HeaderFooter.RemoveFooters.docx");
```

Показывает, как создать верхний и нижний колонтитул.

```csharp
Document doc = new Document();

// Создаем заголовок и добавляем к нему абзац. Текст в этом абзаце
// будет отображаться в верхней части каждой страницы этого раздела, над основным текстом.
HeaderFooter header = new HeaderFooter(doc, HeaderFooterType.HeaderPrimary);
doc.FirstSection.HeadersFooters.Add(header);

Paragraph para = header.AppendParagraph("My header.");

Assert.True(header.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

// Создаем нижний колонтитул и добавляем к нему абзац. Текст в этом абзаце
// будет отображаться внизу каждой страницы этого раздела, под основным текстом.
HeaderFooter footer = new HeaderFooter(doc, HeaderFooterType.FooterPrimary);
doc.FirstSection.HeadersFooters.Add(footer);

para = footer.AppendParagraph("My footer.");

Assert.False(footer.IsHeader);
Assert.True(para.IsEndOfHeaderFooter);

Assert.AreEqual(footer, para.ParentStory);
Assert.AreEqual(footer.ParentSection, para.ParentSection);
Assert.AreEqual(footer.ParentSection, header.ParentSection);

doc.Save(ArtifactsDir + "HeaderFooter.Create.docx");
```

### Смотрите также

* class [NodeCollection](../nodecollection/)
* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
