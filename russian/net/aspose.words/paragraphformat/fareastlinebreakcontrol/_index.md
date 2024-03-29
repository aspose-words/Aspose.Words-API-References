---
title: ParagraphFormat.FarEastLineBreakControl
linktitle: FarEastLineBreakControl
articleTitle: FarEastLineBreakControl
second_title: Aspose.Words для .NET
description: ParagraphFormat FarEastLineBreakControl свойство. Получает или задает флаг указывающий применяются ли восточноазиатские правила разрыва строк к текущему абзацу на С#.
type: docs
weight: 110
url: /ru/net/aspose.words/paragraphformat/fareastlinebreakcontrol/
---
## ParagraphFormat.FarEastLineBreakControl property

Получает или задает флаг, указывающий, применяются ли восточноазиатские правила разрыва строк к текущему абзацу.

```csharp
public bool FarEastLineBreakControl { get; set; }
```

## Примеры

Показывает, как установить специальные свойства для азиатской типографики.

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
