---
title: Document.IncludeTextboxesFootnotesEndnotesInStat
linktitle: IncludeTextboxesFootnotesEndnotesInStat
articleTitle: IncludeTextboxesFootnotesEndnotesInStat
second_title: Aspose.Words для .NET
description: Оптимизируйте количество слов в документе с помощью свойства IncludeTextboxesFootnotesEndnotesInStat. Управляйте текстовыми полями, сносками и концевыми сносками без усилий!
type: docs
weight: 230
url: /ru/net/aspose.words/document/includetextboxesfootnotesendnotesinstat/
---
## Document.IncludeTextboxesFootnotesEndnotesInStat property

Указывает, следует ли включать текстовые поля, сноски и концевые сноски в статистику количества слов.

```csharp
public bool IncludeTextboxesFootnotesEndnotesInStat { get; set; }
```

## Примеры

Показывает, как включать или исключать текстовые поля, сноски и концевые сноски из статистики количества слов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Lorem ipsum");
builder.InsertFootnote(FootnoteType.Footnote, "sit amet");

// По умолчанию параметр имеет значение «false».
doc.UpdateWordCount();
// Количество слов подсчитывается без учета текстовых полей, сносок и концевых сносок.
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Words);

doc.IncludeTextboxesFootnotesEndnotesInStat = true;
doc.UpdateWordCount();
// Количество слов подсчитывается с помощью текстовых полей, сносок и концевых сносок.
Assert.AreEqual(4, doc.BuiltInDocumentProperties.Words);
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
