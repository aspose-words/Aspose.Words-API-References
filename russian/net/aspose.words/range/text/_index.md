---
title: Range.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Range Text, чтобы легко извлекать и обрабатывать текст в указанном диапазоне для улучшенного управления контентом.
type: docs
weight: 60
url: /ru/net/aspose.words/range/text/
---
## Range.Text property

Получает текст диапазона.

```csharp
public string Text { get; }
```

## Примечания

Возвращаемая строка включает все управляющие и специальные символы, как описано в[`ControlChar`](../../controlchar/).

## Примеры

Показывает, как получить текстовое содержимое всех узлов, охватываемых диапазоном.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.Range.Text.Trim());
```

### Смотрите также

* class [Range](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
