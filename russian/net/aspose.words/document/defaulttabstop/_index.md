---
title: Document.DefaultTabStop
linktitle: DefaultTabStop
articleTitle: DefaultTabStop
second_title: Aspose.Words для .NET
description: Узнайте, как настроить свойство DefaultTabStop, чтобы задать точные интервалы табуляции в пунктах, улучшив форматирование и макет документа.
type: docs
weight: 100
url: /ru/net/aspose.words/document/defaulttabstop/
---
## Document.DefaultTabStop property

Возвращает или задает интервал (в пунктах) между позициями табуляции по умолчанию.

```csharp
public double DefaultTabStop { get; set; }
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

* class [TabStopCollection](../../tabstopcollection/)
* class [TabStop](../../tabstop/)
* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
