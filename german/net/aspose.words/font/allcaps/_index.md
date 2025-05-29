---
title: Font.AllCaps
linktitle: AllCaps
articleTitle: AllCaps
second_title: Aspose.Words für .NET
description: Entdecken Sie die Font AllCaps-Funktion. Formatieren Sie Text ganz einfach in Großbuchstaben für bessere Lesbarkeit und ein wirkungsvolles Design Ihrer Projekte.
type: docs
weight: 10
url: /de/net/aspose.words/font/allcaps/
---
## Font.AllCaps property

Wahr, wenn die Schriftart ausschließlich in Großbuchstaben formatiert ist.

```csharp
public bool AllCaps { get; set; }
```

## Beispiele

Zeigt, wie ein Lauf formatiert wird, um seinen Inhalt in Großbuchstaben anzuzeigen.

```csharp
Document doc = new Document();
Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);

// Es gibt zwei Möglichkeiten, einen Lauf dazu zu bringen, seinen Kleinbuchstabentext in Großbuchstaben anzuzeigen, ohne den Inhalt zu ändern.
// 1 – Setzen Sie das AllCaps-Flag, um alle Zeichen in Großbuchstaben anzuzeigen:
Run run = new Run(doc, "all capitals");
run.Font.AllCaps = true;
para.AppendChild(run);

para = (Paragraph)para.ParentNode.AppendChild(new Paragraph(doc));

// 2 - Setzen Sie das SmallCaps-Flag, um alle Zeichen in Kapitälchen anzuzeigen:
// Wenn ein Zeichen klein geschrieben ist, wird es in Großbuchstaben angezeigt
// hat aber die gleiche Höhe wie die Kleinbuchstaben (die x-Höhe der Schriftart).
// Zeichen, die ursprünglich in Großbuchstaben geschrieben waren, sehen gleich aus.
run = new Run(doc, "Small Capitals");
run.Font.SmallCaps = true;
para.AppendChild(run);

doc.Save(ArtifactsDir + "Font.Caps.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
