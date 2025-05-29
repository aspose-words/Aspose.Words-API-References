---
title: Body.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: Aspose.Words для .NET
description: Оптимизируйте свой контент с помощью метода Body EnsureMinimum. Автоматически добавляйте пустой абзац, если последний дочерний элемент не является абзацем, для лучшего форматирования.
type: docs
weight: 70
url: /ru/net/aspose.words/body/ensureminimum/
---
## Body.EnsureMinimum method

Если последний дочерний элемент не является абзацем, создает и добавляет один пустой абзац.

```csharp
public void EnsureMinimum()
```

## Примеры

Удаляет основной текст из всех разделов документа, оставляя сами разделы.

```csharp
Document doc = new Document();

// Пустой документ содержит один раздел, одно тело и один абзац.
// Вызываем метод "RemoveAllChildren", чтобы удалить все эти узлы,
// и в итоге получаем узел документа без дочерних элементов.
doc.RemoveAllChildren();

// В этом документе теперь нет составных дочерних узлов, в которые мы можем добавлять контент.
// Если мы хотим его отредактировать, нам нужно будет заново заполнить его коллекцию узлов.
// Сначала создадим новый раздел, а затем добавим его как дочерний элемент к корневому узлу документа.
Section section = new Section(doc);
doc.AppendChild(section);

// Разделу необходимо тело, которое будет содержать и отображать все его содержимое
// на странице между верхним и нижним колонтитулами раздела.
Body body = new Body(doc);
section.AppendChild(body);

// У этого тела нет дочерних элементов, поэтому мы пока не можем добавлять к нему маршруты.
Assert.AreEqual(0, doc.FirstSection.Body.GetChildNodes(NodeType.Any, true).Count);

 // Вызовите «EnsureMinimum», чтобы убедиться, что этот текст содержит хотя бы один пустой абзац.
body.EnsureMinimum();

// Теперь мы можем добавить прогоны в тело и заставить документ отображать их.
body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Смотрите также

* class [Body](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
