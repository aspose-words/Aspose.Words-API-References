---
title: Enum EmphasisMark
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.EmphasisMark перечисление. Указывает возможные типы знаков акцента.
type: docs
weight: 1460
url: /ru/net/aspose.words/emphasismark/
---
## EmphasisMark enumeration

Указывает возможные типы знаков акцента.

```csharp
public enum EmphasisMark
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| None | `0` | Без знака ударения. |
| OverSolidCircle | `1` | Знак выделения представляет собой сплошной черный круг, отображаемый над текстом. |
| OverComma | `2` | Знак выделения — это символ запятой, отображаемый над текстом. |
| OverWhiteCircle | `3` | Знак выделения — это пустой белый кружок, отображаемый над текстом. |
| UnderSolidCircle | `4` | Знак выделения представляет собой сплошной черный круг, отображаемый под текстом. |

### Примеры

Показывает, как добавить дополнительный символ, отображаемый выше/ниже символа-глифа.

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


