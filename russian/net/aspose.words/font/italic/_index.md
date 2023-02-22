---
title: Font.Italic
second_title: Справочник по API Aspose.Words для .NET
description: Font свойство. Истинно если шрифт отформатирован как курсив.
type: docs
weight: 160
url: /ru/net/aspose.words/font/italic/
---
## Font.Italic property

Истинно, если шрифт отформатирован как курсив.

```csharp
public bool Italic { get; set; }
```

### Примеры

Показывает, как написать выделенный курсивом текст с помощью конструктора документов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.Italic = true;
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "Font.Italic.docx");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../font/)
* сборка [Aspose.Words](../../../)


