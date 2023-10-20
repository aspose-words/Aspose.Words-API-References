---
title: ParagraphFormat.BaselineAlignment
linktitle: BaselineAlignment
articleTitle: BaselineAlignment
second_title: Aspose.Words для .NET
description: ParagraphFormat BaselineAlignment свойство. Получает или задает вертикальное положение шрифта в строке на С#.
type: docs
weight: 40
url: /ru/net/aspose.words/paragraphformat/baselinealignment/
---
## ParagraphFormat.BaselineAlignment property

Получает или задает вертикальное положение шрифта в строке.

```csharp
public BaselineAlignment BaselineAlignment { get; set; }
```

## Примеры

Показывает, как установить вертикальное положение шрифтов в строке.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

ParagraphFormat format = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat;
if (format.BaselineAlignment == BaselineAlignment.Auto)
{                
    format.BaselineAlignment = BaselineAlignment.Top;
}

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphBaselineAlignment.docx");
```

### Смотрите также

* enum [BaselineAlignment](../../baselinealignment/)
* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
