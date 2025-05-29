---
title: Font.DoubleStrikeThrough
linktitle: DoubleStrikeThrough
articleTitle: DoubleStrikeThrough
second_title: Aspose.Words für .NET
description: Entdecken Sie die Font-Eigenschaft DoubleStrikeThrough. Formatieren Sie Text einfach mit doppeltem Durchstreichen für mehr Klarheit und Stil in Ihren Dokumenten.
type: docs
weight: 90
url: /de/net/aspose.words/font/doublestrikethrough/
---
## Font.DoubleStrikeThrough property

Wahr, wenn die Schriftart als doppelt durchgestrichener Text formatiert ist.

```csharp
public bool DoubleStrikeThrough { get; set; }
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
