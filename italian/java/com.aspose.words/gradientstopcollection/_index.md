---
title: "GradientStopCollection"
linktitle: "GradientStopCollection"
second_title: "Aspose.Words per Java"
description: "Contiene una raccolta di oggetti GradientStop in Java."
type: docs
weight: 363
url: /it/java/com.aspose.words/gradientstopcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class GradientStopCollection implements Iterable
```

Contiene una raccolta di oggetti [GradientStop](../../com.aspose.words/gradientstop/).

Per saperne di più, visita l'articolo di documentazione [ Lavorare con gli Elementi Grafici ][Working with Graphic Elements].

 **Remarks:** 

Non si creano istanze di questa classe direttamente. Usa la proprietà [Fill.getGradientStops()](../../com.aspose.words/fill/\#getGradientStops) per accedere ai gradient stop degli oggetti fill.

 **Examples:** 

Mostra come aggiungere gradient stop al riempimento gradiente.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [add(GradientStop gradientStop)](#add-com.aspose.words.GradientStop) | Aggiunge un [GradientStop](../../com.aspose.words/gradientstop/) specificato a un gradiente. |
| [get(int index)](#get-int) | Ottiene un oggetto [GradientStop](../../com.aspose.words/gradientstop/) nella raccolta. |
| [getCount()](#getCount) | Restituisce un valore intero che indica il numero di elementi nella raccolta. |
| [insert(int index, GradientStop gradientStop)](#insert-int-com.aspose.words.GradientStop) | Inserisce un [GradientStop](../../com.aspose.words/gradientstop/) nella raccolta a un indice specificato. |
| [iterator()](#iterator) | Restituisce un enumeratore che itera attraverso la raccolta. |
| [remove(GradientStop gradientStop)](#remove-com.aspose.words.GradientStop) | Rimuove un [GradientStop](../../com.aspose.words/gradientstop/) specificato dalla raccolta. |
| [removeAt(int index)](#removeAt-int) | Rimuove un [GradientStop](../../com.aspose.words/gradientstop/) dalla raccolta a un indice specificato. |
| [set(int index, GradientStop value)](#set-int-com.aspose.words.GradientStop) | Imposta un oggetto [GradientStop](../../com.aspose.words/gradientstop/) nella raccolta. |
### add(GradientStop gradientStop) {#add-com.aspose.words.GradientStop}
```
public GradientStop add(GradientStop gradientStop)
```


Aggiunge un [GradientStop](../../com.aspose.words/gradientstop/) specificato a un gradiente.

 **Examples:** 

Mostra come aggiungere gradient stop al riempimento gradiente.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| gradientStop | [GradientStop](../../com.aspose.words/gradientstop/) |  |

**Returns:**
[GradientStop](../../com.aspose.words/gradientstop/)
### get(int index) {#get-int}
```
public GradientStop get(int index)
```


Ottiene un oggetto [GradientStop](../../com.aspose.words/gradientstop/) nella raccolta.

 **Examples:** 

Mostra come aggiungere gradient stop al riempimento gradiente.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int |  |

**Returns:**
[GradientStop](../../com.aspose.words/gradientstop/) - A [GradientStop](../../com.aspose.words/gradientstop/) object in the collection.
### getCount() {#getCount}
```
public int getCount()
```


Restituisce un valore intero che indica il numero di elementi nella raccolta.

 **Examples:** 

Mostra come aggiungere gradient stop al riempimento gradiente.

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
int - Un valore intero che indica il numero di elementi nella raccolta.
### insert(int index, GradientStop gradientStop) {#insert-int-com.aspose.words.GradientStop}
```
public GradientStop insert(int index, GradientStop gradientStop)
```


Inserisce un [GradientStop](../../com.aspose.words/gradientstop/) nella raccolta a un indice specificato.

 **Examples:** 

Mostra come aggiungere gradient stop al riempimento gradiente.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int |  |
| gradientStop | [GradientStop](../../com.aspose.words/gradientstop/) |  |

**Returns:**
[GradientStop](../../com.aspose.words/gradientstop/)
### iterator() {#iterator}
```
public Iterator iterator()
```


Restituisce un enumeratore che itera attraverso la raccolta.

**Returns:**
java.util.Iterator
### remove(GradientStop gradientStop) {#remove-com.aspose.words.GradientStop}
```
public boolean remove(GradientStop gradientStop)
```


Rimuove un [GradientStop](../../com.aspose.words/gradientstop/) specificato dalla raccolta.

 **Examples:** 

Mostra come aggiungere gradient stop al riempimento gradiente.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| gradientStop | [GradientStop](../../com.aspose.words/gradientstop/) |  |

**Returns:**
boolean -  true  se il gradient stop è stato rimosso con successo, altrimenti  false .
### removeAt(int index) {#removeAt-int}
```
public GradientStop removeAt(int index)
```


Rimuove un [GradientStop](../../com.aspose.words/gradientstop/) dalla raccolta a un indice specificato.

 **Examples:** 

Mostra come aggiungere gradient stop al riempimento gradiente.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int |  |

**Returns:**
[GradientStop](../../com.aspose.words/gradientstop/) - Removed [GradientStop](../../com.aspose.words/gradientstop/).
### set(int index, GradientStop value) {#set-int-com.aspose.words.GradientStop}
```
public void set(int index, GradientStop value)
```


Imposta un oggetto [GradientStop](../../com.aspose.words/gradientstop/) nella raccolta.

 **Examples:** 

Mostra come aggiungere gradient stop al riempimento gradiente.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int |  |
| value | [GradientStop](../../com.aspose.words/gradientstop/) | Un oggetto [GradientStop](../../com.aspose.words/gradientstop/) nella raccolta. |

