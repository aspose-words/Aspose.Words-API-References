---
title: Section.Accept
second_title: Справочник по API Aspose.Words для .NET
description: Section метод. Принимает посетителя.
type: docs
weight: 70
url: /ru/net/aspose.words/section/accept/
---
## Section.Accept method

Принимает посетителя.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| visitor | DocumentVisitor | Посетитель, который посетит узлы. |

### Возвращаемое значение

Истинно, если были посещены все узлы; ложь, если[`DocumentVisitor`](../../documentvisitor/) остановил операцию перед посещением всех узлов.

### Примечания

Перечисляет этот узел и все его дочерние элементы. Каждый узел вызывает соответствующий метод[`DocumentVisitor`](../../documentvisitor/).

Дополнительные сведения см. в шаблоне проектирования «Посетитель».

Звонки[`VisitSectionStart`](../../documentvisitor/visitsectionstart/) , затем звонит[`Accept`](../../node/accept/) для всех дочерних узловsection и вызовов[`VisitSectionEnd`](../../documentvisitor/visitsectionend/) в конце.

### Смотрите также

* class [DocumentVisitor](../../documentvisitor/)
* class [Section](../)
* пространство имен [Aspose.Words](../../section/)
* сборка [Aspose.Words](../../../)


