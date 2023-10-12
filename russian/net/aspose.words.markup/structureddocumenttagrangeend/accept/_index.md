---
title: StructuredDocumentTagRangeEnd.Accept
second_title: Справочник по API Aspose.Words для .NET
description: StructuredDocumentTagRangeEnd метод. Принимает посетителя.
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

Истинно, если были посещены все узлы; ложь, если[`DocumentVisitor`](../../../aspose.words/documentvisitor/) остановил операцию перед посещением всех узлов.

### Примечания

Перечисляет этот узел и все его дочерние элементы. Каждый узел вызывает соответствующий метод[`DocumentVisitor`](../../../aspose.words/documentvisitor/).

Дополнительные сведения см. в шаблоне проектирования «Посетитель».

### Смотрите также

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [StructuredDocumentTagRangeEnd](../)
* пространство имен [Aspose.Words.Markup](../../structureddocumenttagrangeend/)
* сборка [Aspose.Words](../../../)


