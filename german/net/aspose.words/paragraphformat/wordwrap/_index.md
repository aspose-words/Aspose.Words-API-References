---
title: ParagraphFormat.WordWrap
linktitle: WordWrap
articleTitle: WordWrap
second_title: Aspose.Words für .NET
description: ParagraphFormat WordWrap eigendom. Wenn diese Eigenschaft istFALSCH  lateinischer Text in der Mitte eines Wortes kann für den aktuellen Absatz umbrochen werden. Andernfalls wird lateinischer Text durch ganze Wörter umbrochen in C#.
type: docs
weight: 410
url: /de/net/aspose.words/paragraphformat/wordwrap/
---
## ParagraphFormat.WordWrap property

Wenn diese Eigenschaft ist`FALSCH` , lateinischer Text in der Mitte eines Wortes kann für den aktuellen Absatz umbrochen werden. Andernfalls wird lateinischer Text durch ganze Wörter umbrochen.

```csharp
public bool WordWrap { get; set; }
```

## Beispiele

Zeigt, wie spezielle Eigenschaften für asiatische Typografie festgelegt werden.

```csharp
Document doc = new Document(MyDir + "Document.docx");

ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;
format.FarEastLineBreakControl = true;
format.WordWrap = false;
format.HangingPunctuation = true;

doc.Save(ArtifactsDir + "ParagraphFormat.AsianTypographyProperties.docx");
```

### Siehe auch

* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
