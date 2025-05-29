---
title: FootnoteSeparatorType Enum
linktitle: FootnoteSeparatorType
articleTitle: FootnoteSeparatorType
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.FootnoteSeparatorType для настройки разделителей сносок и концевых сносок, что улучшает форматирование и читабельность документа.
type: docs
weight: 5010
url: /ru/net/aspose.words.notes/footnoteseparatortype/
---
## FootnoteSeparatorType enumeration

Указывает тип разделителя сносок/концевых сносок.

```csharp
public enum FootnoteSeparatorType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| FootnoteSeparator | `0` | Разделитель между основным текстом и текстом сноски. |
| FootnoteContinuationSeparator | `1` | Печатается над текстом сноски на странице, когда текст должен быть продолжен с предыдущей страницы. |
| FootnoteContinuationNotice | `2` | Печатается под текстом сноски на странице, когда текст сноски должен быть продолжен на следующей странице. |
| EndnoteSeparator | `3` | Разделитель между основным текстом и текстом концевой сноски. |
| EndnoteContinuationSeparator | `4` | Печатается над текстом концевой сноски на странице, когда текст должен быть продолжен с предыдущей страницы. |
| EndnoteContinuationNotice | `5` | Печатается под текстом концевой сноски на странице, когда текст концевой сноски должен быть продолжен на следующей странице. |

## Примеры

Показывает, как удалить разделитель концевых сносок.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator endnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.EndnoteSeparator];
// Удалить разделитель концевой сноски.
endnoteSeparator.FirstParagraph.FirstChild.Remove();
```

Показывает, как управлять форматом разделителя сносок.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
// Выровнять разделитель сносок.
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### Смотрите также

* пространство имен [Aspose.Words.Notes](../../aspose.words.notes/)
* сборка [Aspose.Words](../../)
