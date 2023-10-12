---
title: Range.Text
second_title: Справочник по API Aspose.Words для .NET
description: Range свойство. Получает текст диапазона.
type: docs
weight: 60
url: /ru/net/aspose.words/range/text/
---
## Range.Text property

Получает текст диапазона.

```csharp
public string Text { get; }
```

### Примечания

Возвращенная строка включает все управляющие и специальные символы, как описано в разделе[`ControlChar`](../../controlchar/).

### Примеры

Показывает, как получить текстовое содержимое всех узлов, охватываемых диапазоном.

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


