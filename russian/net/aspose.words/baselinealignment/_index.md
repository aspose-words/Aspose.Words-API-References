---
title: Enum BaselineAlignment
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.BaselineAlignment перечисление. Определяет вертикальное положение шрифтов в строке.
type: docs
weight: 20
url: /ru/net/aspose.words/baselinealignment/
---
## BaselineAlignment enumeration

Определяет вертикальное положение шрифтов в строке.

```csharp
public enum BaselineAlignment
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Top | `0` | Выравнивается по верху каждого шрифта. |
| Center | `1` | Выравнивает центральные точки каждого шрифта. |
| Baseline | `2` | Выравнивается по базовой линии абзаца. |
| Bottom | `3` | Выравнивается по нижней части каждого шрифта. |
| Auto | `4` | Базовая линия корректируется автоматически. |

### Примеры

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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


