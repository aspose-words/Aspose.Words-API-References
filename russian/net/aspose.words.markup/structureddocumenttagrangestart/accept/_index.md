---
title: StructuredDocumentTagRangeStart.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words для .NET
description: Узнайте, как метод StructuredDocumentTagRangeStart Accept улучшает обработку документов, эффективно принимая посетителей для бесшовной интеграции.
type: docs
weight: 200
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

True, если все узлы были посещены; false, если[`DocumentVisitor`](../../../aspose.words/documentvisitor/) остановил операцию до посещения всех узлов.

## Примечания

Перечисляет этот узел и всех его потомков. Каждый узел вызывает соответствующий метод на[`DocumentVisitor`](../../../aspose.words/documentvisitor/).

Более подробную информацию см. в шаблоне проектирования «Посетитель».

### Смотрите также

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [StructuredDocumentTagRangeStart](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
