---
title: NodeRendererBase.SizeInPoints
second_title: Aspose.Words für .NET-API-Referenz
description: NodeRendererBase eigendom. Ruft die tatsächliche Größe der Form in Punkten ab.
type: docs
weight: 30
url: /de/net/aspose.words.rendering/noderendererbase/sizeinpoints/
---
## NodeRendererBase.SizeInPoints property

Ruft die tatsächliche Größe der Form in Punkten ab.

```csharp
public SizeF SizeInPoints { get; }
```

### Bemerkungen

Diese Eigenschaft gibt die Größe des tatsächlichen (wie auf der Seite gerenderten) Begrenzungsrahmens der Form zurück. Die Größe berücksichtigt die Rotation der Form (falls vorhanden).

### Beispiele

Zeigt, wie Formen gemessen und skaliert werden.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);
OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

// Überprüfen Sie die Größe des Bildes, das das OfficeMath-Objekt beim Rendern erstellt.
Assert.AreEqual(119.0f, renderer.SizeInPoints.Width, 0.2f);
Assert.AreEqual(13.0f, renderer.SizeInPoints.Height, 0.1f);

Assert.AreEqual(119.0f, renderer.BoundsInPoints.Width, 0.2f);
Assert.AreEqual(13.0f, renderer.BoundsInPoints.Height, 0.1f);

// Shapes mit transparenten Teilen können unterschiedliche Werte in den "OpaqueBoundsInPoints"-Eigenschaften enthalten.
Assert.AreEqual(119.0f, renderer.OpaqueBoundsInPoints.Width, 0.2f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// Holen Sie sich die Formgröße in Pixel, mit linearer Skalierung auf eine bestimmte DPI.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// Holen Sie sich die Formgröße in Pixel, aber mit einem anderen DPI für die horizontalen und vertikalen Dimensionen.
bounds = renderer.GetBoundsInPixels(1.0f, 96.0f, 150.0f);
Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(28, bounds.Height);

// Die undurchsichtigen Grenzen können auch hier variieren.
bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

bounds = renderer.GetOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(30, bounds.Height);
```

### Siehe auch

* class [NodeRendererBase](../)
* namensraum [Aspose.Words.Rendering](../../noderendererbase/)
* Montage [Aspose.Words](../../../)


