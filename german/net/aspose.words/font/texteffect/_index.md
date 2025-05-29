---
title: Font.TextEffect
linktitle: TextEffect
articleTitle: TextEffect
second_title: Aspose.Words für .NET
description: Entdecken Sie die Font TextEffect-Eigenschaft, um Schriftanimationen einfach anzupassen und Ihre Designs mit dynamischen Texteffekten für ein fesselndes Benutzererlebnis zu verbessern.
type: docs
weight: 460
url: /de/net/aspose.words/font/texteffect/
---
## Font.TextEffect property

Ruft den Schriftanimationseffekt ab oder legt ihn fest.

```csharp
public TextEffect TextEffect { get; set; }
```

## Beispiele

Zeigt, wie man einem Lauf einen visuellen Effekt zuweist.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.TextEffect = TextEffect.SparkleText;

builder.Writeln("Text with a sparkle effect.");

// Ältere Versionen von Microsoft Word unterstützen nur Schriftanimationseffekte.
doc.Save(ArtifactsDir + "Font.SparklingText.doc");
```

### Siehe auch

* enum [TextEffect](../../texteffect/)
* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
