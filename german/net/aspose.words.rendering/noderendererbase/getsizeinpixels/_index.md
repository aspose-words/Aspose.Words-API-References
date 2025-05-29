---
title: NodeRendererBase.GetSizeInPixels
linktitle: GetSizeInPixels
articleTitle: GetSizeInPixels
second_title: Aspose.Words für .NET
description: Entdecken Sie die NodeRendererBase GetSizeInPixels-Methode, um die Formabmessungen in Pixeln basierend auf Zoomfaktor und Auflösung präzise zu berechnen. Optimieren Sie Ihre Designs!
type: docs
weight: 60
url: /de/net/aspose.words.rendering/noderendererbase/getsizeinpixels/
---
## GetSizeInPixels(*float, float*) {#getsizeinpixels}

Berechnet die Größe der Form in Pixeln für einen angegebenen Zoomfaktor und eine angegebene Auflösung.

```csharp
public Size GetSizeInPixels(float scale, float dpi)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| scale | Single | Der Zoomfaktor (1,0 ist 100 %). |
| dpi | Single | Die Auflösung (horizontal und vertikal) zur Konvertierung von Punkten in Pixel (Punkte pro Zoll). |

### Rückgabewert

Die Größe der Form in Pixeln.

## Bemerkungen

Diese Methode konvertiert[`SizeInPoints`](../sizeinpoints/) in die Größe in Pixel und es ist nützlich , wenn Sie eine Bitmap erstellen möchten, um die Form sauber auf der Bitmap darzustellen.

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

---

## GetSizeInPixels(*float, float, float*) {#getsizeinpixels_1}

Berechnet die Größe der Form in Pixeln für einen angegebenen Zoomfaktor und eine angegebene Auflösung.

```csharp
public Size GetSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| scale | Single | Der Zoomfaktor (1,0 ist 100 %). |
| horizontalDpi | Single | Die horizontale Auflösung zur Konvertierung von Punkten in Pixel (dots per inch). |
| verticalDpi | Single | Die vertikale Auflösung zur Konvertierung von Punkten in Pixel (dots per inch). |

### Rückgabewert

Die Größe der Form in Pixeln.

## Bemerkungen

Diese Methode konvertiert[`SizeInPoints`](../sizeinpoints/) in die Größe in Pixel und es ist nützlich , wenn Sie eine Bitmap erstellen möchten, um die Form sauber auf der Bitmap darzustellen.

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
