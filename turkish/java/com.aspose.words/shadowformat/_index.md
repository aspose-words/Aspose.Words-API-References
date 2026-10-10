---
title: "ShadowFormat"
linktitle: "ShadowFormat"
second_title: "Aspose.Words Java için"
description: "Java'da bir nesne için gölge biçimlendirmesini temsil eder."
type: docs
weight: 610
url: /tr/java/com.aspose.words/shadowformat/
---

**Inheritance:**
java.lang.Object
```
public class ShadowFormat
```

Bir nesne için gölge biçimlendirmesini temsil eder.

Daha fazla bilgi için, [ Working with Graphic Elements ][Working with Graphic Elements] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Gölge rengini almayı gösterir.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```


[Working with Graphic Elements]: https://docs.aspose.com/words/java/working-with-graphic-elements/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [clear()](#clear) | Gölge biçimini temizler. |
| [getColor()](#getColor) | Gölge rengi temsil eden bir java.awt.Color nesnesi alır. |
| [getTransparency()](#getTransparency) | Gölge etkisinin şeffaflık derecesini 0.0 (opak) ile 1.0 (şeffaf) arasında bir değer olarak alır. |
| [getType()](#getType) | ShadowFormat için belirtilen [ShadowType](../../com.aspose.words/shadowtype/) alır. |
| [getVisible()](#getVisible) | Bu örneğe uygulanan biçimlendirme görünürse  true  döndürür. |
| [setColor(Color value)](#setColor-java.awt.Color) | Gölge için rengi temsil eden bir java.awt.Color nesnesi ayarlar. |
| [setTransparency(double value)](#setTransparency-double) | Gölge etkisi için şeffaflık derecesini 0.0 (opak) ile 1.0 (şeffaf) arasında bir değer olarak ayarlar. |
| [setType(int value)](#setType-int) | ShadowFormat için belirtilen [ShadowType](../../com.aspose.words/shadowtype/) ayarlar. |
### clear() {#clear}
```
public void clear()
```


Gölge biçimini temizler.

 **Examples:** 

Şekil için gölge biçimlendirmesiyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Shape stroke pattern border.docx");
 Shape shape = (Shape)doc.getChildNodes(NodeType.SHAPE, true).get(0);

 if (shape.getShadowFormat().getVisible() && shape.getShadowFormat().getType() == ShadowType.SHADOW_2)
     shape.getShadowFormat().setType(ShadowType.SHADOW_7);

 if (shape.getShadowFormat().getType() == ShadowType.SHADOW_MIXED)
     shape.getShadowFormat().clear();
 
```

### getColor() {#getColor}
```
public Color getColor()
```


Gölge için rengi temsil eden bir java.awt.Color nesnesi alır. Varsayılan değer java.awt.Color\#getBlack().getBlack().

 **Examples:** 

Gölge rengini almayı gösterir.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```

Şeffaflık ile bir rengi nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 ShadowFormat shadowFormat = shape.getShadowFormat();
 shadowFormat.setType(ShadowType.SHADOW_21);
 shadowFormat.setColor(Color.RED);
 shadowFormat.setTransparency(0.8);

 doc.save(getArtifactsDir() + "Shape.ShadowFormatTransparency.docx");
 
```

**Returns:**
java.awt.Color - Gölge için rengi temsil eden bir java.awt.Color nesnesi.
### getTransparency() {#getTransparency}
```
public double getTransparency()
```


Gölge etkisi için şeffaflık derecesini 0.0 (opak) ile 1.0 (şeffaf) arasında bir değer olarak alır. Varsayılan değer 0.0.

 **Examples:** 

Şeffaflık ile bir rengi nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 ShadowFormat shadowFormat = shape.getShadowFormat();
 shadowFormat.setType(ShadowType.SHADOW_21);
 shadowFormat.setColor(Color.RED);
 shadowFormat.setTransparency(0.8);

 doc.save(getArtifactsDir() + "Shape.ShadowFormatTransparency.docx");
 
```

**Returns:**
double - Gölge etkisi için şeffaflık derecesi, 0.0 (opak) ile 1.0 (şeffaf) arasında bir değer.
### getType() {#getType}
```
public int getType()
```


ShadowFormat için belirtilen [ShadowType](../../com.aspose.words/shadowtype/) alır.

 **Remarks:** 

Yeni bir gölge türü ayarlamak, Renk ve Şeffaflık değerlerini varsayılanlarına sıfırlar. Bu nedenle, önce istenen gölge türünü ayarlamak ve ardından Renk ve Şeffaflık değerlerini ayarlamak mantıklıdır.

 **Examples:** 

Gölge rengini almayı gösterir.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```

**Returns:**
int - ShadowFormat için belirtilen [ShadowType](../../com.aspose.words/shadowtype/). Döndürülen değer [ShadowType](../../com.aspose.words/shadowtype/) sabitlerinden biridir.
### getVisible() {#getVisible}
```
public boolean getVisible()
```


Bu örneğe uygulanan biçimlendirme görünürse  true  döndürür.

 **Remarks:** 

[clear()](../../com.aspose.words/shadowformat/\#clear) aksine, Visible özelliğine  false  atamak biçimlendirmeyi temizlemez, yalnızca şekil etkisini gizler.

 **Examples:** 

Şekil için gölge biçimlendirmesiyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Shape stroke pattern border.docx");
 Shape shape = (Shape)doc.getChildNodes(NodeType.SHAPE, true).get(0);

 if (shape.getShadowFormat().getVisible() && shape.getShadowFormat().getType() == ShadowType.SHADOW_2)
     shape.getShadowFormat().setType(ShadowType.SHADOW_7);

 if (shape.getShadowFormat().getType() == ShadowType.SHADOW_MIXED)
     shape.getShadowFormat().clear();
 
```

**Returns:**
boolean -  true  bu örneğe uygulanan biçimlendirme görünürse.
### setColor(Color value) {#setColor-java.awt.Color}
```
public void setColor(Color value)
```


Gölge için rengi temsil eden bir java.awt.Color nesnesi ayarlar. Varsayılan değer java.awt.Color\#getBlack().getBlack().

 **Examples:** 

Gölge rengini almayı gösterir.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```

Şeffaflık ile bir rengi nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 ShadowFormat shadowFormat = shape.getShadowFormat();
 shadowFormat.setType(ShadowType.SHADOW_21);
 shadowFormat.setColor(Color.RED);
 shadowFormat.setTransparency(0.8);

 doc.save(getArtifactsDir() + "Shape.ShadowFormatTransparency.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.awt.Color | Gölge için rengi temsil eden bir java.awt.Color nesnesi. |

### setTransparency(double value) {#setTransparency-double}
```
public void setTransparency(double value)
```


Gölge etkisi için şeffaflık derecesini 0.0 (opak) ile 1.0 (şeffaf) arasında bir değer olarak ayarlar. Varsayılan değer 0.0.

 **Examples:** 

Şeffaflık ile bir rengi nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 ShadowFormat shadowFormat = shape.getShadowFormat();
 shadowFormat.setType(ShadowType.SHADOW_21);
 shadowFormat.setColor(Color.RED);
 shadowFormat.setTransparency(0.8);

 doc.save(getArtifactsDir() + "Shape.ShadowFormatTransparency.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Gölge etkisi için şeffaflık derecesi, 0.0 (opak) ile 1.0 (şeffaf) arasında bir değer. |

### setType(int value) {#setType-int}
```
public void setType(int value)
```


ShadowFormat için belirtilen [ShadowType](../../com.aspose.words/shadowtype/) ayarlar.

 **Remarks:** 

Yeni bir gölge türü ayarlamak, Renk ve Şeffaflık değerlerini varsayılanlarına sıfırlar. Bu nedenle, önce istenen gölge türünü ayarlamak ve ardından Renk ve Şeffaflık değerlerini ayarlamak mantıklıdır.

 **Examples:** 

Gölge rengini almayı gösterir.

```

 Document doc = new Document(getMyDir() + "Shadow color.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShadowFormat shadowFormat = shape.getShadowFormat();

 Assert.assertEquals(Color.RED.getRGB(), shadowFormat.getColor().getRGB());
 Assert.assertEquals(ShadowType.SHADOW_MIXED, shadowFormat.getType());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | ShadowFormat için belirtilen [ShadowType](../../com.aspose.words/shadowtype/). Değer, [ShadowType](../../com.aspose.words/shadowtype/) sabitlerinden biri olmalıdır. |

