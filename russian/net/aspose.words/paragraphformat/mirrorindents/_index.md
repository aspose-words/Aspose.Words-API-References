---
title: ParagraphFormat.MirrorIndents
linktitle: MirrorIndents
articleTitle: MirrorIndents
second_title: Aspose.Words для .NET
description: Узнайте, как свойство ParagraphFormat MirrorIndents улучшает форматирование документа, обеспечивая единообразные отступы слева и справа для создания изысканного вида.
type: docs
weight: 240
url: /ru/net/aspose.words/paragraphformat/mirrorindents/
---
## ParagraphFormat.MirrorIndents property

Возвращает или задает флаг, указывающий, имеют ли левый и правый отступы одинаковую ширину.

```csharp
public bool MirrorIndents { get; set; }
```

## Примеры

Покажите, как сделать отступы слева и справа одинаковыми.

```csharp
Document doc = new Document(MyDir + "Document.docx");
ParagraphFormat format = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat;

format.MirrorIndents = true;

doc.Save(ArtifactsDir + "ParagraphFormat.MirrorIndents.docx");
```

### Смотрите также

* class [ParagraphFormat](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
