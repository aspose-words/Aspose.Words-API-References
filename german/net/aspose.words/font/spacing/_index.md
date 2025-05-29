---
title: Font.Spacing
linktitle: Spacing
articleTitle: Spacing
second_title: Aspose.Words für .NET
description: Entdecken Sie die Schriftabstand-Eigenschaft, um den Zeichenabstand in Punkten einfach anzupassen. Verbessern Sie Lesbarkeit und Design mit präziser typografischer Kontrolle.
type: docs
weight: 390
url: /de/net/aspose.words/font/spacing/
---
## Font.Spacing property

Gibt den Abstand (in Punkten) zwischen Zeichen zurück oder legt ihn fest.

```csharp
public double Spacing { get; set; }
```

## Beispiele

Zeigt, wie die horizontale Skalierung und der Abstand für Zeichen festgelegt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Textlauf hinzufügen und Zeichenbreite auf 150 % erhöhen.
builder.Font.Scaling = 150;
builder.Writeln("Wide characters");

// Textlauf hinzufügen und 1pt zusätzlichen horizontalen Abstand zwischen den einzelnen Zeichen hinzufügen.
builder.Font.Spacing = 1;
builder.Writeln("Expanded by 1pt");

// Textlauf hinzufügen und Zeichen um 1pt näher zusammenbringen.
builder.Font.Spacing = -1;
builder.Writeln("Condensed by 1pt");

doc.Save(ArtifactsDir + "Font.ScalingSpacing.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
