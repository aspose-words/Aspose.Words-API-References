---
title: PageSetup.EndnoteOptions
linktitle: EndnoteOptions
articleTitle: EndnoteOptions
second_title: Aspose.Words для .NET
description: Откройте для себя свойство PageSetup EndnoteOptions, позволяющее легко настраивать нумерацию и расположение концевых сносок для улучшенного форматирования и ясности документа.
type: docs
weight: 120
url: /ru/net/aspose.words/pagesetup/endnoteoptions/
---
## PageSetup.EndnoteOptions property

Предоставляет параметры, управляющие нумерацией и расположением концевых сносок в этом разделе.

```csharp
public EndnoteOptions EndnoteOptions { get; }
```

## Примеры

Показывает, как настроить параметры, влияющие на сноски/концевые сноски в разделе.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote reference text.");

// Настройте все сноски в первом разделе, чтобы начать нумерацию заново с 1
// на каждой новой странице и отображаются непосредственно под текстом на каждой странице.
FootnoteOptions footnoteOptions = doc.Sections[0].PageSetup.FootnoteOptions;
footnoteOptions.Position = FootnotePosition.BeneathText;
footnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
footnoteOptions.StartNumber = 1;

builder.Write(" Hello again.");
builder.InsertFootnote(FootnoteType.Footnote, "Endnote reference text.");

// Настройте все концевые сноски в первом разделе, чтобы поддерживать непрерывный подсчет по всему разделу,
// начиная с 1. Также установите, чтобы все они отображались собранными в конце документа.
EndnoteOptions endnoteOptions = doc.Sections[0].PageSetup.EndnoteOptions;
endnoteOptions.Position = EndnotePosition.EndOfDocument;
endnoteOptions.RestartRule = FootnoteNumberingRule.Continuous;
endnoteOptions.StartNumber = 1;

doc.Save(ArtifactsDir + "PageSetup.FootnoteOptions.docx");
```

### Смотрите также

* class [EndnoteOptions](../../../aspose.words.notes/endnoteoptions/)
* class [PageSetup](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
