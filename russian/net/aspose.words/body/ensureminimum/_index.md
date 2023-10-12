---
title: Body.EnsureMinimum
second_title: Справочник по API Aspose.Words для .NET
description: Body метод. Если последний дочерний элемент не является абзацем создается и добавляется один пустой абзац.
type: docs
weight: 70
url: /ru/net/aspose.words/body/ensureminimum/
---
## Body.EnsureMinimum method

Если последний дочерний элемент не является абзацем, создается и добавляется один пустой абзац.

```csharp
public void EnsureMinimum()
```

### Примеры

Удаляет основной текст из всех разделов документа, оставляя сами разделы.

```csharp
Document doc = new Document();

// Пустой документ содержит один раздел, одно тело и один абзац.
// Вызов метода «RemoveAllChildren», чтобы удалить все эти узлы,
// и в итоге получим узел документа без дочерних элементов.
doc.RemoveAllChildren();

// В этом документе теперь нет составных дочерних узлов, к которым мы можем добавлять контент.
// Если мы хотим его отредактировать, нам нужно будет заново заполнить его коллекцию узлов.
// Сначала создаем новый раздел, а затем добавляем его как дочерний к корневому узлу документа.
Section section = new Section(doc);
doc.AppendChild(section);

// Разделу необходимо тело, которое будет содержать и отображать все его содержимое
// на странице между заголовком и подвалом раздела.
Body body = new Body(doc);
section.AppendChild(body);

// У этого тела нет дочерних элементов, поэтому мы пока не можем добавлять в него прогоны.
Assert.AreEqual(0, doc.FirstSection.Body.GetChildNodes(NodeType.Any, true).Count);

 // Вызовите «EnsureMinimum», чтобы убедиться, что это тело содержит хотя бы один пустой абзац.
body.EnsureMinimum();

// Теперь мы можем добавить прогоны в тело и заставить документ отображать их.
body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Смотрите также

* class [Body](../)
* пространство имен [Aspose.Words](../../body/)
* сборка [Aspose.Words](../../../)


