---
title: ControlChar.TabChar
linktitle: TabChar
articleTitle: TabChar
second_title: Aspose.Words для .NET
description: Мастер полей TabChar с ControlChar для бесшовного управления данными. Раскройте эффективность с помощью универсального символа табуляции (char9 или t) сегодня!
type: docs
weight: 280
url: /ru/net/aspose.words/controlchar/tabchar/
---
## ControlChar.TabChar field

Символ табуляции: (char)9 или "\t".

```csharp
public const char TabChar;
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
