---
title: ParagraphFormat.BaselineAlignment
linktitle: BaselineAlignment
articleTitle: BaselineAlignment
second_title: Aspose.Words для .NET
description: Оптимизируйте макет текста с помощью свойства ParagraphFormat BaselineAlignment, позволяющего точно контролировать вертикальное расположение шрифта для улучшения читаемости.
type: docs
weight: 40
url: /ru/net/aspose.words/paragraphformat/baselinealignment/
---
## ParagraphFormat.BaselineAlignment property

Возвращает или задает вертикальное положение шрифтов в строке.

```csharp
public BaselineAlignment BaselineAlignment { get; set; }
```

## Примеры

Показывает, как задать вертикальное положение шрифтов в строке.

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
