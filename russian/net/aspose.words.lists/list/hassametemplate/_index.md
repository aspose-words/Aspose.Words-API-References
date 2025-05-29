---
title: List.HasSameTemplate
linktitle: HasSameTemplate
articleTitle: HasSameTemplate
second_title: Aspose.Words для .NET
description: Откройте для себя метод HasSameTemplate, который позволяет легко проверить, используют ли два списка один и тот же шаблон, обеспечивая согласованность и эффективность управления данными.
type: docs
weight: 120
url: /ru/net/aspose.words.lists/list/hassametemplate/
---
## List.HasSameTemplate method

Возвращает true, если текущий список и заданный список созданы из одного и того же шаблона.

```csharp
public bool HasSameTemplate(List other)
```

## Примеры

Показывает, как определять списки с одинаковым ListDefId.

```csharp
Document doc = new Document(MyDir + "Different lists.docx");

Assert.True(doc.Lists[0].HasSameTemplate(doc.Lists[1]));
Assert.False(doc.Lists[1].HasSameTemplate(doc.Lists[2]));
```

### Смотрите также

* class [List](../)
* пространство имен [Aspose.Words.Lists](../../../aspose.words.lists/)
* сборка [Aspose.Words](../../../)
