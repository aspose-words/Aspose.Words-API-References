---
title: DocumentBuilder.Underline
second_title: Справочник по API Aspose.Words для .NET
description: DocumentBuilder свойство. Получает/устанавливает тип подчеркивания для текущего шрифта.
type: docs
weight: 170
url: /ru/net/aspose.words/documentbuilder/underline/
---
## DocumentBuilder.Underline property

Получает/устанавливает тип подчеркивания для текущего шрифта.

```csharp
public Underline Underline { get; set; }
```

### Примеры

Показывает, как форматировать текст, вставленный конструктором документов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Underline = Underline.Dash;
builder.Font.Color = Color.Blue;
builder.Font.Size = 32;

// Построитель применяет форматирование к своему текущему абзацу и любому новому тексту, добавленному им впоследствии.
builder.Writeln("Large, blue, and underlined text.");

doc.Save(ArtifactsDir + "DocumentBuilder.InsertUnderline.docx");
```

### Смотрите также

* enum [Underline](../../underline/)
* class [DocumentBuilder](../)
* пространство имен [Aspose.Words](../../documentbuilder/)
* сборка [Aspose.Words](../../../)


