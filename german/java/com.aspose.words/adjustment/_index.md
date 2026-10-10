---
title: "Adjustment"
linktitle: "Adjustment"
second_title: "Aspose.Words für Java"
description: "Stellt Anpassungswerte dar, die auf die angegebene Form in Java angewendet werden."
type: docs
weight: 11
url: /de/java/com.aspose.words/adjustment/
---

**Inheritance:**
java.lang.Object
```
public class Adjustment
```

Stellt Anpassungswerte dar, die auf die angegebene Form angewendet werden.

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
| [getName()](#getName) | Ermittelt den Namen der Anpassung. |
| [getValue()](#getValue) | Ermittelt den Rohwert der Anpassung. |
| [setValue(int value)](#setValue-int) | Setzt den Rohwert der Anpassung. |
### getName() {#getName}
```
public String getName()
```


Ermittelt den Namen der Anpassung.

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
java.lang.String - Der Name der Anpassung.
### getValue() {#getValue}
```
public int getValue()
```


Ermittelt den Rohwert der Anpassung.

 **Remarks:** 

Ein Anpassungswert ist einfach ein Leitfaden, für den eine wertbasierte Formel angegeben ist. Das heißt, für einen Anpassungswert‑Leitfaden findet keine Berechnung statt. Stattdessen gibt dieser Leitfaden einen Parameterwert an, der für Berechnungen innerhalb der Form‑Leitfäden verwendet wird.

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
int - Der Rohwert der Anpassung.
### setValue(int value) {#setValue-int}
```
public void setValue(int value)
```


Setzt den Rohwert der Anpassung.

 **Remarks:** 

Ein Anpassungswert ist einfach ein Leitfaden, für den eine wertbasierte Formel angegeben ist. Das heißt, für einen Anpassungswert‑Leitfaden findet keine Berechnung statt. Stattdessen gibt dieser Leitfaden einen Parameterwert an, der für Berechnungen innerhalb der Form‑Leitfäden verwendet wird.

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
| Wert | int | Der Rohwert der Anpassung. |

