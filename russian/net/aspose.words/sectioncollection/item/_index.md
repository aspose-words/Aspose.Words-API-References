---
title: SectionCollection.Item
second_title: Справочник по API Aspose.Words для .NET
description: SectionCollection свойство. Извлекает раздел по заданному индексу.
type: docs
weight: 10
url: /ru/net/aspose.words/sectioncollection/item/
---
## SectionCollection indexer

Извлекает раздел по заданному индексу.

```csharp
public Section this[int index] { get; }
```

| Параметр | Описание |
| --- | --- |
| index | Индекс в списке разделов. |

### Примечания

Индекс отсчитывается от нуля.

Отрицательные индексы разрешены и указывают на доступ из задней части коллекции. Например, -1 означает последний элемент, -2 означает предпоследний элемент и так далее.

Если индекс больше или равен количеству элементов в списке, возвращается нулевая ссылка.

Если индекс отрицателен и его абсолютное значение превышает количество элементов в списке, возвращается нулевая ссылка.

### Примеры

Показывает, когда следует пересчитать макет страницы документа.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Сохранение документа в формате PDF, в изображение или первая печать автоматически
// кэшируем макет документа на его страницах.
doc.Save(ArtifactsDir + "Document.UpdatePageLayout.1.pdf");

// Изменить каким-либо образом документ.
doc.Styles["Normal"].Font.Size = 6;
doc.Sections[0].PageSetup.Orientation = Aspose.Words.Orientation.Landscape;
doc.Sections[0].PageSetup.Margins = Margins.Mirrored;

 // В текущей версии Aspose.Words изменение документа не приводит к автоматической перестройке
// кэшированный макет страницы. Если мы хотим кэшированный макет
// чтобы оставаться в курсе событий, нам нужно будет обновлять его вручную.
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Document.UpdatePageLayout.2.pdf");
```

Показывает, как подготовить новый узел раздела к редактированию.

```csharp
Document doc = new Document();

// Пустой документ имеет раздел, в котором есть тело, которое, в свою очередь, имеет абзац.
// Мы можем добавить содержимое в этот документ, добавив в этот абзац такие элементы, как текстовые фрагменты, фигуры или таблицы.
Assert.AreEqual(NodeType.Section, doc.GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Body, doc.Sections[0].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[0].Body.GetChild(NodeType.Any, 0, true).NodeType);

// Если мы добавим новый раздел таким образом, у него не будет тела или других дочерних узлов.
doc.Sections.Add(new Section(doc));

Assert.AreEqual(0, doc.Sections[1].GetChildNodes(NodeType.Any, true).Count);

// Запускаем метод EnsureMinimum, чтобы добавить тело и абзац в этот раздел и начать его редактирование.
doc.LastSection.EnsureMinimum();

Assert.AreEqual(NodeType.Body, doc.Sections[1].GetChild(NodeType.Any, 0, true).NodeType);
Assert.AreEqual(NodeType.Paragraph, doc.Sections[1].Body.GetChild(NodeType.Any, 0, true).NodeType);

doc.Sections[0].Body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Смотрите также

* class [Section](../../section/)
* class [SectionCollection](../)
* пространство имен [Aspose.Words](../../sectioncollection/)
* сборка [Aspose.Words](../../../)


