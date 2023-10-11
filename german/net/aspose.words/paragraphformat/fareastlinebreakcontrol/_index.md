---
title: ParagraphFormat.FarEastLineBreakControl
second_title: Aspose.Words für .NET-API-Referenz
description: ParagraphFormat eigendom. Ruft ein Flag ab oder legt es fest das angibt ob ostasiatische Zeilenumbruchregeln auf den aktuellen Absatz angewendet werden.
type: docs
weight: 110
url: /de/net/aspose.words/paragraphformat/fareastlinebreakcontrol/
---
## ParagraphFormat.FarEastLineBreakControl property

Ruft ein Flag ab oder legt es fest, das angibt, ob ostasiatische Zeilenumbruchregeln auf den aktuellen Absatz angewendet werden.

```csharp
public bool FarEastLineBreakControl { get; set; }
```

### Beispiele

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
* namensraum [Aspose.Words](../../paragraphformat/)
* Montage [Aspose.Words](../../../)


