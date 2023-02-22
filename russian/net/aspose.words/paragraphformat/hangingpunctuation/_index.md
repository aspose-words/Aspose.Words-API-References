---
title: ParagraphFormat.HangingPunctuation
second_title: Справочник по API Aspose.Words для .NET
description: ParagraphFormat свойство. Получает или устанавливает флаг указывающий включена ли для текущего абзаца висячая пунктуация.
type: docs
weight: 120
url: /ru/net/aspose.words/paragraphformat/hangingpunctuation/
---
## ParagraphFormat.HangingPunctuation property

Получает или устанавливает флаг, указывающий, включена ли для текущего абзаца висячая пунктуация.

```csharp
public bool HangingPunctuation { get; set; }
```

### Примеры

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
* пространство имен [Aspose.Words](../../paragraphformat/)
* сборка [Aspose.Words](../../../)


