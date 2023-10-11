---
title: Font.TextEffect
second_title: Aspose.Words für .NET-API-Referenz
description: Font eigendom. Ruft den Schriftartanimationseffekt ab oder legt ihn fest.
type: docs
weight: 450
url: /de/net/aspose.words/font/texteffect/
---
## Font.TextEffect property

Ruft den Schriftartanimationseffekt ab oder legt ihn fest.

```csharp
public TextEffect TextEffect { get; set; }
```

### Beispiele

Zeigt, wie man einen visuellen Effekt auf einen Lauf anwendet.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.TextEffect = TextEffect.SparkleText;

builder.Writeln("Text with a sparkle effect.");

// Ältere Versionen von Microsoft Word unterstützen nur Schriftartanimationseffekte.
doc.Save(ArtifactsDir + "Font.SparklingText.doc");
```

### Siehe auch

* enum [TextEffect](../../texteffect/)
* class [Font](../)
* namensraum [Aspose.Words](../../font/)
* Montage [Aspose.Words](../../../)


