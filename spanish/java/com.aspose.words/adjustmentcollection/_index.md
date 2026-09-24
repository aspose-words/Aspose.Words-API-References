---
title: "AdjustmentCollection"
linktitle: "AdjustmentCollection"
second_title: "Aspose.Words para Java"
description: "Representa una colección de solo lectura de valores de ajuste Adjustment que se aplican a la forma especificada en Java."
type: docs
weight: 12
url: /es/java/com.aspose.words/adjustmentcollection/
---

**Inheritance:**
java.lang.Object
```
public class AdjustmentCollection
```

Representa una colección de solo lectura de [Adjustment](../../com.aspose.words/adjustment/) valores de ajuste que se aplican a la forma especificada.

 **Examples:** 

Muestra cómo trabajar con valores brutos de ajuste.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [get(int index)](#get-int) | Devuelve un ajuste en el índice especificado. |
| [getCount()](#getCount) | Obtiene el número de elementos contenidos en la colección. |
### get(int index) {#get-int}
```
public Adjustment get(int index)
```


Devuelve un ajuste en el índice especificado.

 **Examples:** 

Muestra cómo trabajar con valores brutos de ajuste.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| índice | int | Un índice en la colección. |

**Returns:**
[Adjustment](../../com.aspose.words/adjustment/) - An adjustment at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Obtiene el número de elementos contenidos en la colección.

 **Examples:** 

Muestra cómo trabajar con valores brutos de ajuste.

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
int - El número de elementos contenidos en la colección.
