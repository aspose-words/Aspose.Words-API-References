---
title: "AdjustmentCollection"
linktitle: "AdjustmentCollection"
second_title: "Aspose.Words Java için"
description: "Java'da belirtilen şekle uygulanan Adjustment ayar değerlerinden oluşan yalnızca okunabilir bir koleksiyonu temsil eder."
type: docs
weight: 12
url: /tr/java/com.aspose.words/adjustmentcollection/
---

**Inheritance:**
java.lang.Object
```
public class AdjustmentCollection
```

Belirtilen şekle uygulanan [Adjustment](../../com.aspose.words/adjustment/) ayar değerlerinden oluşan salt okunur bir koleksiyonu temsil eder.

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
| [get(int index)](#get-int) | Belirtilen dizindeki bir ayarlamayı döndürür. |
| [getCount()](#getCount) | Koleksiyonda bulunan öğe sayısını alır. |
### get(int index) {#get-int}
```
public Adjustment get(int index)
```


Belirtilen dizindeki bir ayarlamayı döndürür.

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
| indeks | int | Koleksiyona ait bir indeks. |

**Returns:**
[Adjustment](../../com.aspose.words/adjustment/) - An adjustment at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Koleksiyonda bulunan öğe sayısını alır.

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
int - Koleksiyonda bulunan öğe sayısı.
