---
title: Font.Size
linktitle: Size
articleTitle: Size
second_title: Aspose.Words для .NET
description: Легко настройте размер шрифта с помощью свойства Font Size. Настройте текст в пунктах для улучшения читаемости и привлекательности дизайна.
type: docs
weight: 350
url: /ru/net/aspose.words/font/size/
---
## Font.Size property

Получает или задает размер шрифта в пунктах.

```csharp
public double Size { get; set; }
```

## Примеры

Показывает, как отформатировать фрагмент текста, используя его свойство шрифта.

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

Показывает, как вставлять форматированный текст с помощью DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Укажите форматирование шрифта, затем добавьте текст.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
