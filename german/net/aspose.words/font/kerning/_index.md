---
title: Font.Kerning
linktitle: Kerning
articleTitle: Kerning
second_title: Aspose.Words für .NET
description: Entdecken Sie die Funktion „Schriftunterschneidung“ und steuern Sie den Beginn der Unterschneidung für optimale Textklarheit und Design. Verbessern Sie Ihre Typografie mit Präzision!
type: docs
weight: 180
url: /de/net/aspose.words/font/kerning/
---
## Font.Kerning property

Ruft die Schriftgröße ab, bei der die Unterschneidung beginnt, oder legt diese fest.

```csharp
public double Kerning { get; set; }
```

## Beispiele

Zeigt, wie Sie die Schriftgröße angeben, ab der die Unterschneidung wirksam wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial Black";

// Legen Sie die Schriftgröße des Builders und die Mindestgröße fest, ab der das Kerning wirksam wird.
// Die Schriftgröße liegt unter dem Kerning-Schwellenwert, daher wird der Lauf unten nicht unterschnitten.
builder.Font.Size = 18;
builder.Font.Kerning = 24;

builder.Writeln("TALLY. (Kerning not applied)");

// Legen Sie den Kerning-Schwellenwert so fest, dass die aktuelle Schriftgröße des Builders darüber liegt.
// Jeder Text, den wir ab diesem Punkt hinzufügen, wird mit Kerning versehen. Die Abstände zwischen den Zeichen
// wird angepasst, was normalerweise zu einem etwas ästhetischeren Textverlauf führt.
builder.Font.Kerning = 12;

builder.Writeln("TALLY. (Kerning applied)");

doc.Save(ArtifactsDir + "Font.Kerning.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
