---
title: "PreferredWidthType"
linktitle: "PreferredWidthType"
second_title: "Aspose.Words para Java"
description: "Especifica la unidad de medida para el ancho preferido de una tabla o celda en Java."
type: docs
weight: 551
url: /es/java/com.aspose.words/preferredwidthtype/
---

**Inheritance:**
java.lang.Object
```
public class PreferredWidthType
```

Especifica la unidad de medida para el ancho preferido de una tabla o celda.

 **Examples:** 

Muestra cómo verificar el tipo y el valor del ancho preferido de una celda de tabla.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 Table table = doc.getFirstSection().getBody().getTables().get(0);
 Cell firstCell = table.getFirstRow().getFirstCell();

 Assert.assertEquals(PreferredWidthType.PERCENT, firstCell.getCellFormat().getPreferredWidth().getType());
 Assert.assertEquals(11.16d, firstCell.getCellFormat().getPreferredWidth().getValue());
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [AUTO](#AUTO) | El ancho preferido no está especificado. |
| [PERCENT](#PERCENT) | Mide el ancho actual del elemento usando un porcentaje especificado. |
| [POINTS](#POINTS) | Mide el ancho actual del elemento usando un número especificado de puntos (1/72 de pulgada). |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String preferredWidthTypeName)](#fromName-java.lang.String) |  |
| [getName(int preferredWidthType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int preferredWidthType)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


El ancho preferido no está especificado. El ancho real de la tabla o celda se especifica mediante el ancho explícito o se determinará automáticamente por el algoritmo de diseño de tabla cuando se muestre la tabla, según la configuración de ajuste automático de la tabla.

### PERCENT {#PERCENT}
```
public static int PERCENT
```


Mide el ancho actual del elemento usando un porcentaje especificado.

### POINTS {#POINTS}
```
public static int POINTS
```


Mide el ancho actual del elemento usando un número especificado de puntos (1/72 de pulgada).

### length {#length}
```
public static int length
```


### fromName(String preferredWidthTypeName) {#fromName-java.lang.String}
```
public static int fromName(String preferredWidthTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| preferredWidthTypeName | java.lang.String |  |

**Returns:**
int
### getName(int preferredWidthType) {#getName-int}
```
public static String getName(int preferredWidthType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| preferredWidthType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int preferredWidthType) {#toString-int}
```
public static String toString(int preferredWidthType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| preferredWidthType | int |  |

**Returns:**
java.lang.String
