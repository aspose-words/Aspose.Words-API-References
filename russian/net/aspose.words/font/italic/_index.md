---
title: Font.Italic
linktitle: Italic
articleTitle: Italic
second_title: Aspose.Words для .NET
description: Font Italic свойство. True если шрифт отформатирован как курсив на С#.
type: docs
weight: 160
url: /ru/net/aspose.words/font/italic/
---
## Font.Italic property

True, если шрифт отформатирован как курсив.

```csharp
public bool Italic { get; set; }
```

## Примеры

Показывает, как написать курсивный текст с помощью построителя документов.

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
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
