---
title: ParagraphFormat.HangingPunctuation
linktitle: HangingPunctuation
articleTitle: HangingPunctuation
second_title: Aspose.Words для .NET
description: Узнайте, как улучшить макет текста с помощью свойства «Висячая пунктуация» в ParagraphFormat. Оптимизируйте читаемость и стиль без усилий!
type: docs
weight: 130
url: /ru/net/aspose.words/paragraphformat/hangingpunctuation/
---
## ParagraphFormat.HangingPunctuation property

Возвращает или задает флаг, указывающий, включена ли висячая пунктуация для текущего абзаца.

```csharp
public bool HangingPunctuation { get; set; }
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
