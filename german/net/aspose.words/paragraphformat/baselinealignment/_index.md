---
title: ParagraphFormat.BaselineAlignment
linktitle: BaselineAlignment
articleTitle: BaselineAlignment
second_title: Aspose.Words für .NET
description: ParagraphFormat BaselineAlignment eigendom. Ruft die vertikale Position von Schriftarten in einer Zeile ab oder legt diese fest in C#.
type: docs
weight: 40
url: /de/net/aspose.words/paragraphformat/baselinealignment/
---
## ParagraphFormat.BaselineAlignment property

Ruft die vertikale Position von Schriftarten in einer Zeile ab oder legt diese fest.

```csharp
public BaselineAlignment BaselineAlignment { get; set; }
```

## Beispiele

Zeigt, wie die vertikale Position von Schriftarten in einer Zeile festgelegt wird.

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
