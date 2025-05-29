---
title: EmphasisMark Enum
linktitle: EmphasisMark
articleTitle: EmphasisMark
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.EmphasisMark, включающее различные типы акцента для улучшения форматирования вашего документа. Повысьте воздействие вашего текста сегодня!
type: docs
weight: 1870
url: /ru/net/aspose.words/emphasismark/
---
## EmphasisMark enumeration

Указывает возможные типы знака ударения.

```csharp
public enum EmphasisMark
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Нет знака ударения. |
| OverSolidCircle | `1` | Знак акцента — это сплошной черный кружок, отображаемый над текстом. |
| OverComma | `2` | Знак акцента — это символ запятой, отображаемый над текстом. |
| OverWhiteCircle | `3` | Знак акцента — это пустой белый кружок, отображаемый над текстом. |
| UnderSolidCircle | `4` | Знак акцента — это сплошной черный кружок, отображаемый под текстом. |

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

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)
