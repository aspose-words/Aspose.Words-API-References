---
title: DocumentBase.FootnoteSeparators
linktitle: FootnoteSeparators
articleTitle: FootnoteSeparators
second_title: Aspose.Words для .NET
description: Получайте доступ и настраивайте разделители сносок и концевых сносок в документе с помощью свойства FootnoteSeparators DocumentBase для расширенного управления форматированием.
type: docs
weight: 40
url: /ru/net/aspose.words/documentbase/footnoteseparators/
---
## DocumentBase.FootnoteSeparators property

Предоставляет доступ к разделителям сносок/концевых сносок, определенным в документе.

```csharp
public FootnoteSeparatorCollection FootnoteSeparators { get; }
```

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

* class [FootnoteSeparatorCollection](../../../aspose.words.notes/footnoteseparatorcollection/)
* class [DocumentBase](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
