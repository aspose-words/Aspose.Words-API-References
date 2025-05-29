---
title: PageInfo.Colored
linktitle: Colored
articleTitle: Colored
second_title: Aspose.Words для .NET
description: Узнайте, содержит ли ваша страница яркий цветной контент с помощью свойства PageInfo Colored. Повысьте вовлеченность пользователей и улучшите визуальную привлекательность!
type: docs
weight: 10
url: /ru/net/aspose.words.rendering/pageinfo/colored/
---
## PageInfo.Colored property

Возврат`истинный` если страница содержит цветной контент.

```csharp
public bool Colored { get; }
```

## Примеры

Показывает, как проверить, цветная ли страница.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Убедитесь, что первая страница документа не цветная.
Assert.IsFalse(doc.GetPageInfo(0).Colored);
```

### Смотрите также

* class [PageInfo](../)
* пространство имен [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* сборка [Aspose.Words](../../../)
