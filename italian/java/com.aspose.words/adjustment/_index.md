---
title: "Regolazione"
linktitle: "Regolazione"
second_title: "Aspose.Words per Java"
description: "Rappresenta i valori di regolazione che vengono applicati alla forma specificata in Java."
type: docs
weight: 11
url: /it/java/com.aspose.words/adjustment/
---

**Inheritance:**
java.lang.Object
```
public class Adjustment
```

Rappresenta i valori di regolazione applicati alla forma specificata.

 **Examples:** 

Mostra come lavorare con i valori grezzi di regolazione.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [getName()](#getName) | Ottiene il nome della regolazione. |
| [getValue()](#getValue) | Ottiene il valore grezzo della regolazione. |
| [setValue(int value)](#setValue-int) | Imposta il valore grezzo della regolazione. |
### getName() {#getName}
```
public String getName()
```


Ottiene il nome della regolazione.

 **Examples:** 

Mostra come lavorare con i valori grezzi di regolazione.

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
java.lang.String - Il nome della regolazione.
### getValue() {#getValue}
```
public int getValue()
```


Ottiene il valore grezzo della regolazione.

 **Remarks:** 

Un valore di regolazione è semplicemente una guida che ha una formula basata su valore specificata. Cioè, non viene eseguito alcun calcolo per una guida di valore di regolazione. Invece, questa guida specifica un valore di parametro che viene utilizzato per i calcoli all'interno delle guide di forma.

 **Examples:** 

Mostra come lavorare con i valori grezzi di regolazione.

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
int - Il valore grezzo della regolazione.
### setValue(int value) {#setValue-int}
```
public void setValue(int value)
```


Imposta il valore grezzo della regolazione.

 **Remarks:** 

Un valore di regolazione è semplicemente una guida che ha una formula basata su valore specificata. Cioè, non viene eseguito alcun calcolo per una guida di valore di regolazione. Invece, questa guida specifica un valore di parametro che viene utilizzato per i calcoli all'interno delle guide di forma.

 **Examples:** 

Mostra come lavorare con i valori grezzi di regolazione.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| valore | int | Il valore grezzo della regolazione. |

