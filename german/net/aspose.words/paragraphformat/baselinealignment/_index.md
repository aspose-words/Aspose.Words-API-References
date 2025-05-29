---
title: ParagraphFormat.BaselineAlignment
linktitle: BaselineAlignment
articleTitle: BaselineAlignment
second_title: Aspose.Words für .NET
description: Optimieren Sie Ihr Textlayout mit der Eigenschaft „ParagraphFormat BaselineAlignment“, die eine präzise Kontrolle über die vertikale Positionierung der Schriftart für eine verbesserte Lesbarkeit ermöglicht.
type: docs
weight: 40
url: /de/net/aspose.words/paragraphformat/baselinealignment/
---
## ParagraphFormat.BaselineAlignment property

Ruft die vertikale Position der Schriftart in einer Zeile ab oder legt sie fest.

```csharp
public BaselineAlignment BaselineAlignment { get; set; }
```

## Beispiele

Zeigt, wie die vertikale Position von Schriftarten auf einer Zeile festgelegt wird.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

ParagraphFormat format = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat;
if (format.BaselineAlignment == BaselineAlignment.Auto)
{                
    format.BaselineAlignment = BaselineAlignment.Top;
}

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphBaselineAlignment.docx");
```

### Siehe auch

* enum [BaselineAlignment](../../baselinealignment/)
* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
