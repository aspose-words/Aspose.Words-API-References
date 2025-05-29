---
title: FindReplaceOptions.IgnoreFootnotes
linktitle: IgnoreFootnotes
articleTitle: IgnoreFootnotes
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FindReplaceOptions IgnoreFootnotes, чтобы легко управлять сносками в документах. Повысьте эффективность редактирования с помощью этого простого переключателя!
type: docs
weight: 90
url: /ru/net/aspose.words.replacing/findreplaceoptions/ignorefootnotes/
---
## FindReplaceOptions.IgnoreFootnotes property

Возвращает или задает логическое значение, указывающее, следует ли игнорировать сноски. Значение по умолчанию:`ЛОЖЬ` .

```csharp
public bool IgnoreFootnotes { get; set; }
```

## Примеры

Показывает, как игнорировать сноски во время операции поиска и замены.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertFootnote(FootnoteType.Footnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder.InsertParagraph();

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertFootnote(FootnoteType.Endnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

// Установите флаг "IgnoreFootnotes" на "true", чтобы получить функцию поиска и замены
// операция игнорирования текста внутри сносок.
// Установите флаг "IgnoreFootnotes" на "false", чтобы получить функцию поиска и замены
// операция также для поиска текста внутри сносок.
FindReplaceOptions options = new FindReplaceOptions { IgnoreFootnotes = isIgnoreFootnotes };
doc.Range.Replace("Lorem ipsum", "Replaced Lorem ipsum", options);
```

### Смотрите также

* class [FindReplaceOptions](../)
* пространство имен [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* сборка [Aspose.Words](../../../)
