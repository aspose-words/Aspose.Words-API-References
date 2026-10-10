---
title: "Ayarlama"
linktitle: "Ayarlama"
second_title: "Aspose.Words Java için"
description: "Belirtilen şekle Java'da uygulanan ayarlama değerlerini temsil eder."
type: docs
weight: 11
url: /tr/java/com.aspose.words/adjustment/
---

**Inheritance:**
java.lang.Object
```
public class Adjustment
```

Belirtilen şekle uygulanan ayar değerlerini temsil eder.

 **Examples:** 

Ayarlama ham değerleriyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Rounded rectangle shape.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 AdjustmentCollection adjustments = shape.getAdjustments();
 Assert.assertEquals(1, adjustments.getCount());

 Adjustment adjustment = adjustments.get(0);
 Assert.assertEquals("adj", adjustment.getName());
 Assert.assertEquals(16667, adjustment.getValue());

 adjustment.setValue(30000);

 doc.save(getArtifactsDir() + "Shape.Adjustments.docx");
 
```
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getName()](#getName) | Ayarlamanın adını alır. |
| [getValue()](#getValue) | Ayarlamanın ham değerini alır. |
| [setValue(int value)](#setValue-int) | Ayarlamanın ham değerini ayarlar. |
### getName() {#getName}
```
public String getName()
```


Ayarlamanın adını alır.

 **Examples:** 

Ayarlama ham değerleriyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Rounded rectangle shape.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 AdjustmentCollection adjustments = shape.getAdjustments();
 Assert.assertEquals(1, adjustments.getCount());

 Adjustment adjustment = adjustments.get(0);
 Assert.assertEquals("adj", adjustment.getName());
 Assert.assertEquals(16667, adjustment.getValue());

 adjustment.setValue(30000);

 doc.save(getArtifactsDir() + "Shape.Adjustments.docx");
 
```

**Returns:**
java.lang.String - Ayarlamanın adı.
### getValue() {#getValue}
```
public int getValue()
```


Ayarlamanın ham değerini alır.

 **Remarks:** 

Bir ayar değeri, yalnızca bir değer tabanlı formül belirtilmiş bir kılavuzdur. Yani, bir ayar değeri kılavuzu için herhangi bir hesaplama yapılmaz. Bunun yerine, bu kılavuz, şekil kılavuzları içinde yapılan hesaplamalarda kullanılan bir parametre değerini belirtir.

 **Examples:** 

Ayarlama ham değerleriyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Rounded rectangle shape.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 AdjustmentCollection adjustments = shape.getAdjustments();
 Assert.assertEquals(1, adjustments.getCount());

 Adjustment adjustment = adjustments.get(0);
 Assert.assertEquals("adj", adjustment.getName());
 Assert.assertEquals(16667, adjustment.getValue());

 adjustment.setValue(30000);

 doc.save(getArtifactsDir() + "Shape.Adjustments.docx");
 
```

**Returns:**
int - Ayarlamanın ham değeri.
### setValue(int value) {#setValue-int}
```
public void setValue(int value)
```


Ayarlamanın ham değerini ayarlar.

 **Remarks:** 

Bir ayar değeri, yalnızca bir değer tabanlı formül belirtilmiş bir kılavuzdur. Yani, bir ayar değeri kılavuzu için herhangi bir hesaplama yapılmaz. Bunun yerine, bu kılavuz, şekil kılavuzları içinde yapılan hesaplamalarda kullanılan bir parametre değerini belirtir.

 **Examples:** 

Ayarlama ham değerleriyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Rounded rectangle shape.docx");
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);

 AdjustmentCollection adjustments = shape.getAdjustments();
 Assert.assertEquals(1, adjustments.getCount());

 Adjustment adjustment = adjustments.get(0);
 Assert.assertEquals("adj", adjustment.getName());
 Assert.assertEquals(16667, adjustment.getValue());

 adjustment.setValue(30000);

 doc.save(getArtifactsDir() + "Shape.Adjustments.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Ayarlamanın ham değeri. |

