---
title: Font.Scaling
second_title: Aspose.Words für .NET-API-Referenz
description: Font eigendom. Ruft die Skalierung der Zeichenbreite in Prozent ab oder legt diese fest.
type: docs
weight: 310
url: /de/net/aspose.words/font/scaling/
---
## Font.Scaling property

Ruft die Skalierung der Zeichenbreite in Prozent ab oder legt diese fest.

```csharp
public int Scaling { get; set; }
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


