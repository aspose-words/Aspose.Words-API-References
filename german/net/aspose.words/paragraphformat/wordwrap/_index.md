---
title: ParagraphFormat.WordWrap
linktitle: WordWrap
articleTitle: WordWrap
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Eigenschaft „ParagraphFormat WordWrap“ den Textumbruch in Word beeinflusst. Lernen Sie, den lateinischen Textfluss zu steuern, um die Lesbarkeit Ihres Dokuments zu verbessern.
type: docs
weight: 420
url: /de/net/aspose.words/paragraphformat/wordwrap/
---
## ParagraphFormat.WordWrap property

Wenn diese Eigenschaft`FALSCH` , lateinischer Text in der Mitte eines Wortes kann für den aktuellen Absatz umgebrochen werden. Andernfalls wird lateinischer Text um ganze Wörter umgebrochen.

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
