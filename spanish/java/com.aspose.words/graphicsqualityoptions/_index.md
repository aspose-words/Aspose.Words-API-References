---
title: "GraphicsQualityOptions"
linktitle: "GraphicsQualityOptions"
second_title: "Aspose.Words para Java"
description: "Permite especificar java.awt.RenderingHints adicionales en Java."
type: docs
weight: 367
url: /es/java/com.aspose.words/graphicsqualityoptions/
---

**Inheritance:**
java.lang.Object
```
public class GraphicsQualityOptions
```

Permite especificar **java.awt.RenderingHints** adicionales.

Para obtener más información, visite el artículo de documentación [ Save a Document ][Save a Document].

Obtiene los **java.awt.RenderingHints** actuales para ver o agregar nuevas sugerencias. Sobrescribe los **java.awt.RenderingHints** actuales.

 **Examples:** 

Muestra cómo establecer opciones de calidad de renderizado al convertir documentos a formatos de imagen.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 GraphicsQualityOptions qualityOptions = new GraphicsQualityOptions();
 qualityOptions.getRenderingHints().put(RenderingHints.KEY_ANTIALIASING, RenderingHints.VALUE_ANTIALIAS_ON); // SmoothingMode
 qualityOptions.getRenderingHints().put(RenderingHints.KEY_TEXT_ANTIALIASING, RenderingHints.VALUE_TEXT_ANTIALIAS_ON); // TextRenderingHint
 qualityOptions.getRenderingHints().put(RenderingHints.KEY_COLOR_RENDERING, RenderingHints.VALUE_COLOR_RENDER_QUALITY); // CompositingMode
 qualityOptions.getRenderingHints().put(RenderingHints.KEY_RENDERING, RenderingHints.VALUE_RENDER_QUALITY); // CompositingQuality
 qualityOptions.getRenderingHints().put(RenderingHints.KEY_INTERPOLATION, RenderingHints.VALUE_INTERPOLATION_BILINEAR); // InterpolationMode
 qualityOptions.getRenderingHints().put(RenderingHints.KEY_FRACTIONALMETRICS, RenderingHints.VALUE_FRACTIONALMETRICS_ON); // StringFormat

 ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.JPEG);
 saveOptions.setGraphicsQualityOptions(qualityOptions);

 doc.save(getArtifactsDir() + "ImageSaveOptions.GraphicsQuality.jpg", saveOptions);
 
```


[Save a Document]: https://docs.aspose.com/words/java/save-a-document/
## Métodos

| Método | Descripción |
| --- | --- |
| [getRenderingHints()](#getRenderingHints) |  |
| [getUseTileFlipMode()](#getUseTileFlipMode) | Obtiene una bandera que indica si WrapMode es TileFlipXY. |
| [setRenderingHints(RenderingHints renderingHints)](#setRenderingHints-java.awt.RenderingHints) |  |
| [setUseTileFlipMode(boolean value)](#setUseTileFlipMode-boolean) | Establece una bandera que indica si WrapMode es TileFlipXY. |
### getRenderingHints() {#getRenderingHints}
```
public RenderingHints getRenderingHints()
```




**Returns:**
java.awt.RenderingHints
### getUseTileFlipMode() {#getUseTileFlipMode}
```
public boolean getUseTileFlipMode()
```


Obtiene una bandera que indica si WrapMode es TileFlipXY.

 **Remarks:** 

El WrapMode especifica cómo se repite una textura o degradado cuando es más pequeño que el área a rellenar.

Por defecto usa WrapMode\#TILE.TILE (especifica repetición sin volteo). Esto causa un renderizado inexacto de la imagen escalada (con alta resolución).

Esta propiedad permite cambiar WrapMode a WrapMode\#TILE\_FLIP\_XY.TILE\_FLIP\_XY (especifica que los mosaicos se voltean horizontalmente al desplazarse por una fila y verticalmente al desplazarse por una columna).

 **Examples:** 

Muestra cómo evitar que aparezca la línea blanca al renderizar con alta resolución.

```

 Document doc = new Document(getMyDir() + "Shape high dpi.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShapeRenderer renderer = shape.getShapeRenderer();

 ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.PNG);
 {
     saveOptions.setResolution(500f); saveOptions.setGraphicsQualityOptions(new GraphicsQualityOptions()); { saveOptions.getGraphicsQualityOptions().setUseTileFlipMode(true); }
 }
 renderer.save(getArtifactsDir() + "ImageSaveOptions.UseTileFlipMode.png", saveOptions);
 
```

**Returns:**
boolean - Una bandera que indica si WrapMode es TileFlipXY.
### setRenderingHints(RenderingHints renderingHints) {#setRenderingHints-java.awt.RenderingHints}
```
public void setRenderingHints(RenderingHints renderingHints)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| renderingHints | java.awt.RenderingHints |  |

### setUseTileFlipMode(boolean value) {#setUseTileFlipMode-boolean}
```
public void setUseTileFlipMode(boolean value)
```


Establece una bandera que indica si WrapMode es TileFlipXY.

 **Remarks:** 

El WrapMode especifica cómo se repite una textura o degradado cuando es más pequeño que el área a rellenar.

Por defecto usa WrapMode\#TILE.TILE (especifica repetición sin volteo). Esto causa un renderizado inexacto de la imagen escalada (con alta resolución).

Esta propiedad permite cambiar WrapMode a WrapMode\#TILE\_FLIP\_XY.TILE\_FLIP\_XY (especifica que los mosaicos se voltean horizontalmente al desplazarse por una fila y verticalmente al desplazarse por una columna).

 **Examples:** 

Muestra cómo evitar que aparezca la línea blanca al renderizar con alta resolución.

```

 Document doc = new Document(getMyDir() + "Shape high dpi.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShapeRenderer renderer = shape.getShapeRenderer();

 ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.PNG);
 {
     saveOptions.setResolution(500f); saveOptions.setGraphicsQualityOptions(new GraphicsQualityOptions()); { saveOptions.getGraphicsQualityOptions().setUseTileFlipMode(true); }
 }
 renderer.save(getArtifactsDir() + "ImageSaveOptions.UseTileFlipMode.png", saveOptions);
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | Una bandera que indica si WrapMode es TileFlipXY. |

