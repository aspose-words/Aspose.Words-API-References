---
title: ControlChar.Tab
linktitle: Tab
articleTitle: Tab
second_title: Aspose.Words для .NET
description: Откройте для себя поле ControlChar Tab, изучите символ табуляции x0009 для эффективного форматирования текста и улучшенного управления данными.
type: docs
weight: 270
url: /ru/net/aspose.words/controlchar/tab/
---
## ControlChar.Tab field

Символ табуляции: "\x0009" или "\t".

```csharp
public static readonly string Tab;
```

## Примеры

Показывает, как задать пользовательский интервал для позиций табуляции.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Установите позиции табуляции так, чтобы они отображались каждые 72 пункта (1 дюйм).
builder.Document.DefaultTabStop = 72;

// Каждый символ табуляции привязывает текст после себя к следующей ближайшей позиции табуляции.
builder.Writeln("Hello" + ControlChar.Tab + "World!");
builder.Writeln("Hello" + ControlChar.TabChar + "World!");
```

### Смотрите также

* class [ControlChar](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
