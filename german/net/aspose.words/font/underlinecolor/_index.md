---
title: Font.UnderlineColor
linktitle: UnderlineColor
articleTitle: UnderlineColor
second_title: Aspose.Words für .NET
description: Entdecken Sie die Font UnderlineColor-Eigenschaft, um die Unterstreichungsfarbe Ihrer Schriftart einfach anzupassen und so den Textstil und die visuelle Attraktivität zu verbessern.
type: docs
weight: 550
url: /de/net/aspose.words/font/underlinecolor/
---
## Font.UnderlineColor property

Ruft die Farbe der Unterstreichung der Schriftart ab oder legt sie fest.

```csharp
public Color UnderlineColor { get; set; }
```

## Beispiele

Zeigt, wie Sie Stil und Farbe einer Textunterstreichung konfigurieren.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Underline = Underline.Dotted;
builder.Font.UnderlineColor = Color.Red;

builder.Writeln("Underlined text.");

doc.Save(ArtifactsDir + "Font.Underlines.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
