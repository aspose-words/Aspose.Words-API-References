---
title: Range.Text
second_title: Справочник по API Aspose.Words для .NET
description: Range свойство. Получает текст диапазона.
type: docs
weight: 50
url: /ru/net/aspose.words/range/text/
---
## Range.Text property

Получает текст диапазона.

```csharp
public string Text { get; }
```

### Примечания

Возвращаемая строка включает все управляющие и специальные символы, как описано в[`ControlChar`](../../controlchar/).

### Примеры

Показывает, как получить текстовое содержимое всех узлов, которые охватывает диапазон.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.Range.Text.Trim());
```

### Смотрите также

* class [Range](../)
* пространство имен [Aspose.Words](../../range/)
* сборка [Aspose.Words](../../../)


