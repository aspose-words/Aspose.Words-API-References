---
title: Font.Scaling
linktitle: Scaling
articleTitle: Scaling
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „Schriftskalierung“, um die Zeichenbreite in Prozent anzupassen und so die Lesbarkeit des Textes und die Designflexibilität für Ihre Projekte zu verbessern.
type: docs
weight: 320
url: /de/net/aspose.words/font/scaling/
---
## Font.Scaling property

Ruft die Zeichenbreitenskalierung in Prozent ab oder legt sie fest.

```csharp
public int Scaling { get; set; }
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
