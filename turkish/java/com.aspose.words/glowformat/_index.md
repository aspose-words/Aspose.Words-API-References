---
title: "GlowFormat"
linktitle: "GlowFormat"
second_title: "Aspose.Words Java için"
description: "Java'da bir nesne için parıltı biçimlendirmesini temsil eder."
type: docs
weight: 358
url: /tr/java/com.aspose.words/glowformat/
---

**Inheritance:**
java.lang.Object
```
public class GlowFormat
```

Bir nesnenin parıltı biçimlendirmesini temsil eder.

 **Remarks:** 

Bir nesnenin parıltı özelliklerine erişmek için [ShapeBase.getGlow()](../../com.aspose.words/shapebase/\\#getGlow) özelliğini kullanın. [GlowFormat](../../com.aspose.words/glowformat/) sınıfının örneklerini doğrudan oluşturmazsınız.

 **Examples:** 

Parıltı şekil etkisiyle nasıl etkileşim kurulacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply glow effect to the shape.
 shape.getGlow().setColor(new Color(0xFFFA8072));
 shape.getGlow().setRadius(30.0);
 shape.getGlow().setTransparency(0.15);

 doc.save(getArtifactsDir() + "Shape.Glow.docx");

 doc = new Document(getArtifactsDir() + "Shape.Glow.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check glow effect attributes.
 Assert.assertEquals(new Color((250), (128), (114), (217)).getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(30, shape.getGlow().getRadius());
 Assert.assertEquals(0.15d, shape.getGlow().getTransparency(), 0.01d);

 // Remove glow effect from the shape.
 shape.getGlow().remove();

 Assert.assertEquals(Color.BLACK.getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(0, shape.getGlow().getRadius());
 Assert.assertEquals(0, shape.getGlow().getTransparency());
 
```
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getColor()](#getColor) | Parıltı etkisi için rengi temsil eden bir java.awt.Color nesnesi alır. |
| [getRadius()](#getRadius) | Parıltı etkisi için yarıçap uzunluğunu nokta (pt) cinsinden temsil eden bir double değer alır. |
| [getTransparency()](#getTransparency) | Parıltı etkisinin şeffaflık derecesini 0.0 (opak) ile 1.0 (şeffaf) arasında bir değer olarak alır. |
| [remove()](#remove) | [GlowFormat](../../com.aspose.words/glowformat/) öğesini üst nesneden kaldırır. |
| [setColor(Color value)](#setColor-java.awt.Color) | Parıltı etkisi için rengi temsil eden bir java.awt.Color nesnesi ayarlar. |
| [setRadius(double value)](#setRadius-double) | Parıltı etkisi için yarıçap uzunluğunu nokta (pt) cinsinden temsil eden bir double değer ayarlar. |
| [setTransparency(double value)](#setTransparency-double) | Parıltı etkisinin şeffaflık derecesini 0.0 (opak) ile 1.0 (şeffaf) arasında bir değer olarak ayarlar. |
### getColor() {#getColor}
```
public Color getColor()
```


Parıltı etkisi için rengi temsil eden bir java.awt.Color nesnesi alır. Varsayılan değer java.awt.Color\\#getBlack().getBlack().

 **Examples:** 

Parıltı şekil etkisiyle nasıl etkileşim kurulacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply glow effect to the shape.
 shape.getGlow().setColor(new Color(0xFFFA8072));
 shape.getGlow().setRadius(30.0);
 shape.getGlow().setTransparency(0.15);

 doc.save(getArtifactsDir() + "Shape.Glow.docx");

 doc = new Document(getArtifactsDir() + "Shape.Glow.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check glow effect attributes.
 Assert.assertEquals(new Color((250), (128), (114), (217)).getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(30, shape.getGlow().getRadius());
 Assert.assertEquals(0.15d, shape.getGlow().getTransparency(), 0.01d);

 // Remove glow effect from the shape.
 shape.getGlow().remove();

 Assert.assertEquals(Color.BLACK.getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(0, shape.getGlow().getRadius());
 Assert.assertEquals(0, shape.getGlow().getTransparency());
 
```

**Returns:**
java.awt.Color - Parıltı etkisi için rengi temsil eden bir java.awt.Color nesnesi.
### getRadius() {#getRadius}
```
public double getRadius()
```


Parıltı etkisi için yarıçap uzunluğunu nokta (pt) cinsinden temsil eden bir double değer alır. Varsayılan değer 0.0.

 **Examples:** 

Parıltı şekil etkisiyle nasıl etkileşim kurulacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply glow effect to the shape.
 shape.getGlow().setColor(new Color(0xFFFA8072));
 shape.getGlow().setRadius(30.0);
 shape.getGlow().setTransparency(0.15);

 doc.save(getArtifactsDir() + "Shape.Glow.docx");

 doc = new Document(getArtifactsDir() + "Shape.Glow.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check glow effect attributes.
 Assert.assertEquals(new Color((250), (128), (114), (217)).getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(30, shape.getGlow().getRadius());
 Assert.assertEquals(0.15d, shape.getGlow().getTransparency(), 0.01d);

 // Remove glow effect from the shape.
 shape.getGlow().remove();

 Assert.assertEquals(Color.BLACK.getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(0, shape.getGlow().getRadius());
 Assert.assertEquals(0, shape.getGlow().getTransparency());
 
```

**Returns:**
double - Parıltı etkisi için yarıçap uzunluğunu nokta (pt) cinsinden temsil eden bir double değer.
### getTransparency() {#getTransparency}
```
public double getTransparency()
```


Parıltı etkisinin şeffaflık derecesini 0.0 (opak) ile 1.0 (şeffaf) arasında bir değer olarak alır. Varsayılan değer 0.0.

 **Examples:** 

Parıltı şekil etkisiyle nasıl etkileşim kurulacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply glow effect to the shape.
 shape.getGlow().setColor(new Color(0xFFFA8072));
 shape.getGlow().setRadius(30.0);
 shape.getGlow().setTransparency(0.15);

 doc.save(getArtifactsDir() + "Shape.Glow.docx");

 doc = new Document(getArtifactsDir() + "Shape.Glow.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check glow effect attributes.
 Assert.assertEquals(new Color((250), (128), (114), (217)).getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(30, shape.getGlow().getRadius());
 Assert.assertEquals(0.15d, shape.getGlow().getTransparency(), 0.01d);

 // Remove glow effect from the shape.
 shape.getGlow().remove();

 Assert.assertEquals(Color.BLACK.getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(0, shape.getGlow().getRadius());
 Assert.assertEquals(0, shape.getGlow().getTransparency());
 
```

**Returns:**
double - Parıltı etkisinin şeffaflık derecesini 0.0 (opak) ile 1.0 (şeffaf) arasında bir değer.
### remove() {#remove}
```
public void remove()
```


[GlowFormat](../../com.aspose.words/glowformat/) öğesini üst nesneden kaldırır.

 **Examples:** 

Parıltı şekil etkisiyle nasıl etkileşim kurulacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply glow effect to the shape.
 shape.getGlow().setColor(new Color(0xFFFA8072));
 shape.getGlow().setRadius(30.0);
 shape.getGlow().setTransparency(0.15);

 doc.save(getArtifactsDir() + "Shape.Glow.docx");

 doc = new Document(getArtifactsDir() + "Shape.Glow.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check glow effect attributes.
 Assert.assertEquals(new Color((250), (128), (114), (217)).getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(30, shape.getGlow().getRadius());
 Assert.assertEquals(0.15d, shape.getGlow().getTransparency(), 0.01d);

 // Remove glow effect from the shape.
 shape.getGlow().remove();

 Assert.assertEquals(Color.BLACK.getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(0, shape.getGlow().getRadius());
 Assert.assertEquals(0, shape.getGlow().getTransparency());
 
```

### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Parıltı etkisi için rengi temsil eden bir java.awt.Color nesnesi ayarlar. Varsayılan değer java.awt.Color\\#getBlack().getBlack().

 **Examples:** 

Parıltı şekil etkisiyle nasıl etkileşim kurulacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply glow effect to the shape.
 shape.getGlow().setColor(new Color(0xFFFA8072));
 shape.getGlow().setRadius(30.0);
 shape.getGlow().setTransparency(0.15);

 doc.save(getArtifactsDir() + "Shape.Glow.docx");

 doc = new Document(getArtifactsDir() + "Shape.Glow.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check glow effect attributes.
 Assert.assertEquals(new Color((250), (128), (114), (217)).getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(30, shape.getGlow().getRadius());
 Assert.assertEquals(0.15d, shape.getGlow().getTransparency(), 0.01d);

 // Remove glow effect from the shape.
 shape.getGlow().remove();

 Assert.assertEquals(Color.BLACK.getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(0, shape.getGlow().getRadius());
 Assert.assertEquals(0, shape.getGlow().getTransparency());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.awt.Color | Parıltı etkisi için rengi temsil eden bir java.awt.Color nesnesi. |

### setRadius(double value) {#setRadius-double}
```
public void setRadius(double value)
```


Parıltı etkisi için yarıçap uzunluğunu nokta (pt) cinsinden temsil eden bir double değer ayarlar. Varsayılan değer 0.0.

 **Examples:** 

Parıltı şekil etkisiyle nasıl etkileşim kurulacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply glow effect to the shape.
 shape.getGlow().setColor(new Color(0xFFFA8072));
 shape.getGlow().setRadius(30.0);
 shape.getGlow().setTransparency(0.15);

 doc.save(getArtifactsDir() + "Shape.Glow.docx");

 doc = new Document(getArtifactsDir() + "Shape.Glow.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check glow effect attributes.
 Assert.assertEquals(new Color((250), (128), (114), (217)).getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(30, shape.getGlow().getRadius());
 Assert.assertEquals(0.15d, shape.getGlow().getTransparency(), 0.01d);

 // Remove glow effect from the shape.
 shape.getGlow().remove();

 Assert.assertEquals(Color.BLACK.getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(0, shape.getGlow().getRadius());
 Assert.assertEquals(0, shape.getGlow().getTransparency());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Parıltı etkisi için yarıçap uzunluğunu nokta (pt) cinsinden temsil eden bir double değer. |

### setTransparency(double value) {#setTransparency-double}
```
public void setTransparency(double value)
```


Parıltı etkisinin şeffaflık derecesini 0.0 (opak) ile 1.0 (şeffaf) arasında bir değer olarak ayarlar. Varsayılan değer 0.0.

 **Examples:** 

Parıltı şekil etkisiyle nasıl etkileşim kurulacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply glow effect to the shape.
 shape.getGlow().setColor(new Color(0xFFFA8072));
 shape.getGlow().setRadius(30.0);
 shape.getGlow().setTransparency(0.15);

 doc.save(getArtifactsDir() + "Shape.Glow.docx");

 doc = new Document(getArtifactsDir() + "Shape.Glow.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check glow effect attributes.
 Assert.assertEquals(new Color((250), (128), (114), (217)).getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(30, shape.getGlow().getRadius());
 Assert.assertEquals(0.15d, shape.getGlow().getTransparency(), 0.01d);

 // Remove glow effect from the shape.
 shape.getGlow().remove();

 Assert.assertEquals(Color.BLACK.getRGB(), shape.getGlow().getColor().getRGB());
 Assert.assertEquals(0, shape.getGlow().getRadius());
 Assert.assertEquals(0, shape.getGlow().getTransparency());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Parıltı etkisinin şeffaflık derecesi 0.0 (opak) ile 1.0 (şeffaf) arasında bir değer. |

