---
title: "ReflectionFormat"
linktitle: "ReflectionFormat"
second_title: "Aspose.Words Java için"
description: "Java'da bir nesne için yansıma biçimlendirmesini temsil eder."
type: docs
weight: 560
url: /tr/java/com.aspose.words/reflectionformat/
---

**Inheritance:**
java.lang.Object
```
public class ReflectionFormat
```

Bir nesnenin yansıma biçimlendirmesini temsil eder.

 **Remarks:** 

Bir nesnenin yansıma özelliklerine erişmek için [ShapeBase.getReflection()](../../com.aspose.words/shapebase/\#getReflection) özelliğini kullanın. [ReflectionFormat](../../com.aspose.words/reflectionformat/) sınıfının örneklerini doğrudan oluşturmazsınız.

 **Examples:** 

Yansıma şekil etkisiyle nasıl etkileşim kurulacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply reflection effect to the shape.
 shape.getReflection().setTransparency(0.37);
 shape.getReflection().setSize(0.48);
 shape.getReflection().setBlur(17.5);
 shape.getReflection().setDistance(9.2);

 doc.save(getArtifactsDir() + "Shape.Reflection.docx");

 doc = new Document(getArtifactsDir() + "Shape.Reflection.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check reflection effect attributes.
 Assert.assertEquals(0.37d, shape.getReflection().getTransparency(), 0.01d);
 Assert.assertEquals(0.48d, shape.getReflection().getSize(), 0.01d);
 Assert.assertEquals(17.5d, shape.getReflection().getBlur(), 0.01d);
 Assert.assertEquals(9.2d, shape.getReflection().getDistance(), 0.01d);

 // Remove reflection effect from the shape.
 shape.getReflection().remove();

 Assert.assertEquals(0, shape.getReflection().getTransparency());
 Assert.assertEquals(0, shape.getReflection().getSize());
 Assert.assertEquals(0, shape.getReflection().getBlur());
 Assert.assertEquals(0, shape.getReflection().getDistance());
 
```
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getBlur()](#getBlur) | Yansıma etkisine uygulanan bulanıklık derecesini puan cinsinden belirten bir double değer döndürür. |
| [getDistance()](#getDistance) | Yansıtılan görüntünün nesneden ayrılma miktarını puan cinsinden belirten bir double değer döndürür. |
| [getSize()](#getSize) | Yansımanın, yansıtılan nesnenin yüzdesi olarak boyutunu temsil eden 0.0 ile 1.0 arasında bir double değer döndürür. |
| [getTransparency()](#getTransparency) | Yansıma etkisinin şeffaflık derecesini temsil eden 0.0 (opak) ile 1.0 (şeffaf) arasında bir double değer döndürür. |
| [remove()](#remove) | [ReflectionFormat](../../com.aspose.words/reflectionformat/) öğesini üst nesneden kaldırır. |
| [setBlur(double value)](#setBlur-double) | Yansıma etkisine uygulanan bulanıklık derecesini puan cinsinden belirten bir double değer ayarlar. |
| [setDistance(double value)](#setDistance-double) | Yansıtılan görüntünün nesneden ayrılma miktarını puan cinsinden belirten bir double değer ayarlar. |
| [setSize(double value)](#setSize-double) | Yansımanın, yansıtılan nesnenin yüzdesi olarak boyutunu temsil eden 0.0 ile 1.0 arasında bir double değer ayarlar. |
| [setTransparency(double value)](#setTransparency-double) | Yansıma etkisinin şeffaflık derecesini temsil eden 0.0 (opak) ile 1.0 (şeffaf) arasında bir double değer ayarlar. |
### getBlur() {#getBlur}
```
public double getBlur()
```


Yansıma etkisine uygulanan bulanıklık derecesini puan cinsinden belirten bir double değer döndürür. Varsayılan değer 0.0'dır.

 **Examples:** 

Yansıma şekil etkisiyle nasıl etkileşim kurulacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply reflection effect to the shape.
 shape.getReflection().setTransparency(0.37);
 shape.getReflection().setSize(0.48);
 shape.getReflection().setBlur(17.5);
 shape.getReflection().setDistance(9.2);

 doc.save(getArtifactsDir() + "Shape.Reflection.docx");

 doc = new Document(getArtifactsDir() + "Shape.Reflection.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check reflection effect attributes.
 Assert.assertEquals(0.37d, shape.getReflection().getTransparency(), 0.01d);
 Assert.assertEquals(0.48d, shape.getReflection().getSize(), 0.01d);
 Assert.assertEquals(17.5d, shape.getReflection().getBlur(), 0.01d);
 Assert.assertEquals(9.2d, shape.getReflection().getDistance(), 0.01d);

 // Remove reflection effect from the shape.
 shape.getReflection().remove();

 Assert.assertEquals(0, shape.getReflection().getTransparency());
 Assert.assertEquals(0, shape.getReflection().getSize());
 Assert.assertEquals(0, shape.getReflection().getBlur());
 Assert.assertEquals(0, shape.getReflection().getDistance());
 
```

**Returns:**
double - Yansıma etkisine uygulanan bulanıklık derecesini puan cinsinden belirten bir double değer.
### getDistance() {#getDistance}
```
public double getDistance()
```


Yansıtılan görüntünün nesneden ayrılma miktarını puan cinsinden belirten bir double değer döndürür. Varsayılan değer 0.0'dır.

 **Examples:** 

Yansıma şekil etkisiyle nasıl etkileşim kurulacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply reflection effect to the shape.
 shape.getReflection().setTransparency(0.37);
 shape.getReflection().setSize(0.48);
 shape.getReflection().setBlur(17.5);
 shape.getReflection().setDistance(9.2);

 doc.save(getArtifactsDir() + "Shape.Reflection.docx");

 doc = new Document(getArtifactsDir() + "Shape.Reflection.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check reflection effect attributes.
 Assert.assertEquals(0.37d, shape.getReflection().getTransparency(), 0.01d);
 Assert.assertEquals(0.48d, shape.getReflection().getSize(), 0.01d);
 Assert.assertEquals(17.5d, shape.getReflection().getBlur(), 0.01d);
 Assert.assertEquals(9.2d, shape.getReflection().getDistance(), 0.01d);

 // Remove reflection effect from the shape.
 shape.getReflection().remove();

 Assert.assertEquals(0, shape.getReflection().getTransparency());
 Assert.assertEquals(0, shape.getReflection().getSize());
 Assert.assertEquals(0, shape.getReflection().getBlur());
 Assert.assertEquals(0, shape.getReflection().getDistance());
 
```

**Returns:**
double - Yansıtılan görüntünün nesneden ayrılma miktarını puan cinsinden belirten bir double değer.
### getSize() {#getSize}
```
public double getSize()
```


Yansımanın, yansıtılan nesnenin yüzdesi olarak boyutunu temsil eden 0.0 ile 1.0 arasında bir double değer döndürür. Varsayılan değer 0.0'dır.

 **Examples:** 

Yansıma şekil etkisiyle nasıl etkileşim kurulacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply reflection effect to the shape.
 shape.getReflection().setTransparency(0.37);
 shape.getReflection().setSize(0.48);
 shape.getReflection().setBlur(17.5);
 shape.getReflection().setDistance(9.2);

 doc.save(getArtifactsDir() + "Shape.Reflection.docx");

 doc = new Document(getArtifactsDir() + "Shape.Reflection.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check reflection effect attributes.
 Assert.assertEquals(0.37d, shape.getReflection().getTransparency(), 0.01d);
 Assert.assertEquals(0.48d, shape.getReflection().getSize(), 0.01d);
 Assert.assertEquals(17.5d, shape.getReflection().getBlur(), 0.01d);
 Assert.assertEquals(9.2d, shape.getReflection().getDistance(), 0.01d);

 // Remove reflection effect from the shape.
 shape.getReflection().remove();

 Assert.assertEquals(0, shape.getReflection().getTransparency());
 Assert.assertEquals(0, shape.getReflection().getSize());
 Assert.assertEquals(0, shape.getReflection().getBlur());
 Assert.assertEquals(0, shape.getReflection().getDistance());
 
```

**Returns:**
double - Yansımanın, yansıtılan nesnenin yüzdesi olarak boyutunu temsil eden 0.0 ile 1.0 arasında bir double değer.
### getTransparency() {#getTransparency}
```
public double getTransparency()
```


Yansıma etkisinin şeffaflık derecesini temsil eden 0.0 (opak) ile 1.0 (şeffaf) arasında bir double değer döndürür. Varsayılan değer 0.0'dır.

 **Examples:** 

Yansıma şekil etkisiyle nasıl etkileşim kurulacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply reflection effect to the shape.
 shape.getReflection().setTransparency(0.37);
 shape.getReflection().setSize(0.48);
 shape.getReflection().setBlur(17.5);
 shape.getReflection().setDistance(9.2);

 doc.save(getArtifactsDir() + "Shape.Reflection.docx");

 doc = new Document(getArtifactsDir() + "Shape.Reflection.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check reflection effect attributes.
 Assert.assertEquals(0.37d, shape.getReflection().getTransparency(), 0.01d);
 Assert.assertEquals(0.48d, shape.getReflection().getSize(), 0.01d);
 Assert.assertEquals(17.5d, shape.getReflection().getBlur(), 0.01d);
 Assert.assertEquals(9.2d, shape.getReflection().getDistance(), 0.01d);

 // Remove reflection effect from the shape.
 shape.getReflection().remove();

 Assert.assertEquals(0, shape.getReflection().getTransparency());
 Assert.assertEquals(0, shape.getReflection().getSize());
 Assert.assertEquals(0, shape.getReflection().getBlur());
 Assert.assertEquals(0, shape.getReflection().getDistance());
 
```

**Returns:**
double - Yansıma etkisinin şeffaflık derecesini temsil eden 0.0 (opak) ile 1.0 (şeffaf) arasında bir double değer.
### remove() {#remove}
```
public void remove()
```


[ReflectionFormat](../../com.aspose.words/reflectionformat/) öğesini üst nesneden kaldırır.

 **Examples:** 

Yansıma şekil etkisiyle nasıl etkileşim kurulacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply reflection effect to the shape.
 shape.getReflection().setTransparency(0.37);
 shape.getReflection().setSize(0.48);
 shape.getReflection().setBlur(17.5);
 shape.getReflection().setDistance(9.2);

 doc.save(getArtifactsDir() + "Shape.Reflection.docx");

 doc = new Document(getArtifactsDir() + "Shape.Reflection.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check reflection effect attributes.
 Assert.assertEquals(0.37d, shape.getReflection().getTransparency(), 0.01d);
 Assert.assertEquals(0.48d, shape.getReflection().getSize(), 0.01d);
 Assert.assertEquals(17.5d, shape.getReflection().getBlur(), 0.01d);
 Assert.assertEquals(9.2d, shape.getReflection().getDistance(), 0.01d);

 // Remove reflection effect from the shape.
 shape.getReflection().remove();

 Assert.assertEquals(0, shape.getReflection().getTransparency());
 Assert.assertEquals(0, shape.getReflection().getSize());
 Assert.assertEquals(0, shape.getReflection().getBlur());
 Assert.assertEquals(0, shape.getReflection().getDistance());
 
```

### setBlur(double value) {#setBlur-double}
```
public void setBlur(double value)
```


Yansıma etkisine uygulanan bulanıklık derecesini puan cinsinden belirten bir double değer ayarlar. Varsayılan değer 0.0'dır.

 **Examples:** 

Yansıma şekil etkisiyle nasıl etkileşim kurulacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply reflection effect to the shape.
 shape.getReflection().setTransparency(0.37);
 shape.getReflection().setSize(0.48);
 shape.getReflection().setBlur(17.5);
 shape.getReflection().setDistance(9.2);

 doc.save(getArtifactsDir() + "Shape.Reflection.docx");

 doc = new Document(getArtifactsDir() + "Shape.Reflection.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check reflection effect attributes.
 Assert.assertEquals(0.37d, shape.getReflection().getTransparency(), 0.01d);
 Assert.assertEquals(0.48d, shape.getReflection().getSize(), 0.01d);
 Assert.assertEquals(17.5d, shape.getReflection().getBlur(), 0.01d);
 Assert.assertEquals(9.2d, shape.getReflection().getDistance(), 0.01d);

 // Remove reflection effect from the shape.
 shape.getReflection().remove();

 Assert.assertEquals(0, shape.getReflection().getTransparency());
 Assert.assertEquals(0, shape.getReflection().getSize());
 Assert.assertEquals(0, shape.getReflection().getBlur());
 Assert.assertEquals(0, shape.getReflection().getDistance());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Yansıma etkisine uygulanan bulanıklık derecesini puan cinsinden belirten bir double değer. |

### setDistance(double value) {#setDistance-double}
```
public void setDistance(double value)
```


Nokta cinsinden yansıtılan görüntünün nesneden ayrılma miktarını belirten bir çift değer ayarlar. Varsayılan değer 0.0'dır.

 **Examples:** 

Yansıma şekil etkisiyle nasıl etkileşim kurulacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply reflection effect to the shape.
 shape.getReflection().setTransparency(0.37);
 shape.getReflection().setSize(0.48);
 shape.getReflection().setBlur(17.5);
 shape.getReflection().setDistance(9.2);

 doc.save(getArtifactsDir() + "Shape.Reflection.docx");

 doc = new Document(getArtifactsDir() + "Shape.Reflection.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check reflection effect attributes.
 Assert.assertEquals(0.37d, shape.getReflection().getTransparency(), 0.01d);
 Assert.assertEquals(0.48d, shape.getReflection().getSize(), 0.01d);
 Assert.assertEquals(17.5d, shape.getReflection().getBlur(), 0.01d);
 Assert.assertEquals(9.2d, shape.getReflection().getDistance(), 0.01d);

 // Remove reflection effect from the shape.
 shape.getReflection().remove();

 Assert.assertEquals(0, shape.getReflection().getTransparency());
 Assert.assertEquals(0, shape.getReflection().getSize());
 Assert.assertEquals(0, shape.getReflection().getBlur());
 Assert.assertEquals(0, shape.getReflection().getDistance());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Nokta cinsinden yansıtılan görüntünün nesneden ayrılma miktarını belirten bir çift değer. |

### setSize(double value) {#setSize-double}
```
public void setSize(double value)
```


0.0 ile 1.0 arasında bir çift değer ayarlar; bu değer yansımanın yansıtılan nesneye oranı olarak yüzdeyi temsil eder. Varsayılan değer 0.0'dır.

 **Examples:** 

Yansıma şekil etkisiyle nasıl etkileşim kurulacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply reflection effect to the shape.
 shape.getReflection().setTransparency(0.37);
 shape.getReflection().setSize(0.48);
 shape.getReflection().setBlur(17.5);
 shape.getReflection().setDistance(9.2);

 doc.save(getArtifactsDir() + "Shape.Reflection.docx");

 doc = new Document(getArtifactsDir() + "Shape.Reflection.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check reflection effect attributes.
 Assert.assertEquals(0.37d, shape.getReflection().getTransparency(), 0.01d);
 Assert.assertEquals(0.48d, shape.getReflection().getSize(), 0.01d);
 Assert.assertEquals(17.5d, shape.getReflection().getBlur(), 0.01d);
 Assert.assertEquals(9.2d, shape.getReflection().getDistance(), 0.01d);

 // Remove reflection effect from the shape.
 shape.getReflection().remove();

 Assert.assertEquals(0, shape.getReflection().getTransparency());
 Assert.assertEquals(0, shape.getReflection().getSize());
 Assert.assertEquals(0, shape.getReflection().getBlur());
 Assert.assertEquals(0, shape.getReflection().getDistance());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | 0.0 ile 1.0 arasında bir çift değer; bu değer yansımanın yansıtılan nesneye oranı olarak yüzdeyi temsil eder. |

### setTransparency(double value) {#setTransparency-double}
```
public void setTransparency(double value)
```


0.0 (opak) ile 1.0 (şeffaf) arasında bir çift değer ayarlar; bu değer yansıma etkisinin şeffaflık derecesini temsil eder. Varsayılan değer 0.0'dır.

 **Examples:** 

Yansıma şekil etkisiyle nasıl etkileşim kurulacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Various shapes.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Apply reflection effect to the shape.
 shape.getReflection().setTransparency(0.37);
 shape.getReflection().setSize(0.48);
 shape.getReflection().setBlur(17.5);
 shape.getReflection().setDistance(9.2);

 doc.save(getArtifactsDir() + "Shape.Reflection.docx");

 doc = new Document(getArtifactsDir() + "Shape.Reflection.docx");
 shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 // Check reflection effect attributes.
 Assert.assertEquals(0.37d, shape.getReflection().getTransparency(), 0.01d);
 Assert.assertEquals(0.48d, shape.getReflection().getSize(), 0.01d);
 Assert.assertEquals(17.5d, shape.getReflection().getBlur(), 0.01d);
 Assert.assertEquals(9.2d, shape.getReflection().getDistance(), 0.01d);

 // Remove reflection effect from the shape.
 shape.getReflection().remove();

 Assert.assertEquals(0, shape.getReflection().getTransparency());
 Assert.assertEquals(0, shape.getReflection().getSize());
 Assert.assertEquals(0, shape.getReflection().getBlur());
 Assert.assertEquals(0, shape.getReflection().getDistance());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | 0.0 (opak) ile 1.0 (şeffaf) arasında bir çift değer; bu değer yansıma etkisinin şeffaflık derecesini temsil eder. |

