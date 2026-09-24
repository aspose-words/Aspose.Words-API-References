---
title: "Ajuste"
linktitle: "Ajuste"
second_title: "Aspose.Words para Java"
description: "Representa los valores de ajuste que se aplican a la forma especificada en Java."
type: docs
weight: 11
url: /es/java/com.aspose.words/adjustment/
---

**Inheritance:**
java.lang.Object
```
public class Adjustment
```

Representa valores de ajuste que se aplican a la forma especificada.

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
| [getName()](#getName) | Obtiene el nombre del ajuste. |
| [getValue()](#getValue) | Obtiene el valor bruto del ajuste. |
| [setValue(int value)](#setValue-int) | Establece el valor bruto del ajuste. |
### getName() {#getName}
```
public String getName()
```


Obtiene el nombre del ajuste.

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
java.lang.String - El nombre del ajuste.
### getValue() {#getValue}
```
public int getValue()
```


Obtiene el valor bruto del ajuste.

 **Remarks:** 

Un valor de ajuste es simplemente una guía que tiene una fórmula basada en valores especificada. Es decir, no se realiza ningún cálculo para una guía de valor de ajuste. En su lugar, esta guía especifica un valor de parámetro que se utiliza para cálculos dentro de las guías de forma.

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
int - El valor bruto del ajuste.
### setValue(int value) {#setValue-int}
```
public void setValue(int value)
```


Establece el valor bruto del ajuste.

 **Remarks:** 

Un valor de ajuste es simplemente una guía que tiene una fórmula basada en valores especificada. Es decir, no se realiza ningún cálculo para una guía de valor de ajuste. En su lugar, esta guía especifica un valor de parámetro que se utiliza para cálculos dentro de las guías de forma.

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
| valor | int | El valor bruto del ajuste. |

