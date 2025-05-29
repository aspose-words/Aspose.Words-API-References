---
title: Font.EmphasisMark
linktitle: EmphasisMark
articleTitle: EmphasisMark
second_title: Aspose.Words для .NET
description: Узнайте, как использовать свойство Font Emphasis Mark для улучшения форматирования текста. Узнайте, как устанавливать и настраивать знаки акцента для лучшей читаемости.
type: docs
weight: 110
url: /ru/net/aspose.words/font/emphasismark/
---
## Font.EmphasisMark property

Возвращает или задает знак акцента, примененный к данному форматированию.

```csharp
public EmphasisMark EmphasisMark { get; set; }
```

## Примеры

Показывает, как добавить дополнительный символ, отображаемый над/под символом-глифом.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Возможные типы знаков ударения:
// https://apireference.aspose.com/words/net/aspose.words/emphasismark
builder.Font.EmphasisMark = emphasisMark; 

builder.Write("Emphasis text");
builder.Writeln();
builder.Font.ClearFormatting();
builder.Write("Simple text");

builder.Document.Save(ArtifactsDir + "Fonts.SetEmphasisMark.docx");
```

### Смотрите также

* enum [EmphasisMark](../../emphasismark/)
* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
