---
title: "TableStyleOptions"
linktitle: "TableStyleOptions"
second_title: "Aspose.Words para Java"
description: "Especifica cómo se aplica el estilo de tabla a una tabla en Java."
type: docs
weight: 661
url: /es/java/com.aspose.words/tablestyleoptions/
---

**Inheritance:**
java.lang.Object
```
public class TableStyleOptions
```

Especifica cómo se aplica el estilo de tabla a una tabla.

 **Examples:** 

Muestra cómo crear una tabla nueva mientras se aplica un estilo.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // We must insert at least one row before setting any table formatting.
 builder.insertCell();

 // Set the table style used based on the style identifier.
 // Note that not all table styles are available when saving to .doc format.
 table.setStyleIdentifier(StyleIdentifier.MEDIUM_SHADING_1_ACCENT_1);

 // Partially apply the style to features of the table based on predicates, then build the table.
 table.setStyleOptions(TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS | TableStyleOptions.FIRST_ROW);
 table.autoFit(AutoFitBehavior.AUTO_FIT_TO_CONTENTS);

 builder.writeln("Item");
 builder.getCellFormat().setRightPadding(40.0);
 builder.insertCell();
 builder.writeln("Quantity (kg)");
 builder.endRow();

 builder.insertCell();
 builder.writeln("Apples");
 builder.insertCell();
 builder.writeln("20");
 builder.endRow();

 builder.insertCell();
 builder.writeln("Bananas");
 builder.insertCell();
 builder.writeln("40");
 builder.endRow();

 builder.insertCell();
 builder.writeln("Carrots");
 builder.insertCell();
 builder.writeln("50");
 builder.endRow();

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTableWithStyle.docx");
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [COLUMN_BANDS](#COLUMN-BANDS) | Aplicar formato condicional de banding de columnas. |
| [DEFAULT](#DEFAULT) | Esto es la configuración predeterminada de Microsoft Word. |
| [DEFAULT_2003](#DEFAULT-2003) | Se aplica el banding de filas y columnas. |
| [FIRST_COLUMN](#FIRST-COLUMN) | Aplicar formato condicional a la primera columna. |
| [FIRST_ROW](#FIRST-ROW) | Aplicar formato condicional a la primera fila. |
| [LAST_COLUMN](#LAST-COLUMN) | Aplicar formato condicional a la última columna. |
| [LAST_ROW](#LAST-ROW) | Aplicar formato condicional a la última fila. |
| [NONE](#NONE) | No se aplica formato de estilo de tabla. |
| [ROW_BANDS](#ROW-BANDS) | Aplicar formato condicional de banding de filas. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String tableStyleOptionsName)](#fromName-java.lang.String) |  |
| [fromNames(Set tableStyleOptionsNames)](#fromNames-java.util.Set) |  |
| [getName(int tableStyleOptions)](#getName-int) |  |
| [getNames(int tableStyleOptions)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int tableStyleOptions)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### COLUMN_BANDS {#COLUMN-BANDS}
```
public static int COLUMN_BANDS
```


Aplicar formato condicional de banding de columnas.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Esto es la configuración predeterminada de Microsoft Word.

### DEFAULT_2003 {#DEFAULT-2003}
```
public static int DEFAULT_2003
```


Se aplica el banding de filas y columnas. Este es el valor predeterminado de Microsoft Word para formatos antiguos como DOC, WML y RTF.

### FIRST_COLUMN {#FIRST-COLUMN}
```
public static int FIRST_COLUMN
```


Aplicar formato condicional a la primera columna.

### FIRST_ROW {#FIRST-ROW}
```
public static int FIRST_ROW
```


Aplicar formato condicional a la primera fila.

### LAST_COLUMN {#LAST-COLUMN}
```
public static int LAST_COLUMN
```


Aplicar formato condicional a la última columna.

### LAST_ROW {#LAST-ROW}
```
public static int LAST_ROW
```


Aplicar formato condicional a la última fila.

### NONE {#NONE}
```
public static int NONE
```


No se aplica formato de estilo de tabla.

### ROW_BANDS {#ROW-BANDS}
```
public static int ROW_BANDS
```


Aplicar formato condicional de banding de filas.

### length {#length}
```
public static int length
```


### fromName(String tableStyleOptionsName) {#fromName-java.lang.String}
```
public static int fromName(String tableStyleOptionsName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tableStyleOptionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set tableStyleOptionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set tableStyleOptionsNames)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tableStyleOptionsNames | java.util.Set |  |

**Returns:**
int
### getName(int tableStyleOptions) {#getName-int}
```
public static String getName(int tableStyleOptions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tableStyleOptions | int |  |

**Returns:**
java.lang.String
### getNames(int tableStyleOptions) {#getNames-int}
```
public static Set getNames(int tableStyleOptions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tableStyleOptions | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int tableStyleOptions) {#toString-int}
```
public static String toString(int tableStyleOptions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| tableStyleOptions | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
