---
title: Footnote.FootnoteType
linktitle: FootnoteType
articleTitle: FootnoteType
second_title: Aspose.Words для .NET
description: Откройте для себя свойство FootnoteType, с легкостью идентифицируйте сноски или концевые сноски в документах для большей ясности и организации.
type: docs
weight: 30
url: /ru/net/aspose.words.notes/footnote/footnotetype/
---
## Footnote.FootnoteType property

Возвращает значение, указывающее, является ли это сноской или концевой сноской.

```csharp
public FootnoteType FootnoteType { get; }
```

## Примеры

Показывает разницу между обычными и концевыми сносками.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Ниже приведены два способа присоединения нумерованных ссылок к тексту. Обе эти ссылки добавят
// небольшой верхний индексный знак в том месте, куда мы их вставляем.
// Знак ссылки по умолчанию — это порядковый номер ссылки среди всех ссылок в документе.
// Каждая ссылка также создаст запись, которая будет иметь тот же ссылочный знак, что и в основном тексте
// и справочный текст, который мы передадим в метод "InsertFootnote" конструктора документа.
// 1 — Сноска, запись которой будет отображаться на той же странице, что и текст, на который она ссылается:
builder.Write("Footnote referenced main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, 
    "Footnote text, will appear at the bottom of the page that contains the referenced text.");

// 2 — Концевая сноска, запись которой появится в конце документа:
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
* пространство имен [Aspose.Words.Notes](../../../aspose.words.notes/)
* сборка [Aspose.Words](../../../)
