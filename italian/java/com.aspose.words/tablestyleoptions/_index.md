---
title: "TableStyleOptions"
linktitle: "TableStyleOptions"
second_title: "Aspose.Words per Java"
description: "Specifica come lo stile della tabella viene applicato a una tabella in Java."
type: docs
weight: 661
url: /it/java/com.aspose.words/tablestyleoptions/
---

**Inheritance:**
java.lang.Object
```
public class TableStyleOptions
```

Specifica come lo stile di tabella viene applicato a una tabella.

 **Examples:** 

Mostra come creare una nuova tabella applicando uno stile.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [COLUMN_BANDS](#COLUMN-BANDS) | Applica la formattazione condizionale a bande di colonna. |
| [DEFAULT](#DEFAULT) | Queste sono le impostazioni predefinite di Microsoft Word. |
| [DEFAULT_2003](#DEFAULT-2003) | Le bande di riga e colonna sono applicate. |
| [FIRST_COLUMN](#FIRST-COLUMN) | Applica la formattazione condizionale alla prima colonna. |
| [FIRST_ROW](#FIRST-ROW) | Applica la formattazione condizionale alla prima riga. |
| [LAST_COLUMN](#LAST-COLUMN) | Applica la formattazione condizionale all'ultima colonna. |
| [LAST_ROW](#LAST-ROW) | Applica la formattazione condizionale all'ultima riga. |
| [NONE](#NONE) | Nessuna formattazione di stile della tabella è applicata. |
| [ROW_BANDS](#ROW-BANDS) | Applica la formattazione condizionale a bande di riga. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
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


Applica la formattazione condizionale a bande di colonna.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Queste sono le impostazioni predefinite di Microsoft Word.

### DEFAULT_2003 {#DEFAULT-2003}
```
public static int DEFAULT_2003
```


Le bande di riga e colonna sono applicate. Questa è l'impostazione predefinita di Microsoft Word per i formati vecchi come DOC, WML e RTF.

### FIRST_COLUMN {#FIRST-COLUMN}
```
public static int FIRST_COLUMN
```


Applica la formattazione condizionale alla prima colonna.

### FIRST_ROW {#FIRST-ROW}
```
public static int FIRST_ROW
```


Applica la formattazione condizionale alla prima riga.

### LAST_COLUMN {#LAST-COLUMN}
```
public static int LAST_COLUMN
```


Applica la formattazione condizionale all'ultima colonna.

### LAST_ROW {#LAST-ROW}
```
public static int LAST_ROW
```


Applica la formattazione condizionale all'ultima riga.

### NONE {#NONE}
```
public static int NONE
```


Nessuna formattazione di stile della tabella è applicata.

### ROW_BANDS {#ROW-BANDS}
```
public static int ROW_BANDS
```


Applica la formattazione condizionale a bande di riga.

### length {#length}
```
public static int length
```


### fromName(String tableStyleOptionsName) {#fromName-java.lang.String}
```
public static int fromName(String tableStyleOptionsName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tableStyleOptionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set tableStyleOptionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set tableStyleOptionsNames)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tableStyleOptionsNames | java.util.Set |  |

**Returns:**
int
### getName(int tableStyleOptions) {#getName-int}
```
public static String getName(int tableStyleOptions)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tableStyleOptions | int |  |

**Returns:**
java.lang.String
### getNames(int tableStyleOptions) {#getNames-int}
```
public static Set getNames(int tableStyleOptions)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| tableStyleOptions | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
