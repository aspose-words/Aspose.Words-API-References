---
title: "AdjustmentCollection"
linktitle: "AdjustmentCollection"
second_title: "Aspose.Words für Java"
description: "Stellt eine schreibgeschützte Sammlung von Adjustment-Anpassungswerten dar, die auf die angegebene Form in Java angewendet werden."
type: docs
weight: 12
url: /de/java/com.aspose.words/adjustmentcollection/
---

**Inheritance:**
java.lang.Object
```
public class AdjustmentCollection
```

Stellt eine schreibgeschützte Sammlung von [Adjustment](../../com.aspose.words/adjustment/) Anpassungswerten dar, die auf die angegebene Form angewendet werden.

 **Examples:** 

Zeigt, wie man mit rohen Anpassungswerten arbeitet.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get(int index)](#get-int) | Gibt eine Anpassung am angegebenen Index zurück. |
| [getCount()](#getCount) | Ermittelt die Anzahl der im Sammelobjekt enthaltenen Elemente. |
### get(int index) {#get-int}
```
public Adjustment get(int index)
```


Gibt eine Anpassung am angegebenen Index zurück.

 **Examples:** 

Zeigt, wie man mit rohen Anpassungswerten arbeitet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int | Ein Index in die Sammlung. |

**Returns:**
[Adjustment](../../com.aspose.words/adjustment/) - An adjustment at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Ermittelt die Anzahl der im Sammelobjekt enthaltenen Elemente.

 **Examples:** 

Zeigt, wie man mit rohen Anpassungswerten arbeitet.

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
int – Die Anzahl der im Sammelobjekt enthaltenen Elemente.
