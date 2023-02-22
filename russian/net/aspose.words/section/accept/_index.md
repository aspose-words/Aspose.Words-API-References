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
| visitor | DocumentVisitor | Посетитель, который будет посещать узлы. |

### Возвращаемое значение

Истинно, если все узлы были посещены; false, если DocumentVisitor остановил операцию перед посещением всех узлов.

### Примечания

Перечисляет этот узел и все его дочерние элементы. Каждый узел вызывает соответствующий метод в DocumentVisitor.

Дополнительные сведения см. в шаблоне проектирования «Посетитель».

Вызывает DocumentVisitor.VisitSectionStart, затем вызывает Accept для всех дочерних узлов section и вызывает DocumentVisitor.VisitSectionEnd в конце.

### Смотрите также

* class [DocumentVisitor](../../documentvisitor/)
* class [Section](../)
* пространство имен [Aspose.Words](../../section/)
* сборка [Aspose.Words](../../../)


