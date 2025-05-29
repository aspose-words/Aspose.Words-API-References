---
title: Font.Subscript
linktitle: Subscript
articleTitle: Subscript
second_title: Aspose.Words für .NET
description: Entdecken Sie die Font-Tiefstellungseigenschaft. Formatieren Sie Text einfach als Tiefstellung für verbesserte Lesbarkeit und Stil in Ihren Dokumenten. Verbessern Sie Ihr Design noch heute!
type: docs
weight: 440
url: /de/net/aspose.words/font/subscript/
---
## Font.Subscript property

Wahr, wenn die Schriftart als tiefgestellt formatiert ist.

```csharp
public bool Subscript { get; set; }
```

## Beispiele

Zeigt, wie Text formatiert wird, um seine Position zu verschieben.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Heben Sie diesen Textlauf 5 Punkte über die Grundlinie.
Run run = new Run(doc, "Raised text. ");
run.Font.Position = 5;
para.AppendChild(run);

// Senken Sie diesen Textlauf 10 Punkte unter die Grundlinie.
run = new Run(doc, "Lowered text. ");
run.Font.Position = -10;
para.AppendChild(run);

// Fügen Sie einen normalen Textabschnitt hinzu.
run = new Run(doc, "Text in its default position. ");
para.AppendChild(run);

// Fügen Sie einen Textlauf hinzu, der als tiefgestellter Index angezeigt wird.
run = new Run(doc, "Subscript. ");
run.Font.Subscript = true;
para.AppendChild(run);

// Fügen Sie einen Textlauf hinzu, der als hochgestellte Zahl angezeigt wird.
run = new Run(doc, "Superscript.");
run.Font.Superscript = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.PositionSubscript.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
