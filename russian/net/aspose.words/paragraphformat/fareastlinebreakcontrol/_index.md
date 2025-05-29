---
title: ParagraphFormat.FarEastLineBreakControl
linktitle: FarEastLineBreakControl
articleTitle: FarEastLineBreakControl
second_title: Aspose.Words для .NET
description: Откройте для себя свойство ParagraphFormat FarEastLineBreakControl, включающее правила переноса строк для восточноазиатских языков для точного форматирования текста в ваших документах.
type: docs
weight: 110
url: /ru/net/aspose.words/paragraphformat/fareastlinebreakcontrol/
---
## ParagraphFormat.FarEastLineBreakControl property

Возвращает или задает флаг, указывающий, применяются ли к текущему абзацу правила переноса строк в восточноазиатских языках.

```csharp
public bool FarEastLineBreakControl { get; set; }
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
