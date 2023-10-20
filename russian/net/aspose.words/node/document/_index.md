---
title: Node.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words для .NET
description: Node Document свойство. Получает документ которому принадлежит этот узел на С#.
type: docs
weight: 20
url: /ru/net/aspose.words/node/document/
---
## Node.Document property

Получает документ, которому принадлежит этот узел.

```csharp
public virtual DocumentBase Document { get; }
```

## Примечания

Узел всегда принадлежит документу, даже если он только что был создан и еще не добавлен в дерево, или если он был удален из дерева.

## Примеры

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

* class [DocumentBase](../../documentbase/)
* class [Node](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
