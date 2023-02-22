---
title: Section.Body
second_title: Справочник по API Aspose.Words для .NET
description: Section свойство. Возвращает Тело дочерний узел раздела.
type: docs
weight: 20
url: /ru/net/aspose.words/section/body/
---
## Section.Body property

Возвращает **Тело** дочерний узел раздела.

```csharp
public Body Body { get; }
```

### Примечания

**Тело** содержит основной текст раздела.

Возвращает null, если раздел не имеет **Тело** узел среди его дочерних элементов.

### Примеры

Удаляет основной текст из всех разделов документа, оставляя сами разделы.

```csharp
Document doc = new Document();

// Пустой документ содержит один раздел, одно тело и один абзац.
// Вызовите метод "RemoveAllChildren", чтобы удалить все эти узлы,
// и получаем узел документа без дочерних элементов.
doc.RemoveAllChildren();

// Этот документ теперь не имеет составных дочерних узлов, к которым мы можем добавить содержимое.
// Если мы хотим отредактировать его, нам нужно будет повторно заполнить его коллекцию узлов.
// Сначала создайте новый раздел, а затем добавьте его как дочерний к корневому узлу документа.
Section section = new Section(doc);
doc.AppendChild(section);

// Разделу нужно тело, которое будет содержать и отображать все его содержимое
// на странице между шапкой и нижним колонтитулом раздела.
Body body = new Body(doc);
section.AppendChild(body);

// У этого тела нет дочерних элементов, поэтому мы пока не можем добавлять к нему прогоны.
Assert.AreEqual(0, doc.FirstSection.Body.GetChildNodes(NodeType.Any, true).Count);

// Вызовите "EnsureMinimum", чтобы убедиться, что это тело содержит хотя бы один пустой абзац. 
body.EnsureMinimum();

// Теперь мы можем добавить прогоны в тело и заставить документ отображать их.
body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Смотрите также

* class [Body](../../body/)
* class [Section](../)
* пространство имен [Aspose.Words](../../section/)
* сборка [Aspose.Words](../../../)


