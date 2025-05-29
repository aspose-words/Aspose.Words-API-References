---
title: StructuredDocumentTagRangeEnd.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words для .NET
description: Изучите метод StructuredDocumentTagRangeEnd Accept. Улучшите обработку документов, эффективно управляя взаимодействием посетителей.
type: docs
weight: 40
url: /ru/net/aspose.words.markup/structureddocumenttagrangeend/accept/
---
## StructuredDocumentTagRangeEnd.Accept method

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
* class [StructuredDocumentTagRangeEnd](../)
* пространство имен [Aspose.Words.Markup](../../../aspose.words.markup/)
* сборка [Aspose.Words](../../../)
