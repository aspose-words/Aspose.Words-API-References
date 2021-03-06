---
title: HighlightColor
second_title: Справочник по API Aspose.Words для .NET
description: Получает или задает цвет выделения маркера.
type: docs
weight: 150
url: /ru/net/aspose.words/font/highlightcolor/
---
## Font.HighlightColor property

Получает или задает цвет выделения (маркера).

```csharp
public Color HighlightColor { get; set; }
```

### Примеры

Показывает, как отформатировать набор текста, используя его свойство шрифта.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

### Смотрите также

* class [Font](../../font)
* пространство имен [Aspose.Words](../../font)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
