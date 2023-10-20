---
title: StructuredDocumentTagRangeStart.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words для .NET
description: StructuredDocumentTagRangeStart Accept метод. Принимает посетителя на С#.
type: docs
weight: 190
url: /ru/net/aspose.words.markup/structureddocumenttagrangestart/accept/
---
## StructuredDocumentTagRangeStart.Accept method

Принимает посетителя.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| visitor | DocumentVisitor | Посетитель, который посетит узлы. |

### Возвращаемое значение

Истинно, если были посещены все узлы; ложь, если[`DocumentVisitor`](../../../aspose.words/documentvisitor/) остановил операцию перед посещением всех узлов.

## Примечания

Перечисляет этот узел и все его дочерние элементы. Каждый узел вызывает соответствующий метод[`DocumentVisitor`](../../../aspose.words/documentvisitor/).

Дополнительные сведения см. в шаблоне проектирования «Посетитель».

### Смотрите также

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [StructuredDocumentTagRangeStart](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
