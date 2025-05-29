---
title: Font.StrikeThrough
linktitle: StrikeThrough
articleTitle: StrikeThrough
second_title: Aspose.Words für .NET
description: Entdecken Sie die Schrift-Durchstreichungseigenschaft. Formatieren Sie Text einfach durchgestrichen für klare visuelle Hervorhebung in Ihren Designs. Verbessern Sie noch heute die Lesbarkeit!
type: docs
weight: 400
url: /de/net/aspose.words/font/strikethrough/
---
## Font.StrikeThrough property

Wahr, wenn die Schriftart als durchgestrichener Text formatiert ist.

```csharp
public bool StrikeThrough { get; set; }
```

## Beispiele

Zeigt, wie Sie einem Text eine durchgestrichene Zeile hinzufügen.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

Run run = new Run(doc, "Text with a single-line strikethrough.");
run.Font.StrikeThrough = true;
para.AppendChild(run);

para = (Paragraph)para.ParentNode.AppendChild(new Paragraph(doc));

run = new Run(doc, "Text with a double-line strikethrough.");
run.Font.DoubleStrikeThrough = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.StrikeThrough.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
