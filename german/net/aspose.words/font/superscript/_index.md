---
title: Font.Superscript
linktitle: Superscript
articleTitle: Superscript
second_title: Aspose.Words für .NET
description: Font Superscript eigendom. True wenn die Schriftart hochgestellt formatiert ist in C#.
type: docs
weight: 440
url: /de/net/aspose.words/font/superscript/
---
## Font.Superscript property

True, wenn die Schriftart hochgestellt formatiert ist.

```csharp
public bool Superscript { get; set; }
```

## Beispiele

Zeigt, wie Text formatiert wird, um seine Position zu versetzen.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Diese Textzeile um 5 Punkte über die Grundlinie anheben.
Run run = new Run(doc, "Raised text. ");
run.Font.Position = 5;
para.AppendChild(run);

// Diese Textzeile um 10 Punkte unter die Grundlinie senken.
run = new Run(doc, "Lowered text. ");
run.Font.Position = -10;
para.AppendChild(run);

// Einen Lauf mit normalem Text hinzufügen.
run = new Run(doc, "Text in its default position. ");
para.AppendChild(run);

// Fügen Sie eine Textzeile hinzu, die als Index angezeigt wird.
run = new Run(doc, "Subscript. ");
run.Font.Subscript = true;
para.AppendChild(run);

// Fügen Sie eine Textzeile hinzu, die hochgestellt angezeigt wird.
run = new Run(doc, "Superscript.");
run.Font.Superscript = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.PositionSubscript.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
