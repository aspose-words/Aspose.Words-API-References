---
title: Node.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words для .NET
description: Легко дублируйте узлы с помощью метода Node Clone. Улучшите свой процесс разработки и оптимизируйте эффективность проекта уже сегодня!
type: docs
weight: 100
url: /ru/net/aspose.words/node/clone/
---
## Node.Clone method

Создает дубликат узла.

```csharp
public Node Clone(bool isCloneChildren)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| isCloneChildren | Boolean | True для рекурсивного клонирования поддерева под указанным узлом; false для клонирования только самого узла. |

### Возвращаемое значение

Клонированный узел.

## Примечания

Этот метод служит конструктором копирования для узлов. Клонированный узел не имеет родителя, но принадлежит тому же документу, что и исходный узел.

Этот метод всегда выполняет глубокое копирование узла.*isCloneChildren* параметр указывает, следует ли также выполнять копирование всех дочерних узлов.

## Примеры

Показывает, как клонировать составной узел.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;
para.AppendChild(new Run(doc, "Hello world!"));

// Ниже приведены два способа клонирования составного узла.
// 1 — Создать клон узла, а также создать клон каждого из его дочерних узлов.
Node cloneWithChildren = para.Clone(true);

Assert.IsTrue(((CompositeNode)cloneWithChildren).HasChildNodes);
Assert.AreEqual("Hello world!", cloneWithChildren.GetText().Trim());

// 2 - Создать клон узла без каких-либо дочерних узлов.
Node cloneWithoutChildren = para.Clone(false);

Assert.IsFalse(((CompositeNode)cloneWithoutChildren).HasChildNodes);
Assert.AreEqual(string.Empty, cloneWithoutChildren.GetText().Trim());
```

### Смотрите также

* class [Node](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
