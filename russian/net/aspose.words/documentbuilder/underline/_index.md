---
title: DocumentBuilder.Underline
linktitle: Underline
articleTitle: Underline
second_title: Aspose.Words для .NET
description: Откройте для себя свойство DocumentBuilder Underline, чтобы легко настраивать стили шрифтов. Улучшите свои документы с помощью универсальных вариантов подчеркивания для профессионального вида.
type: docs
weight: 190
url: /ru/net/aspose.words/documentbuilder/underline/
---
## DocumentBuilder.Underline property

Получает/устанавливает тип подчеркивания для текущего шрифта.

```csharp
public Underline Underline { get; set; }
```

## Примеры

Показывает, как форматировать текст, вставленный с помощью конструктора документов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Underline = Underline.Dash;
builder.Font.Color = Color.Blue;
builder.Font.Size = 32;

// Конструктор применяет форматирование к текущему абзацу и любому новому тексту, добавленному им впоследствии.
builder.Writeln("Large, blue, and underlined text.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertUnderline.docx");
```

### Смотрите также

* enum [Underline](../../underline/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
