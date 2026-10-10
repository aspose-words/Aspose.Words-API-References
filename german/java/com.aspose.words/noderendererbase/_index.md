---
title: "NodeRendererBase"
linktitle: "NodeRendererBase"
second_title: "Aspose.Words für Java"
description: "Basisklasse für ShapeRenderer und OfficeMathRenderer in Java."
type: docs
weight: 482
url: /de/java/com.aspose.words/noderendererbase/
---

**Inheritance:**
java.lang.Object
```
public abstract class NodeRendererBase
```

Basisklasse für [ShapeRenderer](../../com.aspose.words/shaperenderer/) und [OfficeMathRenderer](../../com.aspose.words/officemathrenderer/).

Um mehr zu erfahren, besuchen Sie den [ Working with Shapes ][Working with Shapes] Dokumentationsartikel.

 **Examples:** 

Zeigt, wie Formen gemessen und skaliert werden.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```


[Working with Shapes]: https://docs.aspose.com/words/java/working-with-shapes/
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [NodeRendererBase()](#NodeRendererBase) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getBoundsInPixels(float scale, float dpi)](#getBoundsInPixels-float-float) | Berechnet die Begrenzungen der Form in Pixeln für einen angegebenen Zoomfaktor und eine Auflösung. |
| [getBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)](#getBoundsInPixels-float-float-float) | Berechnet die Begrenzungen der Form in Pixeln für einen angegebenen Zoomfaktor und eine Auflösung. |
| [getBoundsInPoints()](#getBoundsInPoints) | Ermittelt die tatsächlichen Begrenzungen der Form in Punkten. |
| [getOpaqueBoundsInPixels(float scale, float dpi)](#getOpaqueBoundsInPixels-float-float) | Berechnet die undurchsichtigen Begrenzungen der Form in Pixeln für einen angegebenen Zoomfaktor und eine Auflösung. |
| [getOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)](#getOpaqueBoundsInPixels-float-float-float) | Berechnet die undurchsichtigen Begrenzungen der Form in Pixeln für einen angegebenen Zoomfaktor und eine Auflösung. |
| [getOpaqueBoundsInPoints()](#getOpaqueBoundsInPoints) | Ermittelt die undurchsichtigen Begrenzungen der Form in Punkten. |
| [getSizeInPixels(float scale, float dpi)](#getSizeInPixels-float-float) | Berechnet die Größe der Form in Pixeln für einen angegebenen Zoomfaktor und eine Auflösung. |
| [getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)](#getSizeInPixels-float-float-float) | Berechnet die Größe der Form in Pixeln für einen angegebenen Zoomfaktor und eine Auflösung. |
| [getSizeInPoints()](#getSizeInPoints) | Ermittelt die tatsächliche Größe der Form in Punkten. |
| [renderToScale(Graphics2D graphics, float x, float y, float scale)](#renderToScale-java.awt.Graphics2D-float-float-float) | Rendert die Form in ein java.awt.Graphics2D-Objekt mit einem angegebenen Maßstab. |
| [renderToSize(Graphics2D graphics, float x, float y, float width, float height)](#renderToSize-java.awt.Graphics2D-float-float-float-float) | Rendert die Form in ein java.awt.Graphics2D-Objekt mit einer angegebenen Größe. |
| [save(OutputStream stream, ImageSaveOptions saveOptions)](#save-java.io.OutputStream-com.aspose.words.ImageSaveOptions) |  |
| [save(OutputStream stream, SvgSaveOptions saveOptions)](#save-java.io.OutputStream-com.aspose.words.SvgSaveOptions) |  |
| [save(String fileName, ImageSaveOptions saveOptions)](#save-java.lang.String-com.aspose.words.ImageSaveOptions) | Rendert die Form und speichert sie in ein Bild. |
| [save(String fileName, SvgSaveOptions saveOptions)](#save-java.lang.String-com.aspose.words.SvgSaveOptions) | Rendert die Form und speichert sie in ein SVG-Bild. |
### NodeRendererBase() {#NodeRendererBase}
```
public NodeRendererBase()
```


### getBoundsInPixels(float scale, float dpi) {#getBoundsInPixels-float-float}
```
public Rectangle getBoundsInPixels(float scale, float dpi)
```


Berechnet die Begrenzungen der Form in Pixeln für einen angegebenen Zoomfaktor und eine Auflösung.

 **Remarks:** 

Diese Methode konvertiert [getBoundsInPoints()](../../com.aspose.words/noderendererbase/\#getBoundsInPoints) in ein Rechteck in Pixeln.

 **Examples:** 

Zeigt, wie Formen gemessen und skaliert werden.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Maßstab | float | Der Zoomfaktor (1,0 entspricht 100 %). |
| dpi | float | Die Auflösung (horizontal und vertikal), um von Punkten zu Pixeln (dots per inch) zu konvertieren. |

**Returns:**
java.awt.Rectangle – Die tatsächliche (wie auf der Seite gerenderte) Begrenzungsbox der Form in Pixeln.
### getBoundsInPixels(float scale, float horizontalDpi, float verticalDpi) {#getBoundsInPixels-float-float-float}
```
public Rectangle getBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)
```


Berechnet die Begrenzungen der Form in Pixeln für einen angegebenen Zoomfaktor und eine Auflösung.

 **Remarks:** 

Diese Methode konvertiert [getBoundsInPoints()](../../com.aspose.words/noderendererbase/\#getBoundsInPoints) in ein Rechteck in Pixeln.

 **Examples:** 

Zeigt, wie Formen gemessen und skaliert werden.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Maßstab | float | Der Zoomfaktor (1,0 entspricht 100 %). |
| horizontalDpi | float | Die horizontale Auflösung, um von Punkten zu Pixeln (dots per inch) zu konvertieren. |
| verticalDpi | float | Die vertikale Auflösung, um von Punkten zu Pixeln (dots per inch) zu konvertieren. |

**Returns:**
java.awt.Rectangle – Die tatsächliche (wie auf der Seite gerenderte) Begrenzungsbox der Form in Pixeln.
### getBoundsInPoints() {#getBoundsInPoints}
```
public Rectangle2D.Float getBoundsInPoints()
```


Ermittelt die tatsächlichen Begrenzungen der Form in Punkten.

 **Remarks:** 

Diese Eigenschaft gibt die tatsächliche (wie auf der Seite gerenderte) Begrenzungsbox der Form zurück. Die Begrenzungen berücksichtigen die Drehung der Form (falls vorhanden).

 **Examples:** 

Zeigt, wie Formen gemessen und skaliert werden.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Returns:**
java.awt.geom.Rectangle2D.Float – Die tatsächlichen Begrenzungen der Form in Punkten.
### getOpaqueBoundsInPixels(float scale, float dpi) {#getOpaqueBoundsInPixels-float-float}
```
public Rectangle getOpaqueBoundsInPixels(float scale, float dpi)
```


Berechnet die undurchsichtigen Begrenzungen der Form in Pixeln für einen angegebenen Zoomfaktor und eine Auflösung.

 **Remarks:** 

Diese Methode konvertiert [getOpaqueBoundsInPoints()](../../com.aspose.words/noderendererbase/\#getOpaqueBoundsInPoints) in ein Rechteck in Pixeln und ist nützlich, wenn Sie ein Bitmap erstellen möchten, um die Form nur mit dem undurchsichtigen Teil zu rendern.

 **Examples:** 

Zeigt, wie Formen gemessen und skaliert werden.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Maßstab | float | Der Zoomfaktor (1,0 entspricht 100 %). |
| dpi | float | Die Auflösung zur Umwandlung von Punkten in Pixel (Punkte pro Zoll). |

**Returns:**
java.awt.Rectangle - Das undurchsichtige Rechteck der Form in Pixeln.
### getOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi) {#getOpaqueBoundsInPixels-float-float-float}
```
public Rectangle getOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)
```


Berechnet die undurchsichtigen Begrenzungen der Form in Pixeln für einen angegebenen Zoomfaktor und eine Auflösung.

 **Remarks:** 

Diese Methode konvertiert [getOpaqueBoundsInPoints()](../../com.aspose.words/noderendererbase/\#getOpaqueBoundsInPoints) in ein Rechteck in Pixeln und ist nützlich, wenn Sie ein Bitmap erstellen möchten, um die Form nur mit dem undurchsichtigen Teil zu rendern.

 **Examples:** 

Zeigt, wie Formen gemessen und skaliert werden.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Maßstab | float | Der Zoomfaktor (1,0 entspricht 100 %). |
| horizontalDpi | float | Die horizontale Auflösung, um von Punkten zu Pixeln (dots per inch) zu konvertieren. |
| verticalDpi | float | Die vertikale Auflösung, um von Punkten zu Pixeln (dots per inch) zu konvertieren. |

**Returns:**
java.awt.Rectangle - Das undurchsichtige Rechteck der Form in Pixeln.
### getOpaqueBoundsInPoints() {#getOpaqueBoundsInPoints}
```
public Rectangle2D.Float getOpaqueBoundsInPoints()
```


Ermittelt die undurchsichtigen Begrenzungen der Form in Punkten.

 **Remarks:** 

Diese Eigenschaft gibt die undurchsichtige (d. h. transparente Teile der Form werden ignoriert) Begrenzungsbox der Form zurück. Die Begrenzung berücksichtigt die Drehung der Form.

 **Examples:** 

Zeigt, wie Formen gemessen und skaliert werden.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Returns:**
java.awt.geom.Rectangle2D.Float - Die undurchsichtigen Begrenzungen der Form in Punkten.
### getSizeInPixels(float scale, float dpi) {#getSizeInPixels-float-float}
```
public Dimension getSizeInPixels(float scale, float dpi)
```


Berechnet die Größe der Form in Pixeln für einen angegebenen Zoomfaktor und eine Auflösung.

 **Remarks:** 

Diese Methode konvertiert [getSizeInPoints()](../../com.aspose.words/noderendererbase/\#getSizeInPoints) in eine Größe in Pixel und ist nützlich, wenn Sie ein Bitmap erstellen möchten, um die Form sauber auf das Bitmap zu rendern.

 **Examples:** 

Zeigt, wie Formen gemessen und skaliert werden.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Maßstab | float | Der Zoomfaktor (1,0 entspricht 100 %). |
| dpi | float | Die Auflösung (horizontal und vertikal), um von Punkten zu Pixeln (dots per inch) zu konvertieren. |

**Returns:**
java.awt.Dimension - Die Größe der Form in Pixeln.
### getSizeInPixels(float scale, float horizontalDpi, float verticalDpi) {#getSizeInPixels-float-float-float}
```
public Dimension getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```


Berechnet die Größe der Form in Pixeln für einen angegebenen Zoomfaktor und eine Auflösung.

 **Remarks:** 

Diese Methode konvertiert [getSizeInPoints()](../../com.aspose.words/noderendererbase/\#getSizeInPoints) in eine Größe in Pixel und ist nützlich, wenn Sie ein Bitmap erstellen möchten, um die Form sauber auf das Bitmap zu rendern.

 **Examples:** 

Zeigt, wie Formen gemessen und skaliert werden.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Maßstab | float | Der Zoomfaktor (1,0 entspricht 100 %). |
| horizontalDpi | float | Die horizontale Auflösung, um von Punkten zu Pixeln (dots per inch) zu konvertieren. |
| verticalDpi | float | Die vertikale Auflösung, um von Punkten zu Pixeln (dots per inch) zu konvertieren. |

**Returns:**
java.awt.Dimension - Die Größe der Form in Pixeln.
### getSizeInPoints() {#getSizeInPoints}
```
public Point2D.Float getSizeInPoints()
```


Ermittelt die tatsächliche Größe der Form in Punkten.

 **Remarks:** 

Diese Eigenschaft gibt die Größe der tatsächlichen (wie auf der Seite gerenderten) Begrenzungsbox der Form zurück. Die Größe berücksichtigt die Drehung der Form (falls vorhanden).

 **Examples:** 

Zeigt, wie Formen gemessen und skaliert werden.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath officeMath = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);
 OfficeMathRenderer renderer = new OfficeMathRenderer(officeMath);

 Assert.assertEquals(122.0f, renderer.getBoundsInPoints().getWidth(), 0.25f);
 Assert.assertEquals(12.9f, renderer.getBoundsInPoints().getHeight(), 0.1f);

 // Shapes with transparent parts may contain different values in the "OpaqueBoundsInPoints" properties.
 Assert.assertEquals(119.5f, 0.25f, renderer.getOpaqueBoundsInPoints().getWidth());
 Assert.assertEquals(14.2f, renderer.getOpaqueBoundsInPoints().getHeight(), 0.1f);

 // Get the shape size in pixels, with linear scaling to a specific DPI.
 Rectangle bounds = renderer.getBoundsInPixels(1.0f, 96.0f);

 String dpi96 = "DPI 96";
 Assert.assertEquals(163, bounds.getWidth(), dpi96);
 Assert.assertEquals(18, bounds.getHeight(), dpi96);

 // Get the shape size in pixels, but with a different DPI for the horizontal and vertical dimensions.
 bounds = renderer.getBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150 = "DPI 96 150";
 Assert.assertEquals(163, bounds.getWidth(), dpi96150);
 Assert.assertEquals(27, bounds.getHeight(), dpi96150);

 // The opaque bounds may vary here also.
 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f);
 String dpi96Opaque = "DPI 96 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96Opaque);
 Assert.assertEquals(19, bounds.getHeight(), dpi96Opaque);

 bounds = renderer.getOpaqueBoundsInPixels(1.0f, 96.0f, 150.0f);
 String dpi96150Opaque = "DPI 96 150 Opaque";
 Assert.assertEquals(160, bounds.getWidth(), dpi96150Opaque);
 Assert.assertEquals(29, bounds.getHeight(), dpi96150Opaque);
 
```

**Returns:**
java.awt.geom.Point2D.Float - Die tatsächliche Größe der Form in Punkten.
### renderToScale(Graphics2D graphics, float x, float y, float scale) {#renderToScale-java.awt.Graphics2D-float-float-float}
```
public Point2D.Float renderToScale(Graphics2D graphics, float x, float y, float scale)
```


Rendert die Form in ein java.awt.Graphics2D-Objekt mit einem angegebenen Maßstab.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Grafik | java.awt.Graphics2D | Das Objekt, in das gerendert werden soll. |
| x | float | Die X-Koordinate (in Welteinheiten) der oberen linken Ecke der gerenderten Form. |
| y | float | Die Y-Koordinate (in Welteinheiten) der oberen linken Ecke der gerenderten Form. |
| Maßstab | float | Der Maßstab für das Rendern der Form (1,0 entspricht 100 %). |

**Returns:**
java.awt.geom.Point2D.Float - Die Breite und Höhe (in Welteinheiten) der gerenderten Form.
### renderToSize(Graphics2D graphics, float x, float y, float width, float height) {#renderToSize-java.awt.Graphics2D-float-float-float-float}
```
public float renderToSize(Graphics2D graphics, float x, float y, float width, float height)
```


Rendert die Form in ein java.awt.Graphics2D-Objekt mit einer angegebenen Größe.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Grafik | java.awt.Graphics2D | Das Objekt, in das gerendert werden soll. |
| x | float | Die X-Koordinate (in Welteinheiten) der oberen linken Ecke der gerenderten Form. |
| y | float | Die Y-Koordinate (in Welteinheiten) der oberen linken Ecke der gerenderten Form. |
| Breite | float | Die maximale Breite (in Welteinheiten), die von der gerenderten Form eingenommen werden kann. |
| Höhe | float | Die maximale Höhe (in Welteinheiten), die von der gerenderten Form eingenommen werden kann. |

**Returns:**
float - Der Maßstab, der automatisch für die gerenderte Form berechnet wurde, um die angegebene Größe zu passen.
### save(OutputStream stream, ImageSaveOptions saveOptions) {#save-java.io.OutputStream-com.aspose.words.ImageSaveOptions}
```
public void save(OutputStream stream, ImageSaveOptions saveOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | java.io.OutputStream |  |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) |  |

### save(OutputStream stream, SvgSaveOptions saveOptions) {#save-java.io.OutputStream-com.aspose.words.SvgSaveOptions}
```
public void save(OutputStream stream, SvgSaveOptions saveOptions)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | java.io.OutputStream |  |
| saveOptions | [SvgSaveOptions](../../com.aspose.words/svgsaveoptions/) |  |

### save(String fileName, ImageSaveOptions saveOptions) {#save-java.lang.String-com.aspose.words.ImageSaveOptions}
```
public void save(String fileName, ImageSaveOptions saveOptions)
```


Rendert die Form und speichert sie in ein Bild.  Rendert die Form in ein Bild und speichert sie in einer Datei.

 **Examples:** 

Zeigt, wie ein Office‑Math‑Objekt in eine Bilddatei im lokalen Dateisystem gerendert wird.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath math = (OfficeMath) doc.getChild(NodeType.OFFICE_MATH, 0, true);

 // Create an "ImageSaveOptions" object to pass to the node renderer's "Save" method to modify
 // how it renders the OfficeMath node into an image.
 ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.PNG);

 // Set the "Scale" property to 5 to render the object to five times its original size.
 saveOptions.setScale(5f);

 math.getMathRenderer().save(getArtifactsDir() + "Shape.RenderOfficeMath.png", saveOptions);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | java.lang.String | Der Name der Bilddatei. Wenn bereits eine Datei mit dem angegebenen Namen existiert, wird die vorhandene Datei überschrieben. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Gibt die Optionen an, die steuern, wie die Form gerendert und gespeichert wird. Kann  null  sein. |

### save(String fileName, SvgSaveOptions saveOptions) {#save-java.lang.String-com.aspose.words.SvgSaveOptions}
```
public void save(String fileName, SvgSaveOptions saveOptions)
```


Rendert die Form und speichert sie in ein SVG‑Bild.  Rendert die Form in ein SVG‑Bild und speichert sie in einer Datei.

 **Examples:** 

Zeigt, wie Speicheroptionen beim Rendern von Office‑Mathematik übergeben werden.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath math = (OfficeMath)doc.getChild(NodeType.OFFICE_MATH, 0, true);

 SvgSaveOptions options = new SvgSaveOptions();
 options.setTextOutputMode(SvgTextOutputMode.USE_PLACED_GLYPHS);

 math.getMathRenderer().save(getArtifactsDir() + "SvgSaveOptions.Output.svg", options);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | java.lang.String | Der Name der Bilddatei. Wenn bereits eine Datei mit dem angegebenen Namen existiert, wird die vorhandene Datei überschrieben. |
| saveOptions | [SvgSaveOptions](../../com.aspose.words/svgsaveoptions/) | Gibt die Optionen an, die steuern, wie die Form gerendert und gespeichert wird. Kann  null  sein. |

