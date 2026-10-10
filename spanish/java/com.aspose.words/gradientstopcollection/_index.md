---
title: "GradientStopCollection"
linktitle: "GradientStopCollection"
second_title: "Aspose.Words para Java"
description: "Contiene una colección de objetos GradientStop en Java."
type: docs
weight: 363
url: /es/java/com.aspose.words/gradientstopcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class GradientStopCollection implements Iterable
```

Contiene una colección de [GradientStop](../../com.aspose.words/gradientstop/) objetos.

Para obtener más información, visite el artículo de documentación [ Working with Graphic Elements ][Working with Graphic Elements].

 **Remarks:** 

No crea instancias de esta clase directamente. Utilice la propiedad [Fill.getGradientStops()](../../com.aspose.words/fill/\#getGradientStops) para acceder a los puntos de degradado de los objetos de relleno.

 **Examples:** 

Muestra cómo agregar puntos de degradado al relleno de degradado.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 80.0, 80.0);
 shape.getFill().twoColorGradient(Color.green, Color.RED, GradientStyle.HORIZONTAL, GradientVariant.VARIANT_2);

 // Get gradient stops collection.
 GradientStopCollection gradientStops = shape.getFill().getGradientStops();

 // Change first gradient stop.
 gradientStops.get(0).setColor(Color.yellow);
 gradientStops.get(0).setPosition(0.1);
 gradientStops.get(0).setTransparency(0.25);

 // Add new gradient stop to the end of collection.
 GradientStop gradientStop = new GradientStop(Color.blue, 0.5);
 gradientStops.add(gradientStop);

 // Remove gradient stop at index 1.
 gradientStops.removeAt(1);
 // And insert new gradient stop at the same index 1.
 gradientStops.insert(1, new GradientStop(Color.pink, 0.75, 0.3));

 // Remove last gradient stop in the collection.
 gradientStop = gradientStops.get(2);
 gradientStops.remove(gradientStop);

 Assert.assertEquals(2, gradientStops.getCount());

 Assert.assertEquals(new Color((255), (255), (0)), gradientStops.get(0).getBaseColor());
 Assert.assertEquals(Color.yellow.getRGB(), gradientStops.get(0).getColor().getRGB());
 Assert.assertEquals(0.1d, gradientStops.get(0).getPosition(), 0.01d);
 Assert.assertEquals(0.25d, gradientStops.get(0).getTransparency(), 0.01d);

 Assert.assertEquals(Color.pink.getRGB(), gradientStops.get(1).getColor().getRGB());
 Assert.assertEquals(0.75d, gradientStops.get(1).getPosition(), 0.01d);
 Assert.assertEquals(0.3d, gradientStops.get(1).getTransparency(), 0.01d);

 // Use the compliance option to define the shape using DML
 // if you want to get "GradientStops" property after the document saves.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(); { saveOptions.setCompliance(OoxmlCompliance.ISO_29500_2008_STRICT); }

 doc.save(getArtifactsDir() + "Shape.GradientStops.docx", saveOptions);
 
```


[Working with Graphic Elements]: https://docs.aspose.com/words/java/working-with-graphic-elements/
## Métodos

| Método | Descripción |
| --- | --- |
| [add(GradientStop gradientStop)](#add-com.aspose.words.GradientStop) | Agrega un [GradientStop](../../com.aspose.words/gradientstop/) especificado a un degradado. |
| [get(int index)](#get-int) | Obtiene un objeto [GradientStop](../../com.aspose.words/gradientstop/) de la colección. |
| [getCount()](#getCount) | Obtiene un valor entero que indica la cantidad de elementos en la colección. |
| [insert(int index, GradientStop gradientStop)](#insert-int-com.aspose.words.GradientStop) | Inserta un [GradientStop](../../com.aspose.words/gradientstop/) en la colección en un índice especificado. |
| [iterator()](#iterator) | Devuelve un enumerador que recorre la colección. |
| [remove(GradientStop gradientStop)](#remove-com.aspose.words.GradientStop) | Elimina un [GradientStop](../../com.aspose.words/gradientstop/) especificado de la colección. |
| [removeAt(int index)](#removeAt-int) | Elimina un [GradientStop](../../com.aspose.words/gradientstop/) de la colección en un índice especificado. |
| [set(int index, GradientStop value)](#set-int-com.aspose.words.GradientStop) | Establece un objeto [GradientStop](../../com.aspose.words/gradientstop/) en la colección. |
### add(GradientStop gradientStop) {#add-com.aspose.words.GradientStop}
```
public GradientStop add(GradientStop gradientStop)
```


Agrega un [GradientStop](../../com.aspose.words/gradientstop/) especificado a un degradado.

 **Examples:** 

Muestra cómo agregar puntos de degradado al relleno de degradado.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 80.0, 80.0);
 shape.getFill().twoColorGradient(Color.green, Color.RED, GradientStyle.HORIZONTAL, GradientVariant.VARIANT_2);

 // Get gradient stops collection.
 GradientStopCollection gradientStops = shape.getFill().getGradientStops();

 // Change first gradient stop.
 gradientStops.get(0).setColor(Color.yellow);
 gradientStops.get(0).setPosition(0.1);
 gradientStops.get(0).setTransparency(0.25);

 // Add new gradient stop to the end of collection.
 GradientStop gradientStop = new GradientStop(Color.blue, 0.5);
 gradientStops.add(gradientStop);

 // Remove gradient stop at index 1.
 gradientStops.removeAt(1);
 // And insert new gradient stop at the same index 1.
 gradientStops.insert(1, new GradientStop(Color.pink, 0.75, 0.3));

 // Remove last gradient stop in the collection.
 gradientStop = gradientStops.get(2);
 gradientStops.remove(gradientStop);

 Assert.assertEquals(2, gradientStops.getCount());

 Assert.assertEquals(new Color((255), (255), (0)), gradientStops.get(0).getBaseColor());
 Assert.assertEquals(Color.yellow.getRGB(), gradientStops.get(0).getColor().getRGB());
 Assert.assertEquals(0.1d, gradientStops.get(0).getPosition(), 0.01d);
 Assert.assertEquals(0.25d, gradientStops.get(0).getTransparency(), 0.01d);

 Assert.assertEquals(Color.pink.getRGB(), gradientStops.get(1).getColor().getRGB());
 Assert.assertEquals(0.75d, gradientStops.get(1).getPosition(), 0.01d);
 Assert.assertEquals(0.3d, gradientStops.get(1).getTransparency(), 0.01d);

 // Use the compliance option to define the shape using DML
 // if you want to get "GradientStops" property after the document saves.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(); { saveOptions.setCompliance(OoxmlCompliance.ISO_29500_2008_STRICT); }

 doc.save(getArtifactsDir() + "Shape.GradientStops.docx", saveOptions);
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| gradientStop | [GradientStop](../../com.aspose.words/gradientstop/) |  |

**Returns:**
[GradientStop](../../com.aspose.words/gradientstop/)
### get(int index) {#get-int}
```
public GradientStop get(int index)
```


Obtiene un objeto [GradientStop](../../com.aspose.words/gradientstop/) de la colección.

 **Examples:** 

Muestra cómo agregar puntos de degradado al relleno de degradado.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 80.0, 80.0);
 shape.getFill().twoColorGradient(Color.green, Color.RED, GradientStyle.HORIZONTAL, GradientVariant.VARIANT_2);

 // Get gradient stops collection.
 GradientStopCollection gradientStops = shape.getFill().getGradientStops();

 // Change first gradient stop.
 gradientStops.get(0).setColor(Color.yellow);
 gradientStops.get(0).setPosition(0.1);
 gradientStops.get(0).setTransparency(0.25);

 // Add new gradient stop to the end of collection.
 GradientStop gradientStop = new GradientStop(Color.blue, 0.5);
 gradientStops.add(gradientStop);

 // Remove gradient stop at index 1.
 gradientStops.removeAt(1);
 // And insert new gradient stop at the same index 1.
 gradientStops.insert(1, new GradientStop(Color.pink, 0.75, 0.3));

 // Remove last gradient stop in the collection.
 gradientStop = gradientStops.get(2);
 gradientStops.remove(gradientStop);

 Assert.assertEquals(2, gradientStops.getCount());

 Assert.assertEquals(new Color((255), (255), (0)), gradientStops.get(0).getBaseColor());
 Assert.assertEquals(Color.yellow.getRGB(), gradientStops.get(0).getColor().getRGB());
 Assert.assertEquals(0.1d, gradientStops.get(0).getPosition(), 0.01d);
 Assert.assertEquals(0.25d, gradientStops.get(0).getTransparency(), 0.01d);

 Assert.assertEquals(Color.pink.getRGB(), gradientStops.get(1).getColor().getRGB());
 Assert.assertEquals(0.75d, gradientStops.get(1).getPosition(), 0.01d);
 Assert.assertEquals(0.3d, gradientStops.get(1).getTransparency(), 0.01d);

 // Use the compliance option to define the shape using DML
 // if you want to get "GradientStops" property after the document saves.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(); { saveOptions.setCompliance(OoxmlCompliance.ISO_29500_2008_STRICT); }

 doc.save(getArtifactsDir() + "Shape.GradientStops.docx", saveOptions);
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int |  |

**Returns:**
[GradientStop](../../com.aspose.words/gradientstop/) - A [GradientStop](../../com.aspose.words/gradientstop/) object in the collection.
### getCount() {#getCount}
```
public int getCount()
```


Obtiene un valor entero que indica la cantidad de elementos en la colección.

 **Examples:** 

Muestra cómo agregar puntos de degradado al relleno de degradado.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 80.0, 80.0);
 shape.getFill().twoColorGradient(Color.green, Color.RED, GradientStyle.HORIZONTAL, GradientVariant.VARIANT_2);

 // Get gradient stops collection.
 GradientStopCollection gradientStops = shape.getFill().getGradientStops();

 // Change first gradient stop.
 gradientStops.get(0).setColor(Color.yellow);
 gradientStops.get(0).setPosition(0.1);
 gradientStops.get(0).setTransparency(0.25);

 // Add new gradient stop to the end of collection.
 GradientStop gradientStop = new GradientStop(Color.blue, 0.5);
 gradientStops.add(gradientStop);

 // Remove gradient stop at index 1.
 gradientStops.removeAt(1);
 // And insert new gradient stop at the same index 1.
 gradientStops.insert(1, new GradientStop(Color.pink, 0.75, 0.3));

 // Remove last gradient stop in the collection.
 gradientStop = gradientStops.get(2);
 gradientStops.remove(gradientStop);

 Assert.assertEquals(2, gradientStops.getCount());

 Assert.assertEquals(new Color((255), (255), (0)), gradientStops.get(0).getBaseColor());
 Assert.assertEquals(Color.yellow.getRGB(), gradientStops.get(0).getColor().getRGB());
 Assert.assertEquals(0.1d, gradientStops.get(0).getPosition(), 0.01d);
 Assert.assertEquals(0.25d, gradientStops.get(0).getTransparency(), 0.01d);

 Assert.assertEquals(Color.pink.getRGB(), gradientStops.get(1).getColor().getRGB());
 Assert.assertEquals(0.75d, gradientStops.get(1).getPosition(), 0.01d);
 Assert.assertEquals(0.3d, gradientStops.get(1).getTransparency(), 0.01d);

 // Use the compliance option to define the shape using DML
 // if you want to get "GradientStops" property after the document saves.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(); { saveOptions.setCompliance(OoxmlCompliance.ISO_29500_2008_STRICT); }

 doc.save(getArtifactsDir() + "Shape.GradientStops.docx", saveOptions);
 
```

**Returns:**
int - Un valor entero que indica la cantidad de elementos en la colección.
### insert(int index, GradientStop gradientStop) {#insert-int-com.aspose.words.GradientStop}
```
public GradientStop insert(int index, GradientStop gradientStop)
```


Inserta un [GradientStop](../../com.aspose.words/gradientstop/) en la colección en un índice especificado.

 **Examples:** 

Muestra cómo agregar puntos de degradado al relleno de degradado.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 80.0, 80.0);
 shape.getFill().twoColorGradient(Color.green, Color.RED, GradientStyle.HORIZONTAL, GradientVariant.VARIANT_2);

 // Get gradient stops collection.
 GradientStopCollection gradientStops = shape.getFill().getGradientStops();

 // Change first gradient stop.
 gradientStops.get(0).setColor(Color.yellow);
 gradientStops.get(0).setPosition(0.1);
 gradientStops.get(0).setTransparency(0.25);

 // Add new gradient stop to the end of collection.
 GradientStop gradientStop = new GradientStop(Color.blue, 0.5);
 gradientStops.add(gradientStop);

 // Remove gradient stop at index 1.
 gradientStops.removeAt(1);
 // And insert new gradient stop at the same index 1.
 gradientStops.insert(1, new GradientStop(Color.pink, 0.75, 0.3));

 // Remove last gradient stop in the collection.
 gradientStop = gradientStops.get(2);
 gradientStops.remove(gradientStop);

 Assert.assertEquals(2, gradientStops.getCount());

 Assert.assertEquals(new Color((255), (255), (0)), gradientStops.get(0).getBaseColor());
 Assert.assertEquals(Color.yellow.getRGB(), gradientStops.get(0).getColor().getRGB());
 Assert.assertEquals(0.1d, gradientStops.get(0).getPosition(), 0.01d);
 Assert.assertEquals(0.25d, gradientStops.get(0).getTransparency(), 0.01d);

 Assert.assertEquals(Color.pink.getRGB(), gradientStops.get(1).getColor().getRGB());
 Assert.assertEquals(0.75d, gradientStops.get(1).getPosition(), 0.01d);
 Assert.assertEquals(0.3d, gradientStops.get(1).getTransparency(), 0.01d);

 // Use the compliance option to define the shape using DML
 // if you want to get "GradientStops" property after the document saves.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(); { saveOptions.setCompliance(OoxmlCompliance.ISO_29500_2008_STRICT); }

 doc.save(getArtifactsDir() + "Shape.GradientStops.docx", saveOptions);
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int |  |
| gradientStop | [GradientStop](../../com.aspose.words/gradientstop/) |  |

**Returns:**
[GradientStop](../../com.aspose.words/gradientstop/)
### iterator() {#iterator}
```
public Iterator iterator()
```


Devuelve un enumerador que recorre la colección.

**Returns:**
java.util.Iterator
### remove(GradientStop gradientStop) {#remove-com.aspose.words.GradientStop}
```
public boolean remove(GradientStop gradientStop)
```


Elimina un [GradientStop](../../com.aspose.words/gradientstop/) especificado de la colección.

 **Examples:** 

Muestra cómo agregar puntos de degradado al relleno de degradado.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 80.0, 80.0);
 shape.getFill().twoColorGradient(Color.green, Color.RED, GradientStyle.HORIZONTAL, GradientVariant.VARIANT_2);

 // Get gradient stops collection.
 GradientStopCollection gradientStops = shape.getFill().getGradientStops();

 // Change first gradient stop.
 gradientStops.get(0).setColor(Color.yellow);
 gradientStops.get(0).setPosition(0.1);
 gradientStops.get(0).setTransparency(0.25);

 // Add new gradient stop to the end of collection.
 GradientStop gradientStop = new GradientStop(Color.blue, 0.5);
 gradientStops.add(gradientStop);

 // Remove gradient stop at index 1.
 gradientStops.removeAt(1);
 // And insert new gradient stop at the same index 1.
 gradientStops.insert(1, new GradientStop(Color.pink, 0.75, 0.3));

 // Remove last gradient stop in the collection.
 gradientStop = gradientStops.get(2);
 gradientStops.remove(gradientStop);

 Assert.assertEquals(2, gradientStops.getCount());

 Assert.assertEquals(new Color((255), (255), (0)), gradientStops.get(0).getBaseColor());
 Assert.assertEquals(Color.yellow.getRGB(), gradientStops.get(0).getColor().getRGB());
 Assert.assertEquals(0.1d, gradientStops.get(0).getPosition(), 0.01d);
 Assert.assertEquals(0.25d, gradientStops.get(0).getTransparency(), 0.01d);

 Assert.assertEquals(Color.pink.getRGB(), gradientStops.get(1).getColor().getRGB());
 Assert.assertEquals(0.75d, gradientStops.get(1).getPosition(), 0.01d);
 Assert.assertEquals(0.3d, gradientStops.get(1).getTransparency(), 0.01d);

 // Use the compliance option to define the shape using DML
 // if you want to get "GradientStops" property after the document saves.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(); { saveOptions.setCompliance(OoxmlCompliance.ISO_29500_2008_STRICT); }

 doc.save(getArtifactsDir() + "Shape.GradientStops.docx", saveOptions);
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| gradientStop | [GradientStop](../../com.aspose.words/gradientstop/) |  |

**Returns:**
boolean -  true  si el punto de degradado se eliminó correctamente, de lo contrario  false .
### removeAt(int index) {#removeAt-int}
```
public GradientStop removeAt(int index)
```


Elimina un [GradientStop](../../com.aspose.words/gradientstop/) de la colección en un índice especificado.

 **Examples:** 

Muestra cómo agregar puntos de degradado al relleno de degradado.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 80.0, 80.0);
 shape.getFill().twoColorGradient(Color.green, Color.RED, GradientStyle.HORIZONTAL, GradientVariant.VARIANT_2);

 // Get gradient stops collection.
 GradientStopCollection gradientStops = shape.getFill().getGradientStops();

 // Change first gradient stop.
 gradientStops.get(0).setColor(Color.yellow);
 gradientStops.get(0).setPosition(0.1);
 gradientStops.get(0).setTransparency(0.25);

 // Add new gradient stop to the end of collection.
 GradientStop gradientStop = new GradientStop(Color.blue, 0.5);
 gradientStops.add(gradientStop);

 // Remove gradient stop at index 1.
 gradientStops.removeAt(1);
 // And insert new gradient stop at the same index 1.
 gradientStops.insert(1, new GradientStop(Color.pink, 0.75, 0.3));

 // Remove last gradient stop in the collection.
 gradientStop = gradientStops.get(2);
 gradientStops.remove(gradientStop);

 Assert.assertEquals(2, gradientStops.getCount());

 Assert.assertEquals(new Color((255), (255), (0)), gradientStops.get(0).getBaseColor());
 Assert.assertEquals(Color.yellow.getRGB(), gradientStops.get(0).getColor().getRGB());
 Assert.assertEquals(0.1d, gradientStops.get(0).getPosition(), 0.01d);
 Assert.assertEquals(0.25d, gradientStops.get(0).getTransparency(), 0.01d);

 Assert.assertEquals(Color.pink.getRGB(), gradientStops.get(1).getColor().getRGB());
 Assert.assertEquals(0.75d, gradientStops.get(1).getPosition(), 0.01d);
 Assert.assertEquals(0.3d, gradientStops.get(1).getTransparency(), 0.01d);

 // Use the compliance option to define the shape using DML
 // if you want to get "GradientStops" property after the document saves.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(); { saveOptions.setCompliance(OoxmlCompliance.ISO_29500_2008_STRICT); }

 doc.save(getArtifactsDir() + "Shape.GradientStops.docx", saveOptions);
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int |  |

**Returns:**
[GradientStop](../../com.aspose.words/gradientstop/) - Removed [GradientStop](../../com.aspose.words/gradientstop/).
### set(int index, GradientStop value) {#set-int-com.aspose.words.GradientStop}
```
public void set(int index, GradientStop value)
```


Establece un objeto [GradientStop](../../com.aspose.words/gradientstop/) en la colección.

 **Examples:** 

Muestra cómo agregar puntos de degradado al relleno de degradado.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 80.0, 80.0);
 shape.getFill().twoColorGradient(Color.green, Color.RED, GradientStyle.HORIZONTAL, GradientVariant.VARIANT_2);

 // Get gradient stops collection.
 GradientStopCollection gradientStops = shape.getFill().getGradientStops();

 // Change first gradient stop.
 gradientStops.get(0).setColor(Color.yellow);
 gradientStops.get(0).setPosition(0.1);
 gradientStops.get(0).setTransparency(0.25);

 // Add new gradient stop to the end of collection.
 GradientStop gradientStop = new GradientStop(Color.blue, 0.5);
 gradientStops.add(gradientStop);

 // Remove gradient stop at index 1.
 gradientStops.removeAt(1);
 // And insert new gradient stop at the same index 1.
 gradientStops.insert(1, new GradientStop(Color.pink, 0.75, 0.3));

 // Remove last gradient stop in the collection.
 gradientStop = gradientStops.get(2);
 gradientStops.remove(gradientStop);

 Assert.assertEquals(2, gradientStops.getCount());

 Assert.assertEquals(new Color((255), (255), (0)), gradientStops.get(0).getBaseColor());
 Assert.assertEquals(Color.yellow.getRGB(), gradientStops.get(0).getColor().getRGB());
 Assert.assertEquals(0.1d, gradientStops.get(0).getPosition(), 0.01d);
 Assert.assertEquals(0.25d, gradientStops.get(0).getTransparency(), 0.01d);

 Assert.assertEquals(Color.pink.getRGB(), gradientStops.get(1).getColor().getRGB());
 Assert.assertEquals(0.75d, gradientStops.get(1).getPosition(), 0.01d);
 Assert.assertEquals(0.3d, gradientStops.get(1).getTransparency(), 0.01d);

 // Use the compliance option to define the shape using DML
 // if you want to get "GradientStops" property after the document saves.
 OoxmlSaveOptions saveOptions = new OoxmlSaveOptions(); { saveOptions.setCompliance(OoxmlCompliance.ISO_29500_2008_STRICT); }

 doc.save(getArtifactsDir() + "Shape.GradientStops.docx", saveOptions);
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int |  |
| value | [GradientStop](../../com.aspose.words/gradientstop/) | Un objeto [GradientStop](../../com.aspose.words/gradientstop/) en la colección. |

