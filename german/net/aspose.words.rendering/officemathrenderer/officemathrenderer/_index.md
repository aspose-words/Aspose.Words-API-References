---
title: OfficeMathRenderer.OfficeMathRenderer
second_title: Aspose.Words für .NET-API-Referenz
description: OfficeMathRenderer constructeur. Initialisiert eine neue Instanz dieser Klasse.
type: docs
weight: 10
url: /de/net/aspose.words.rendering/officemathrenderer/officemathrenderer/
---
## OfficeMathRenderer constructor

Initialisiert eine neue Instanz dieser Klasse.

```csharp
public OfficeMathRenderer(OfficeMath math)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| math | OfficeMath | Der[`OfficeMath`](../../../aspose.words.math/officemath/) Objekt, das Sie rendern möchten. |

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

// Formen mit transparenten Teilen können unterschiedliche Werte in den „OpaqueBoundsInPoints“-Eigenschaften enthalten.
Assert.AreEqual(119.0f, renderer.OpaqueBoundsInPoints.Width, 0.2f);
Assert.AreEqual(14.2f, renderer.OpaqueBoundsInPoints.Height, 0.1f);

// Ermittelt die Formgröße in Pixeln mit linearer Skalierung auf eine bestimmte DPI.
Rectangle bounds = renderer.GetBoundsInPixels(1.0f, 96.0f);

Assert.AreEqual(159, bounds.Width);
Assert.AreEqual(18, bounds.Height);

// Ermittelt die Formgröße in Pixeln, jedoch mit unterschiedlichen DPI-Werten für die horizontalen und vertikalen Abmessungen.
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

* class [OfficeMath](../../../aspose.words.math/officemath/)
* class [OfficeMathRenderer](../)
* namensraum [Aspose.Words.Rendering](../../officemathrenderer/)
* Montage [Aspose.Words](../../../)


