---
title: "Ajustement"
linktitle: "Ajustement"
second_title: "Aspose.Words pour Java"
description: "Représente les valeurs d’ajustement qui sont appliquées à la forme spécifiée en Java."
type: docs
weight: 11
url: /fr/java/com.aspose.words/adjustment/
---

**Inheritance:**
java.lang.Object
```
public class Adjustment
```

Représente les valeurs d'ajustement appliquées à la forme spécifiée.

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
| [getName()](#getName) | Obtient le nom de l’ajustement. |
| [getValue()](#getValue) | Obtient la valeur brute de l’ajustement. |
| [setValue(int value)](#setValue-int) | Définit la valeur brute de l’ajustement. |
### getName() {#getName}
```
public String getName()
```


Obtient le nom de l’ajustement.

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
java.lang.String - Le nom de l'ajustement.
### getValue() {#getValue}
```
public int getValue()
```


Obtient la valeur brute de l’ajustement.

 **Remarks:** 

Une valeur d'ajustement est simplement un guide qui possède une formule basée sur une valeur spécifiée. Autrement dit, aucun calcul n'est effectué pour un guide de valeur d'ajustement. Au lieu de cela, ce guide spécifie une valeur de paramètre qui est utilisée pour les calculs au sein des guides de forme.

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
int - La valeur brute de l'ajustement.
### setValue(int value) {#setValue-int}
```
public void setValue(int value)
```


Définit la valeur brute de l’ajustement.

 **Remarks:** 

Une valeur d'ajustement est simplement un guide qui possède une formule basée sur une valeur spécifiée. Autrement dit, aucun calcul n'est effectué pour un guide de valeur d'ajustement. Au lieu de cela, ce guide spécifie une valeur de paramètre qui est utilisée pour les calculs au sein des guides de forme.

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
| valeur | int | La valeur brute de l'ajustement. |

