---
title: Font.Bold
linktitle: Bold
articleTitle: Bold
second_title: Aspose.Words для .NET
description: Font Bold свойство. True если шрифт отформатирован как жирный на С#.
type: docs
weight: 40
url: /ru/net/aspose.words/font/bold/
---
## Font.Bold property

True, если шрифт отформатирован как жирный.

```csharp
public bool Bold { get; set; }
```

## Примеры

Показывает, как вставлять форматированный текст с помощью DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Укажите форматирование шрифта, затем добавьте текст.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
