---
title: BaselineAlignment Enum
linktitle: BaselineAlignment
articleTitle: BaselineAlignment
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.BaselineAlignment для точного позиционирования шрифта. Улучшите форматирование документа с помощью оптимальных параметров вертикального выравнивания.
type: docs
weight: 130
url: /ru/net/aspose.words/baselinealignment/
---
## BaselineAlignment enumeration

Задает вертикальное положение шрифта в строке.

```csharp
public enum BaselineAlignment
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Top | `0` | Выравнивает по верхнему краю каждого шрифта. |
| Center | `1` | Выравнивает центральные точки каждого шрифта. |
| Baseline | `2` | Выравнивает по базовой линии абзаца. |
| Bottom | `3` | Выравнивает по нижнему краю каждого шрифта. |
| Auto | `4` | Базовая линия настраивается автоматически. |

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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
