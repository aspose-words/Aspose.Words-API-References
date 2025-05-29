---
title: Document.GetPageInfo
linktitle: GetPageInfo
articleTitle: GetPageInfo
second_title: Aspose.Words для .NET
description: Откройте для себя метод GetPageInfo, позволяющий получить основные данные о размере страницы, ее ориентации и рендеринге для оптимизированной печати и улучшенного управления документами.
type: docs
weight: 650
url: /ru/net/aspose.words/document/getpageinfo/
---
## Document.GetPageInfo method

Получает размер страницы, ориентацию и другую информацию о странице, которая может быть полезна для печати или рендеринга.

```csharp
public PageInfo GetPageInfo(int pageIndex)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| pageIndex | Int32 | Индекс страниц, начинающийся с 0. |

## Примеры

Показывает, как проверить, цветная ли страница.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Убедитесь, что первая страница документа не цветная.
Assert.IsFalse(doc.GetPageInfo(0).Colored);
```

### Смотрите также

* class [PageInfo](../../../aspose.words.rendering/pageinfo/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
