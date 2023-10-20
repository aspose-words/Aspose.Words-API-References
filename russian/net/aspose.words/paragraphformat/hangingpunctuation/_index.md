---
title: ParagraphFormat.HangingPunctuation
linktitle: HangingPunctuation
articleTitle: HangingPunctuation
second_title: Aspose.Words для .NET
description: ParagraphFormat HangingPunctuation свойство. Получает или задает флаг указывающий включена ли висячая пунктуация для текущего абзаца на С#.
type: docs
weight: 130
url: /ru/net/aspose.words/paragraphformat/hangingpunctuation/
---
## ParagraphFormat.HangingPunctuation property

Получает или задает флаг, указывающий, включена ли висячая пунктуация для текущего абзаца.

```csharp
public bool HangingPunctuation { get; set; }
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
