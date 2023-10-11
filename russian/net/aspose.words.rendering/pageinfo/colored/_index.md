---
title: PageInfo.Colored
second_title: Справочник по API Aspose.Words для .NET
description: PageInfo свойство. Возвращаетистинный если страница содержит цветной контент.
type: docs
weight: 10
url: /ru/net/aspose.words.rendering/pageinfo/colored/
---
## PageInfo.Colored property

Возвращает`истинный` если страница содержит цветной контент.

```csharp
public bool Colored { get; }
```

### Примеры

Показывает, как проверить, цветная страница или нет.

```csharp
Document doc = new Document(MyDir + "Document.docx");

// Проверяем, что первая страница документа не окрашена.
Assert.IsFalse(doc.GetPageInfo(0).Colored);
```

### Смотрите также

* class [PageInfo](../)
* пространство имен [Aspose.Words.Rendering](../../pageinfo/)
* сборка [Aspose.Words](../../../)


