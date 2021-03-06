---
title: Scaling
second_title: Aspose.Words für .NET-API-Referenz
description: Ermittelt oder setzt die Skalierung der Zeichenbreite in Prozent.
type: docs
weight: 310
url: /de/net/aspose.words/font/scaling/
---
## Font.Scaling property

Ermittelt oder setzt die Skalierung der Zeichenbreite in Prozent.

```csharp
public int Scaling { get; set; }
```

### Beispiele

Zeigt, wie Sie die horizontale Skalierung und den Abstand für Zeichen festlegen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Textverlauf hinzufügen und Zeichenbreite auf 150 % erhöhen.
builder.Font.Scaling = 150;
builder.Writeln("Wide characters");

// Textverlauf hinzufügen und 1pt zusätzlichen horizontalen Abstand zwischen jedem Zeichen hinzufügen.
builder.Font.Spacing = 1;
builder.Writeln("Expanded by 1pt");

// Textverlauf hinzufügen und Zeichen um 1pt näher zusammenbringen.
builder.Font.Spacing = -1;
builder.Writeln("Condensed by 1pt");

doc.Save(ArtifactsDir + "Font.ScalingSpacing.docx");
```

### Siehe auch

* class [Font](../../font)
* namensraum [Aspose.Words](../../font)
* Montage [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
