---
title: NodeRendererBase Class
linktitle: NodeRendererBase
articleTitle: NodeRendererBase
second_title: Aspose.Words für .NET
description: Entdecken Sie die Klasse Aspose.Words.Rendering.NodeRendererBase – Ihre Grundlage für effizientes Shape- und OfficeMath-Rendering bei der Dokumentverarbeitung.
type: docs
weight: 5280
url: /de/net/aspose.words.rendering/noderendererbase/
---
## NodeRendererBase class

Basisklasse für[`ShapeRenderer`](../shaperenderer/) Und[`OfficeMathRenderer`](../officemathrenderer/) .

Um mehr zu erfahren, besuchen Sie die[Arbeiten mit Formen](https://docs.aspose.com/words/net/working-with-shapes/) Dokumentationsartikel.

```csharp
public abstract class NodeRendererBase
```

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [BoundsInPoints](../../aspose.words.rendering/noderendererbase/boundsinpoints/) { get; } | Ruft die tatsächlichen Grenzen der Form in Punkten ab. |
| [OpaqueBoundsInPoints](../../aspose.words.rendering/noderendererbase/opaqueboundsinpoints/) { get; } | Ruft die undurchsichtigen Grenzen der Form in Punkten ab. |
| [SizeInPoints](../../aspose.words.rendering/noderendererbase/sizeinpoints/) { get; } | Ruft die tatsächliche Größe der Form in Punkten ab. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/#getboundsinpixels)(*float, float*) | Berechnet die Grenzen der Form in Pixeln für einen angegebenen Zoomfaktor und eine angegebene Auflösung. |
| [GetBoundsInPixels](../../aspose.words.rendering/noderendererbase/getboundsinpixels/#getboundsinpixels_1)(*float, float, float*) | Berechnet die Grenzen der Form in Pixeln für einen angegebenen Zoomfaktor und eine angegebene Auflösung. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/#getopaqueboundsinpixels)(*float, float*) | Berechnet die undurchsichtigen Grenzen der Form in Pixeln für einen angegebenen Zoomfaktor und eine angegebene Auflösung. |
| [GetOpaqueBoundsInPixels](../../aspose.words.rendering/noderendererbase/getopaqueboundsinpixels/#getopaqueboundsinpixels_1)(*float, float, float*) | Berechnet die undurchsichtigen Grenzen der Form in Pixeln für einen angegebenen Zoomfaktor und eine angegebene Auflösung. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/#getsizeinpixels)(*float, float*) | Berechnet die Größe der Form in Pixeln für einen angegebenen Zoomfaktor und eine angegebene Auflösung. |
| [GetSizeInPixels](../../aspose.words.rendering/noderendererbase/getsizeinpixels/#getsizeinpixels_1)(*float, float, float*) | Berechnet die Größe der Form in Pixeln für einen angegebenen Zoomfaktor und eine angegebene Auflösung. |
| [RenderToScale](../../aspose.words.rendering/noderendererbase/rendertoscale/)(*Graphics, float, float, float*) | Rendert die Form in einGraphics Objekt auf einen angegebenen Maßstab. |
| [RenderToSize](../../aspose.words.rendering/noderendererbase/rendertosize/)(*Graphics, float, float, float, float*) | Rendert die Form in einGraphics Objekt auf eine angegebene Größe. |
| [Save](../../aspose.words.rendering/noderendererbase/save/#save)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Rendert die Form in ein Bild und speichert sie in einem Stream. |
| [Save](../../aspose.words.rendering/noderendererbase/save/#save_1)(*Stream, [SvgSaveOptions](../../aspose.words.saving/svgsaveoptions/)*) | Rendert die Form in ein SVG-Bild und speichert sie in einem Stream. |
| [Save](../../aspose.words.rendering/noderendererbase/save/#save_2)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Rendert die Form in ein Bild und speichert sie in einer Datei. |
| [Save](../../aspose.words.rendering/noderendererbase/save/#save_3)(*string, [SvgSaveOptions](../../aspose.words.saving/svgsaveoptions/)*) | Rendert die Form in ein SVG-Bild und speichert sie in einer Datei. |

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

* namensraum [Aspose.Words.Rendering](../../aspose.words.rendering/)
* Montage [Aspose.Words](../../)
