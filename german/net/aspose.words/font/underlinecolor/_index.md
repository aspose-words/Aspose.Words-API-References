---
title: Font.UnderlineColor
second_title: Aspose.Words für .NET-API-Referenz
description: Font eigendom. Ruft die Farbe der auf die Schriftart angewendeten Unterstreichung ab oder legt diese fest.
type: docs
weight: 540
url: /de/net/aspose.words/font/underlinecolor/
---
## Font.UnderlineColor property

Ruft die Farbe der auf die Schriftart angewendeten Unterstreichung ab oder legt diese fest.

```csharp
public Color UnderlineColor { get; set; }
```

### Beispiele

Zeigt, wie Sie den Stil und die Farbe einer Textunterstreichung konfigurieren.

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
* namensraum [Aspose.Words](../../font/)
* Montage [Aspose.Words](../../../)


