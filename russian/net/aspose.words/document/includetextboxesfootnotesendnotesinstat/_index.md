---
title: Document.IncludeTextboxesFootnotesEndnotesInStat
second_title: Справочник по API Aspose.Words для .NET
description: Document свойство. Указывает включать ли текстовые поля сноски и концевые сноски в статистику количества слов.
type: docs
weight: 220
url: /ru/net/aspose.words/document/includetextboxesfootnotesendnotesinstat/
---
## Document.IncludeTextboxesFootnotesEndnotesInStat property

Указывает, включать ли текстовые поля, сноски и концевые сноски в статистику количества слов.

```csharp
public bool IncludeTextboxesFootnotesEndnotesInStat { get; set; }
```

### Примеры

Показывает, как включить или исключить текстовые поля, сноски и концевые сноски из статистики количества слов.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Lorem ipsum");
builder.InsertFootnote(FootnoteType.Footnote, "sit amet");

// По умолчанию для параметра установлено значение «false».
doc.UpdateWordCount();
// Количество слов без текстовых полей, сносок и концевых сносок.
Assert.AreEqual(2, doc.BuiltInDocumentProperties.Words);            

doc.IncludeTextboxesFootnotesEndnotesInStat = true;
doc.UpdateWordCount();
// Количество слов в текстовых полях, сносках и концевых сносках.
Assert.AreEqual(4, doc.BuiltInDocumentProperties.Words);
```

### Смотрите также

* class [Document](../)
* пространство имен [Aspose.Words](../../document/)
* сборка [Aspose.Words](../../../)


