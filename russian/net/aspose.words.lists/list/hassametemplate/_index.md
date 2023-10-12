---
title: List.HasSameTemplate
second_title: Справочник по API Aspose.Words для .NET
description: List метод. Возвращает true если текущий список и данный список созданы на основе одного и того же шаблона.
type: docs
weight: 120
url: /ru/net/aspose.words.lists/list/hassametemplate/
---
## List.HasSameTemplate method

Возвращает true, если текущий список и данный список созданы на основе одного и того же шаблона.

```csharp
public bool HasSameTemplate(List other)
```

### Примеры

Показывает, как определять списки с одинаковым ListDefId.

```csharp
Document doc = new Document(MyDir + "Different lists.docx");

Assert.True(doc.Lists[0].HasSameTemplate(doc.Lists[1]));
Assert.False(doc.Lists[1].HasSameTemplate(doc.Lists[2]));
```

### Смотрите также

* class [List](../)
* пространство имен [Aspose.Words.Lists](../../list/)
* сборка [Aspose.Words](../../../)


