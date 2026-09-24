---
title: "NodeRendererBase"
linktitle: "NodeRendererBase"
second_title: "Aspose.Words para Java"
description: "Clase base para ShapeRenderer y OfficeMathRenderer en Java."
type: docs
weight: 482
url: /es/java/com.aspose.words/noderendererbase/
---

**Inheritance:**
java.lang.Object
```
public abstract class NodeRendererBase
```

Clase base para [ShapeRenderer](../../com.aspose.words/shaperenderer/) y [OfficeMathRenderer](../../com.aspose.words/officemathrenderer/).

Para obtener más información, visite el artículo de documentación [ Working with Shapes ][Working with Shapes].

 **Examples:** 

Muestra cómo medir y escalar formas.

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
## Constructores

| Constructor | Descripción |
| --- | --- |
| [NodeRendererBase()](#NodeRendererBase) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [getBoundsInPixels(float scale, float dpi)](#getBoundsInPixels-float-float) | Calcula los límites de la forma en píxeles para un factor de zoom y resolución especificados. |
| [getBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)](#getBoundsInPixels-float-float-float) | Calcula los límites de la forma en píxeles para un factor de zoom y resolución especificados. |
| [getBoundsInPoints()](#getBoundsInPoints) | Obtiene los límites reales de la forma en puntos. |
| [getOpaqueBoundsInPixels(float scale, float dpi)](#getOpaqueBoundsInPixels-float-float) | Calcula los límites opacos de la forma en píxeles para un factor de zoom y resolución especificados. |
| [getOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)](#getOpaqueBoundsInPixels-float-float-float) | Calcula los límites opacos de la forma en píxeles para un factor de zoom y resolución especificados. |
| [getOpaqueBoundsInPoints()](#getOpaqueBoundsInPoints) | Obtiene los límites opacos de la forma en puntos. |
| [getSizeInPixels(float scale, float dpi)](#getSizeInPixels-float-float) | Calcula el tamaño de la forma en píxeles para un factor de zoom y resolución especificados. |
| [getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)](#getSizeInPixels-float-float-float) | Calcula el tamaño de la forma en píxeles para un factor de zoom y resolución especificados. |
| [getSizeInPoints()](#getSizeInPoints) | Obtiene el tamaño real de la forma en puntos. |
| [renderToScale(Graphics2D graphics, float x, float y, float scale)](#renderToScale-java.awt.Graphics2D-float-float-float) | Renderiza la forma en un objeto java.awt.Graphics2D a una escala especificada. |
| [renderToSize(Graphics2D graphics, float x, float y, float width, float height)](#renderToSize-java.awt.Graphics2D-float-float-float-float) | Renderiza la forma en un objeto java.awt.Graphics2D a un tamaño especificado. |
| [save(OutputStream stream, ImageSaveOptions saveOptions)](#save-java.io.OutputStream-com.aspose.words.ImageSaveOptions) |  |
| [save(OutputStream stream, SvgSaveOptions saveOptions)](#save-java.io.OutputStream-com.aspose.words.SvgSaveOptions) |  |
| [save(String fileName, ImageSaveOptions saveOptions)](#save-java.lang.String-com.aspose.words.ImageSaveOptions) | Renderiza la forma y la guarda en una imagen. |
| [save(String fileName, SvgSaveOptions saveOptions)](#save-java.lang.String-com.aspose.words.SvgSaveOptions) | Renderiza la forma y la guarda en una imagen SVG. |
### NodeRendererBase() {#NodeRendererBase}
```
public NodeRendererBase()
```


### getBoundsInPixels(float scale, float dpi) {#getBoundsInPixels-float-float}
```
public Rectangle getBoundsInPixels(float scale, float dpi)
```


Calcula los límites de la forma en píxeles para un factor de zoom y resolución especificados.

 **Remarks:** 

Este método convierte [getBoundsInPoints()](../../com.aspose.words/noderendererbase/\#getBoundsInPoints) en un rectángulo en píxeles.

 **Examples:** 

Muestra cómo medir y escalar formas.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| escala | float | El factor de zoom (1.0 es 100%). |
| dpi | float | La resolución (horizontal y vertical) para convertir de puntos a píxeles (puntos por pulgada). |

**Returns:**
java.awt.Rectangle - El cuadro delimitador real (tal como se renderiza en la página) de la forma en píxeles.
### getBoundsInPixels(float scale, float horizontalDpi, float verticalDpi) {#getBoundsInPixels-float-float-float}
```
public Rectangle getBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)
```


Calcula los límites de la forma en píxeles para un factor de zoom y resolución especificados.

 **Remarks:** 

Este método convierte [getBoundsInPoints()](../../com.aspose.words/noderendererbase/\#getBoundsInPoints) en un rectángulo en píxeles.

 **Examples:** 

Muestra cómo medir y escalar formas.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| escala | float | El factor de zoom (1.0 es 100%). |
| horizontalDpi | float | La resolución horizontal para convertir de puntos a píxeles (puntos por pulgada). |
| verticalDpi | float | La resolución vertical para convertir de puntos a píxeles (puntos por pulgada). |

**Returns:**
java.awt.Rectangle - El cuadro delimitador real (tal como se renderiza en la página) de la forma en píxeles.
### getBoundsInPoints() {#getBoundsInPoints}
```
public Rectangle2D.Float getBoundsInPoints()
```


Obtiene los límites reales de la forma en puntos.

 **Remarks:** 

Esta propiedad devuelve el cuadro delimitador real (tal como se renderiza en la página) de la forma. Los límites tienen en cuenta la rotación de la forma (si la hay).

 **Examples:** 

Muestra cómo medir y escalar formas.

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
java.awt.geom.Rectangle2D.Float - Los límites reales de la forma en puntos.
### getOpaqueBoundsInPixels(float scale, float dpi) {#getOpaqueBoundsInPixels-float-float}
```
public Rectangle getOpaqueBoundsInPixels(float scale, float dpi)
```


Calcula los límites opacos de la forma en píxeles para un factor de zoom y resolución especificados.

 **Remarks:** 

Este método convierte [getOpaqueBoundsInPoints()](../../com.aspose.words/noderendererbase/\#getOpaqueBoundsInPoints) en un rectángulo en píxeles y es útil cuando deseas crear un mapa de bits para renderizar la forma con solo la parte opaca de la forma.

 **Examples:** 

Muestra cómo medir y escalar formas.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| escala | float | El factor de zoom (1.0 es 100%). |
| dpi | float | La resolución para convertir de puntos a píxeles (puntos por pulgada). |

**Returns:**
java.awt.Rectangle - El rectángulo opaco de la forma en píxeles.
### getOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi) {#getOpaqueBoundsInPixels-float-float-float}
```
public Rectangle getOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)
```


Calcula los límites opacos de la forma en píxeles para un factor de zoom y resolución especificados.

 **Remarks:** 

Este método convierte [getOpaqueBoundsInPoints()](../../com.aspose.words/noderendererbase/\#getOpaqueBoundsInPoints) en un rectángulo en píxeles y es útil cuando deseas crear un mapa de bits para renderizar la forma con solo la parte opaca de la forma.

 **Examples:** 

Muestra cómo medir y escalar formas.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| escala | float | El factor de zoom (1.0 es 100%). |
| horizontalDpi | float | La resolución horizontal para convertir de puntos a píxeles (puntos por pulgada). |
| verticalDpi | float | La resolución vertical para convertir de puntos a píxeles (puntos por pulgada). |

**Returns:**
java.awt.Rectangle - El rectángulo opaco de la forma en píxeles.
### getOpaqueBoundsInPoints() {#getOpaqueBoundsInPoints}
```
public Rectangle2D.Float getOpaqueBoundsInPoints()
```


Obtiene los límites opacos de la forma en puntos.

 **Remarks:** 

Esta propiedad devuelve el cuadro delimitador opaco (es decir, se ignoran las partes transparentes de la forma) de la forma. Los límites tienen en cuenta la rotación de la forma.

 **Examples:** 

Muestra cómo medir y escalar formas.

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
java.awt.geom.Rectangle2D.Float - Los límites opacos de la forma en puntos.
### getSizeInPixels(float scale, float dpi) {#getSizeInPixels-float-float}
```
public Dimension getSizeInPixels(float scale, float dpi)
```


Calcula el tamaño de la forma en píxeles para un factor de zoom y resolución especificados.

 **Remarks:** 

Este método convierte [getSizeInPoints()](../../com.aspose.words/noderendererbase/\#getSizeInPoints) en tamaño en píxeles y es útil cuando deseas crear un mapa de bits para renderizar la forma de manera ordenada sobre el mapa de bits.

 **Examples:** 

Muestra cómo medir y escalar formas.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| escala | float | El factor de zoom (1.0 es 100%). |
| dpi | float | La resolución (horizontal y vertical) para convertir de puntos a píxeles (puntos por pulgada). |

**Returns:**
java.awt.Dimension - El tamaño de la forma en píxeles.
### getSizeInPixels(float scale, float horizontalDpi, float verticalDpi) {#getSizeInPixels-float-float-float}
```
public Dimension getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```


Calcula el tamaño de la forma en píxeles para un factor de zoom y resolución especificados.

 **Remarks:** 

Este método convierte [getSizeInPoints()](../../com.aspose.words/noderendererbase/\#getSizeInPoints) en tamaño en píxeles y es útil cuando deseas crear un mapa de bits para renderizar la forma de manera ordenada sobre el mapa de bits.

 **Examples:** 

Muestra cómo medir y escalar formas.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| escala | float | El factor de zoom (1.0 es 100%). |
| horizontalDpi | float | La resolución horizontal para convertir de puntos a píxeles (puntos por pulgada). |
| verticalDpi | float | La resolución vertical para convertir de puntos a píxeles (puntos por pulgada). |

**Returns:**
java.awt.Dimension - El tamaño de la forma en píxeles.
### getSizeInPoints() {#getSizeInPoints}
```
public Point2D.Float getSizeInPoints()
```


Obtiene el tamaño real de la forma en puntos.

 **Remarks:** 

Esta propiedad devuelve el tamaño del cuadro delimitador real (tal como se renderiza en la página) de la forma. El tamaño tiene en cuenta la rotación de la forma (si la hay).

 **Examples:** 

Muestra cómo medir y escalar formas.

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
java.awt.geom.Point2D.Float - El tamaño real de la forma en puntos.
### renderToScale(Graphics2D graphics, float x, float y, float scale) {#renderToScale-java.awt.Graphics2D-float-float-float}
```
public Point2D.Float renderToScale(Graphics2D graphics, float x, float y, float scale)
```


Renderiza la forma en un objeto java.awt.Graphics2D a una escala especificada.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| gráficos | java.awt.Graphics2D | El objeto donde renderizar. |
| x | float | La coordenada X (en unidades del mundo) de la esquina superior izquierda de la forma renderizada. |
| y | float | La coordenada Y (en unidades del mundo) de la esquina superior izquierda de la forma renderizada. |
| escala | float | La escala para renderizar la forma (1.0 es 100%). |

**Returns:**
java.awt.geom.Point2D.Float - El ancho y alto (en unidades del mundo) de la forma renderizada.
### renderToSize(Graphics2D graphics, float x, float y, float width, float height) {#renderToSize-java.awt.Graphics2D-float-float-float-float}
```
public float renderToSize(Graphics2D graphics, float x, float y, float width, float height)
```


Renderiza la forma en un objeto java.awt.Graphics2D a un tamaño especificado.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| gráficos | java.awt.Graphics2D | El objeto donde renderizar. |
| x | float | La coordenada X (en unidades del mundo) de la esquina superior izquierda de la forma renderizada. |
| y | float | La coordenada Y (en unidades del mundo) de la esquina superior izquierda de la forma renderizada. |
| ancho | float | El ancho máximo (en unidades del mundo) que puede ocupar la forma renderizada. |
| alto | float | El alto máximo (en unidades del mundo) que puede ocupar la forma renderizada. |

**Returns:**
float - La escala que se calculó automáticamente para que la forma renderizada se ajuste al tamaño especificado.
### save(OutputStream stream, ImageSaveOptions saveOptions) {#save-java.io.OutputStream-com.aspose.words.ImageSaveOptions}
```
public void save(OutputStream stream, ImageSaveOptions saveOptions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| stream | java.io.OutputStream |  |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) |  |

### save(OutputStream stream, SvgSaveOptions saveOptions) {#save-java.io.OutputStream-com.aspose.words.SvgSaveOptions}
```
public void save(OutputStream stream, SvgSaveOptions saveOptions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| stream | java.io.OutputStream |  |
| saveOptions | [SvgSaveOptions](../../com.aspose.words/svgsaveoptions/) |  |

### save(String fileName, ImageSaveOptions saveOptions) {#save-java.lang.String-com.aspose.words.ImageSaveOptions}
```
public void save(String fileName, ImageSaveOptions saveOptions)
```


Renderiza la forma y la guarda en una imagen.  Renderiza la forma en una imagen y la guarda en un archivo.

 **Examples:** 

Muestra cómo renderizar un objeto Office Math en un archivo de imagen en el sistema de archivos local.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | java.lang.String | El nombre del archivo de imagen. Si ya existe un archivo con el nombre especificado, se sobrescribe el archivo existente. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions/) | Especifica las opciones que controlan cómo se renderiza y guarda la forma. Puede ser  null . |

### save(String fileName, SvgSaveOptions saveOptions) {#save-java.lang.String-com.aspose.words.SvgSaveOptions}
```
public void save(String fileName, SvgSaveOptions saveOptions)
```


Renderiza la forma y la guarda en una imagen SVG.  Renderiza la forma en una imagen SVG y la guarda en un archivo.

 **Examples:** 

Muestra cómo pasar opciones de guardado al renderizar matemáticas de Office.

```

 Document doc = new Document(getMyDir() + "Office math.docx");

 OfficeMath math = (OfficeMath)doc.getChild(NodeType.OFFICE_MATH, 0, true);

 SvgSaveOptions options = new SvgSaveOptions();
 options.setTextOutputMode(SvgTextOutputMode.USE_PLACED_GLYPHS);

 math.getMathRenderer().save(getArtifactsDir() + "SvgSaveOptions.Output.svg", options);
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | java.lang.String | El nombre del archivo de imagen. Si ya existe un archivo con el nombre especificado, se sobrescribe el archivo existente. |
| saveOptions | [SvgSaveOptions](../../com.aspose.words/svgsaveoptions/) | Especifica las opciones que controlan cómo se renderiza y guarda la forma. Puede ser  null . |

