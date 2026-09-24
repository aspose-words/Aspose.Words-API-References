---
title: "SoftEdgeFormat"
linktitle: "SoftEdgeFormat"
second_title: "Aspose.Words Java için"
description: "Java'da bir nesne için yumuşak kenar biçimlendirmesini temsil eder."
type: docs
weight: 625
url: /tr/java/com.aspose.words/softedgeformat/
---

**Inheritance:**
java.lang.Object
```
public class SoftEdgeFormat
```

Bir nesnenin yumuşak kenar biçimlendirmesini temsil eder.

 **Remarks:** 

Bir nesnenin yumuşak kenar özelliklerine erişmek için [ShapeBase.getSoftEdge()](../../com.aspose.words/shapebase/\#getSoftEdge) özelliğini kullanın. [SoftEdgeFormat](../../com.aspose.words/softedgeformat/) sınıfının örneklerini doğrudan oluşturmazsınız.

 **Examples:** 

Yumuşak kenar biçimlendirmesiyle nasıl çalışılacağını gösterir.

```

 DocumentBuilder builder = new DocumentBuilder();
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 200.0, 200.0);

 // Apply soft edge to the shape.
 shape.getSoftEdge().setRadius(30.0);

 builder.getDocument().save(getArtifactsDir() + "Shape.SoftEdge.docx");

 // Load document with rectangle shape with soft edge.
 Document doc = new Document(getArtifactsDir() + "Shape.SoftEdge.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check soft edge radius.
 Assert.assertEquals(30, shape.getSoftEdge().getRadius());

 // Remove soft edge from the shape.
 shape.getSoftEdge().remove();

 // Check radius of the removed soft edge.
 Assert.assertEquals(0, shape.getSoftEdge().getRadius());
 
```
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getRadius()](#getRadius) | Yumuşak kenar etkisi için yarıçap uzunluğunu nokta (pt) cinsinden temsil eden bir double değer alır. |
| [remove()](#remove) | [SoftEdgeFormat](../../com.aspose.words/softedgeformat/) öğesini üst nesneden kaldırır. |
| [setRadius(double value)](#setRadius-double) | Yumuşak kenar etkisi için yarıçap uzunluğunu nokta (pt) cinsinden temsil eden bir double değer ayarlar. |
### getRadius() {#getRadius}
```
public double getRadius()
```


Yumuşak kenar etkisi için yarıçap uzunluğunu nokta (pt) cinsinden temsil eden bir double değer alır. Varsayılan değer 0.0'dır.

 **Examples:** 

Yumuşak kenar biçimlendirmesiyle nasıl çalışılacağını gösterir.

```

 DocumentBuilder builder = new DocumentBuilder();
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 200.0, 200.0);

 // Apply soft edge to the shape.
 shape.getSoftEdge().setRadius(30.0);

 builder.getDocument().save(getArtifactsDir() + "Shape.SoftEdge.docx");

 // Load document with rectangle shape with soft edge.
 Document doc = new Document(getArtifactsDir() + "Shape.SoftEdge.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check soft edge radius.
 Assert.assertEquals(30, shape.getSoftEdge().getRadius());

 // Remove soft edge from the shape.
 shape.getSoftEdge().remove();

 // Check radius of the removed soft edge.
 Assert.assertEquals(0, shape.getSoftEdge().getRadius());
 
```

Görüntü çözünürlüğü sınırının nasıl ayarlanacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 SvgSaveOptions saveOptions = new SvgSaveOptions();
 saveOptions.setMaxImageResolution(72);

 doc.save(getArtifactsDir() + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
 
```

**Returns:**
double - Yumuşak kenar etkisi için yarıçap uzunluğunu nokta (pt) cinsinden temsil eden bir double değer.
### remove() {#remove}
```
public void remove()
```


[SoftEdgeFormat](../../com.aspose.words/softedgeformat/) öğesini üst nesneden kaldırır.

 **Examples:** 

Yumuşak kenar biçimlendirmesiyle nasıl çalışılacağını gösterir.

```

 DocumentBuilder builder = new DocumentBuilder();
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 200.0, 200.0);

 // Apply soft edge to the shape.
 shape.getSoftEdge().setRadius(30.0);

 builder.getDocument().save(getArtifactsDir() + "Shape.SoftEdge.docx");

 // Load document with rectangle shape with soft edge.
 Document doc = new Document(getArtifactsDir() + "Shape.SoftEdge.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check soft edge radius.
 Assert.assertEquals(30, shape.getSoftEdge().getRadius());

 // Remove soft edge from the shape.
 shape.getSoftEdge().remove();

 // Check radius of the removed soft edge.
 Assert.assertEquals(0, shape.getSoftEdge().getRadius());
 
```

Görüntü çözünürlüğü sınırının nasıl ayarlanacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 SvgSaveOptions saveOptions = new SvgSaveOptions();
 saveOptions.setMaxImageResolution(72);

 doc.save(getArtifactsDir() + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
 
```

### setRadius(double value) {#setRadius-double}
```
public void setRadius(double value)
```


Yumuşak kenar etkisi için yarıçap uzunluğunu nokta (pt) cinsinden temsil eden bir double değer ayarlar. Varsayılan değer 0.0'dır.

 **Examples:** 

Yumuşak kenar biçimlendirmesiyle nasıl çalışılacağını gösterir.

```

 DocumentBuilder builder = new DocumentBuilder();
 Shape shape = builder.insertShape(ShapeType.RECTANGLE, 200.0, 200.0);

 // Apply soft edge to the shape.
 shape.getSoftEdge().setRadius(30.0);

 builder.getDocument().save(getArtifactsDir() + "Shape.SoftEdge.docx");

 // Load document with rectangle shape with soft edge.
 Document doc = new Document(getArtifactsDir() + "Shape.SoftEdge.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check soft edge radius.
 Assert.assertEquals(30, shape.getSoftEdge().getRadius());

 // Remove soft edge from the shape.
 shape.getSoftEdge().remove();

 // Check radius of the removed soft edge.
 Assert.assertEquals(0, shape.getSoftEdge().getRadius());
 
```

Görüntü çözünürlüğü sınırının nasıl ayarlanacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 SvgSaveOptions saveOptions = new SvgSaveOptions();
 saveOptions.setMaxImageResolution(72);

 doc.save(getArtifactsDir() + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Yumuşak kenar etkisi için yarıçap uzunluğunu nokta (pt) cinsinden temsil eden bir double değer. |

