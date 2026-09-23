---
title: "AdjustmentCollection"
linktitle: "AdjustmentCollection"
second_title: "Aspose.Words pour Java"
description: "Représente une collection en lecture seule des valeurs d'ajustement Adjustment qui sont appliquées à la forme spécifiée en Java."
type: docs
weight: 12
url: /fr/java/com.aspose.words/adjustmentcollection/
---

**Inheritance:**
java.lang.Object
```
public class AdjustmentCollection
```

Représente une collection en lecture seule des valeurs d'[Adjustment](../../com.aspose.words/adjustment/) appliquées à la forme spécifiée.

 **Examples:** 

Montre comment travailler avec les valeurs brutes d'ajustement.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [get(int index)](#get-int) | Renvoie un ajustement à l'index spécifié. |
| [getCount()](#getCount) | Obtient le nombre d'éléments contenus dans la collection. |
### get(int index) {#get-int}
```
public Adjustment get(int index)
```


Renvoie un ajustement à l'index spécifié.

 **Examples:** 

Montre comment travailler avec les valeurs brutes d'ajustement.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| index | int | Un index dans la collection. |

**Returns:**
[Adjustment](../../com.aspose.words/adjustment/) - An adjustment at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Obtient le nombre d'éléments contenus dans la collection.

 **Examples:** 

Montre comment travailler avec les valeurs brutes d'ajustement.

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
int - Le nombre d'éléments contenus dans la collection.
