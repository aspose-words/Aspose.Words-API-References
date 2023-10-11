---
title: ParagraphFormat.HangingPunctuation
second_title: Справочник по API Aspose.Words для .NET
description: ParagraphFormat свойство. Получает или задает флаг указывающий включена ли висячая пунктуация для текущего абзаца.
type: docs
weight: 130
url: /ru/net/aspose.words/paragraphformat/hangingpunctuation/
---
## ParagraphFormat.HangingPunctuation property

Получает или задает флаг, указывающий, включена ли висячая пунктуация для текущего абзаца.

```csharp
public bool HangingPunctuation { get; set; }
```

### Примеры

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
* пространство имен [Aspose.Words](../../paragraphformat/)
* сборка [Aspose.Words](../../../)


