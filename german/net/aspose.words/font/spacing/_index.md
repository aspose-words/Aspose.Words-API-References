---
title: Font.Spacing
second_title: Aspose.Words für .NET-API-Referenz
description: Font eigendom. Gibt den Abstand in Punkt zwischen Zeichen zurück oder legt diesen fest.
type: docs
weight: 380
url: /de/net/aspose.words/font/spacing/
---
## Font.Spacing property

Gibt den Abstand (in Punkt) zwischen Zeichen zurück oder legt diesen fest.

```csharp
public double Spacing { get; set; }
```

### Beispiele

Zeigt, wie die horizontale Skalierung und der Abstand für Zeichen festgelegt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Text hinzufügen und Zeichenbreite auf 150 % erhöhen.
builder.Font.Scaling = 150;
builder.Writeln("Wide characters");

// Textlauf hinzufügen und 1 Punkt zusätzlichen horizontalen Abstand zwischen jedem Zeichen hinzufügen.
builder.Font.Spacing = 1;
builder.Writeln("Expanded by 1pt");

// Text hinzufügen und Zeichen um 1 Punkt näher zusammenbringen.
builder.Font.Spacing = -1;
builder.Writeln("Condensed by 1pt");

doc.Save(ArtifactsDir + "Font.ScalingSpacing.docx");
```

### Siehe auch

* class [Font](../)
* namensraum [Aspose.Words](../../font/)
* Montage [Aspose.Words](../../../)


