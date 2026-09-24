---
title: "HeightRule"
linktitle: "HeightRule"
second_title: "Aspose.Words para Java"
description: "Especifica la regla para determinar la altura de un objeto en Java."
type: docs
weight: 373
url: /es/java/com.aspose.words/heightrule/
---

**Inheritance:**
java.lang.Object
```
public class HeightRule
```

Especifica la regla para determinar la altura de un objeto.

 **Examples:** 

Muestra cómo formatear filas con un document builder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Row 1, cell 1.");

 // Start a second row, and then configure its height. The builder will apply these settings to
 // its current row, as well as any new rows it creates afterwards.
 builder.endRow();

 RowFormat rowFormat = builder.getRowFormat();
 rowFormat.setHeight(100.0);
 rowFormat.setHeightRule(HeightRule.EXACTLY);

 builder.insertCell();
 builder.write("Row 2, cell 1.");
 builder.endTable();

 // The first row was unaffected by the padding reconfiguration and still holds the default values.
 Assert.assertEquals(0.0d, table.getRows().get(0).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.AUTO, table.getRows().get(0).getRowFormat().getHeightRule());

 Assert.assertEquals(100.0d, table.getRows().get(1).getRowFormat().getHeight());
 Assert.assertEquals(HeightRule.EXACTLY, table.getRows().get(1).getRowFormat().getHeightRule());

 doc.save(getArtifactsDir() + "DocumentBuilder.SetRowFormatting.docx");
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [AT_LEAST](#AT-LEAST) | La altura será al menos la altura especificada en puntos. |
| [AUTO](#AUTO) | La altura crecerá automáticamente para acomodar todo el texto dentro de un objeto. |
| [EXACTLY](#EXACTLY) | La altura se especifica exactamente en puntos. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String heightRuleName)](#fromName-java.lang.String) |  |
| [getName(int heightRule)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int heightRule)](#toString-int) |  |
### AT_LEAST {#AT-LEAST}
```
public static int AT_LEAST
```


La altura será al menos la altura especificada en puntos. Crecerá, si es necesario, para acomodar todo el texto dentro de un objeto.

### AUTO {#AUTO}
```
public static int AUTO
```


La altura crecerá automáticamente para acomodar todo el texto dentro de un objeto.

### EXACTLY {#EXACTLY}
```
public static int EXACTLY
```


La altura se especifica exactamente en puntos. Tenga en cuenta que si el texto no cabe dentro del objeto con esta altura, aparecerá truncado.

### length {#length}
```
public static int length
```


### fromName(String heightRuleName) {#fromName-java.lang.String}
```
public static int fromName(String heightRuleName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| heightRuleName | java.lang.String |  |

**Returns:**
int
### getName(int heightRule) {#getName-int}
```
public static String getName(int heightRule)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| heightRule | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int heightRule) {#toString-int}
```
public static String toString(int heightRule)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| heightRule | int |  |

**Returns:**
java.lang.String
