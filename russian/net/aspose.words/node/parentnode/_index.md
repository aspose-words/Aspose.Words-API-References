---
title: Node.ParentNode
linktitle: ParentNode
articleTitle: ParentNode
second_title: Aspose.Words для .NET
description: Node ParentNode свойство. Получает непосредственного родителя этого узла на С#.
type: docs
weight: 60
url: /ru/net/aspose.words/node/parentnode/
---
## Node.ParentNode property

Получает непосредственного родителя этого узла.

```csharp
public CompositeNode ParentNode { get; }
```

## Примечания

Если узел только что был создан и еще не добавлен в дерево, , или если он был удален из дерева, родительским элементом является`нулевой`.

## Примеры

Показывает, как получить доступ к родительскому узлу узла.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Добавляем дочерний узел Run к первому абзацу документа.
Run run = new Run(doc, "Hello world!");
para.AppendChild(run);

// Абзац является родительским узлом узла выполнения. Мы можем проследить эту родословную
// вплоть до узла документа, который является корнем дерева узлов документа.
Assert.AreEqual(para, run.ParentNode);
Assert.AreEqual(doc.FirstSection.Body, para.ParentNode);
Assert.AreEqual(doc.FirstSection, doc.FirstSection.Body.ParentNode);
Assert.AreEqual(doc, doc.FirstSection.ParentNode);
```

Показывает, как создать узел и установить для него документ-владелец.

```csharp
Document doc = new Document();
Paragraph para = new Paragraph(doc);
para.AppendChild(new Run(doc, "Hello world!"));

// Мы еще не добавили этот абзац как дочерний ни к одному составному узлу.
Assert.IsNull(para.ParentNode);

// Если узел является подходящим типом дочернего узла другого составного узла,
// мы можем прикрепить его как дочерний, только если оба узла имеют один и тот же документ-владелец.
// Документ-владелец — это документ, который мы передали конструктору узла.
// Мы не прикрепили этот абзац к документу, поэтому документ не содержит его текста.
Assert.AreEqual(para.Document, doc);
Assert.AreEqual(string.Empty, doc.GetText().Trim());

// Поскольку документ владеет этим абзацем, мы можем применить один из его стилей к содержимому абзаца.
para.ParagraphFormat.Style = doc.Styles["Heading 1"];

// Добавляем этот узел в документ, а затем проверяем его содержимое.
doc.FirstSection.Body.AppendChild(para);

Assert.AreEqual(doc.FirstSection.Body, para.ParentNode);
Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Смотрите также

* class [CompositeNode](../../compositenode/)
* class [Node](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
