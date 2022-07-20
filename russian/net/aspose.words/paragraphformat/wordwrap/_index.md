---
title: WordWrap
second_title: Справочник по API Aspose.Words для .NET
description: Если это свойство ЛОЖЬ латинский текст в середине слова можно переносить на текущего абзаца. В противном случае латинский текст переносится целыми словами.
type: docs
weight: 400
url: /ru/net/aspose.words/paragraphformat/wordwrap/
---
## ParagraphFormat.WordWrap property

Если это свойство **ЛОЖЬ** латинский текст в середине слова можно переносить на текущего абзаца. В противном случае латинский текст переносится целыми словами.

```csharp
public bool WordWrap { get; set; }
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

* class [ParagraphFormat](../../paragraphformat)
* пространство имен [Aspose.Words](../../paragraphformat)
* сборка [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->