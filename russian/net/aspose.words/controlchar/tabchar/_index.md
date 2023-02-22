---
title: ControlChar.TabChar
second_title: Справочник по API Aspose.Words для .NET
description: ControlChar поле. Символ табуляции char9 или t.
type: docs
weight: 280
url: /ru/net/aspose.words/controlchar/tabchar/
---
## ControlChar.TabChar field

Символ табуляции: (char)9 или "\t".

```csharp
public const char TabChar;
```

### Примеры

Показывает, как установить собственный интервал для позиций табуляции.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Установите позиции табуляции так, чтобы они появлялись через каждые 72 пункта (1 дюйм).
builder.Document.DefaultTabStop = 72;

// Каждый символ табуляции привязывает текст после него к ближайшей позиции табуляции.
builder.Writeln("Hello" + ControlChar.Tab + "World!");
builder.Writeln("Hello" + ControlChar.TabChar + "World!");
```

### Смотрите также

* class [ControlChar](../)
* пространство имен [Aspose.Words](../../controlchar/)
* сборка [Aspose.Words](../../../)


