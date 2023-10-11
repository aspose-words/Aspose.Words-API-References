---
title: Section.Body
second_title: Справочник по API Aspose.Words для .NET
description: Section свойство. ВозвращаетBody дочерний узел раздела.
type: docs
weight: 20
url: /ru/net/aspose.words/section/body/
---
## Section.Body property

Возвращает[`Body`](../../body/) дочерний узел раздела.

```csharp
public Body Body { get; }
```

### Примечания

[`Body`](../../body/) содержит основной текст раздела.

Возврат`нулевой` если в разделе нет[`Body`](../../body/) узел среди своих дочерних элементов.

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

* class [Body](../../body/)
* class [Section](../)
* пространство имен [Aspose.Words](../../section/)
* сборка [Aspose.Words](../../../)


