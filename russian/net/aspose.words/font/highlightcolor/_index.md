---
title: Font.HighlightColor
linktitle: HighlightColor
articleTitle: HighlightColor
second_title: Aspose.Words для .NET
description: Откройте для себя свойство Font HighlightColor — легко настройте цвет подсветки текста для улучшения читаемости и визуальной привлекательности. Поднимите свой дизайн на новый уровень!
type: docs
weight: 150
url: /ru/net/aspose.words/font/highlightcolor/
---
## Font.HighlightColor property

Получает или задает цвет выделения (маркера).

```csharp
public Color HighlightColor { get; set; }
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

### Смотрите также

* class [Font](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
