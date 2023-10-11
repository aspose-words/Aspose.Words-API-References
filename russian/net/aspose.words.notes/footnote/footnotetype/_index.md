---
title: Footnote.FootnoteType
second_title: Справочник по API Aspose.Words для .NET
description: Footnote свойство. Возвращает значение указывающее является ли это сноской или концевой сноской.
type: docs
weight: 20
url: /ru/net/aspose.words.notes/footnote/footnotetype/
---
## Footnote.FootnoteType property

Возвращает значение, указывающее, является ли это сноской или концевой сноской.

```csharp
public FootnoteType FootnoteType { get; }
```

### Примеры

Показывает разницу между сносками и концевыми сносками.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены два способа прикрепления к тексту нумерованных ссылок. Обе эти ссылки добавят
// небольшой верхний индекс в том месте, где мы их вставляем.
// Знак ссылки по умолчанию представляет собой порядковый номер ссылки среди всех ссылок в документе.
// Каждая ссылка также создаст запись, которая будет иметь тот же знак ссылки, что и в основном тексте
// и ссылочный текст, который мы передадим методу компоновщика документов «InsertFootnote».
// 1 — сноска, запись которой появится на той же странице, что и текст, на который она ссылается:
builder.Write("Footnote referenced main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, 
    "Footnote text, will appear at the bottom of the page that contains the referenced text.");

// 2 - Сноска, запись которой появится в конце документа:
builder.Write("Endnote referenced main body text.");
Footnote endnote = builder.InsertFootnote(FootnoteType.Endnote, 
    "Endnote text, will appear at the very end of the document.");

builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(FootnoteType.Footnote, footnote.FootnoteType);
Assert.AreEqual(FootnoteType.Endnote, endnote.FootnoteType);

doc.Save(ArtifactsDir + "InlineStory.FootnoteEndnote.docx");
```

### Смотрите также

* enum [FootnoteType](../../footnotetype/)
* class [Footnote](../)
* пространство имен [Aspose.Words.Notes](../../footnote/)
* сборка [Aspose.Words](../../../)


