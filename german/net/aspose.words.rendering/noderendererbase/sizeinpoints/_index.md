---
title: NodeRendererBase.SizeInPoints
linktitle: SizeInPoints
articleTitle: SizeInPoints
second_title: Aspose.Words für .NET
description: Entdecken Sie die SizeInPoints-Eigenschaft von NodeRendererBase, um einfach auf die genaue Formgröße in Punkten zuzugreifen und so die Präzision und Effizienz Ihres Designs zu verbessern.
type: docs
weight: 30
url: /de/net/aspose.words.rendering/noderendererbase/sizeinpoints/
---
## NodeRendererBase.SizeInPoints property

Ruft die tatsächliche Größe der Form in Punkten ab.

```csharp
public SizeF SizeInPoints { get; }
```

## Bemerkungen

Diese Eigenschaft gibt die Größe des tatsächlichen (wie auf der Seite gerenderten) Begrenzungsrahmens der Form zurück. Die Größe berücksichtigt die Formdrehung (sofern vorhanden).

## Beispiele

Zeigt, wie Formen gemessen und skaliert werden.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);
OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

// Überprüfen Sie die Größe des Bildes, das das OfficeMath-Objekt beim Rendern erstellt.
Assert.AreEqual(122.0f, renderer.SizeInPoints.Width, 0.25f);
Assert.AreEqual(13.0f, renderer.SizeInPoints.Height, 0.15f);

Assert.AreEqual(122.0f, renderer.BoundsInPoints.Width, 0.25f);
Assert.AreEqual(13.0f, renderer.BoundsInPoints.Height, 0.15f);

// Formen mit transparenten Teilen können unterschiedliche Werte in den „OpaqueBoundsInPoints“-Eigenschaften enthalten.
Assert.AreEqual(122.0f, renderer.OpaqueBoundsInPoints.Width, 0.25f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// Holen Sie sich die Formgröße in Pixeln mit linearer Skalierung auf einen bestimmten DPI.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// Holen Sie sich die Formgröße in Pixeln, aber mit einem anderen DPI für die horizontalen und vertikalen Abmessungen.
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(27, bounds.Height);

// Die undurchsichtigen Grenzen können auch hier variieren.
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(19, bounds.Height);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.AreEqual(163, bounds.Width);
Assert.AreEqual(29, bounds.Height);
```

### Siehe auch

* class [NodeRendererBase](../)
* namensraum [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* Montage [Aspose.Words](../../../)
