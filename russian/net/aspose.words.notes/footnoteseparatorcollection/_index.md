---
title: FootnoteSeparatorCollection Class
linktitle: FootnoteSeparatorCollection
articleTitle: FootnoteSeparatorCollection
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.Notes.FootnoteSeparatorCollection для легкого доступа к разделителям сносок в ваших документах. Улучшите форматирование ваших документов сегодня!
type: docs
weight: 5000
url: /ru/net/aspose.words.notes/footnoteseparatorcollection/
---
## FootnoteSeparatorCollection class

Предоставляет типизированный доступ к[`FootnoteSeparator`](../footnoteseparator/) узлы документа.

```csharp
public class FootnoteSeparatorCollection : IEnumerable<FootnoteSeparator>
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FootnoteSeparatorCollection](footnoteseparatorcollection/)() | Конструктор по умолчанию. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [Item](../../aspose.words.notes/footnoteseparatorcollection/item/) { get; } | Извлекает[`FootnoteSeparator`](../footnoteseparator/) указанного типа. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetEnumerator](../../aspose.words.notes/footnoteseparatorcollection/getenumerator/)() |  |

## Примеры

Показывает, как управлять форматом разделителя сносок.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

FootnoteSeparator footnoteSeparator = doc.FootnoteSeparators[FootnoteSeparatorType.FootnoteSeparator];
// Выровнять разделитель сносок.
footnoteSeparator.FirstParagraph.ParagraphFormat.Alignment = ParagraphAlignment.Center;
```

### Смотрите также

* class [FootnoteSeparator](../footnoteseparator/)
* пространство имен [Aspose.Words.Notes](../../aspose.words.notes/)
* сборка [Aspose.Words](../../)
