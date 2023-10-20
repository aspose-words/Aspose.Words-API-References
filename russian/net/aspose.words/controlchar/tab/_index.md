---
title: ControlChar.Tab
linktitle: Tab
articleTitle: Tab
second_title: Aspose.Words для .NET
description: ControlChar Tab поле. Символ табуляции x0009 или t на С#.
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

Показывает, как установить собственный интервал для позиций табуляции.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Установите позиции табуляции так, чтобы они появлялись каждые 72 пункта (1 дюйм).
builder.Document.DefaultTabStop = 72;

// Каждый символ табуляции привязывает текст после него к следующей ближайшей позиции табуляции.
builder.Writeln("Hello" + ControlChar.Tab + "World!");
builder.Writeln("Hello" + ControlChar.TabChar + "World!");
```

### Смотрите также

* class [ControlChar](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
