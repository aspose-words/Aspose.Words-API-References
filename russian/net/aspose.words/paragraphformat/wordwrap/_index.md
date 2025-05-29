---
title: ParagraphFormat.WordWrap
linktitle: WordWrap
articleTitle: WordWrap
second_title: Aspose.Words для .NET
description: Узнайте, как свойство ParagraphFormat WordWrap влияет на перенос текста в Word. Узнайте, как управлять потоком латинского текста для улучшения читаемости документа.
type: docs
weight: 420
url: /ru/net/aspose.words/paragraphformat/wordwrap/
---
## ParagraphFormat.WordWrap property

Если это свойство`ЛОЖЬ` , Латинский текст в середине слова может быть перенесен на текущий абзац. В противном случае латинский текст переносится на целые слова.

```csharp
public bool WordWrap { get; set; }
```

## Примеры

Показывает, как задать специальные свойства для азиатской типографики.

```csharp
Document doc = new Document(MyDir + "Document.docx");

ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;
format.FarEastLineBreakControl = true;
format.WordWrap = false;
format.HangingPunctuation = true;

doc.Save(ArtifactsDir + "ParagraphFormat.AsianTypographyProperties.docx");
```

### Смотрите также

* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
