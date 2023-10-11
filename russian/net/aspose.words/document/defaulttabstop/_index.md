---
title: Document.DefaultTabStop
second_title: Справочник по API Aspose.Words для .NET
description: Document свойство. Получает или задает интервал в пунктах между позициями табуляции по умолчанию.
type: docs
weight: 90
url: /ru/net/aspose.words/document/defaulttabstop/
---
## Document.DefaultTabStop property

Получает или задает интервал (в пунктах) между позициями табуляции по умолчанию.

```csharp
public double DefaultTabStop { get; set; }
```

### Примеры

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

* class [TabStopCollection](../../tabstopcollection/)
* class [TabStop](../../tabstop/)
* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)


