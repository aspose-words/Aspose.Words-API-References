---
title: "TableStyleOptions"
linktitle: "TableStyleOptions"
second_title: "Aspose.Words pour Java"
description: "Spécifie comment le style de tableau est appliqué à un tableau en Java."
type: docs
weight: 661
url: /fr/java/com.aspose.words/tablestyleoptions/
---

**Inheritance:**
java.lang.Object
```
public class TableStyleOptions
```

Spécifie comment le style de tableau est appliqué à un tableau.

 **Examples:** 

Montre comment créer un nouveau tableau tout en appliquant un style.

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
## Champs

| Champ | Description |
| --- | --- |
| [COLUMN_BANDS](#COLUMN-BANDS) | Appliquer le formatage conditionnel de bandes de colonnes. |
| [DEFAULT](#DEFAULT) | Il s'agit des paramètres par défaut de Microsoft Word. |
| [DEFAULT_2003](#DEFAULT-2003) | Le banding des lignes et des colonnes est appliqué. |
| [FIRST_COLUMN](#FIRST-COLUMN) | Appliquer le formatage conditionnel de la première colonne. |
| [FIRST_ROW](#FIRST-ROW) | Appliquer le formatage conditionnel de la première ligne. |
| [LAST_COLUMN](#LAST-COLUMN) | Appliquer le formatage conditionnel de la dernière colonne. |
| [LAST_ROW](#LAST-ROW) | Appliquer le formatage conditionnel de la dernière ligne. |
| [NONE](#NONE) | Aucun formatage de style de tableau n'est appliqué. |
| [ROW_BANDS](#ROW-BANDS) | Appliquer le formatage conditionnel de bandes de lignes. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
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


Appliquer le formatage conditionnel de bandes de colonnes.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Il s'agit des paramètres par défaut de Microsoft Word.

### DEFAULT_2003 {#DEFAULT-2003}
```
public static int DEFAULT_2003
```


Le banding des lignes et des colonnes est appliqué. Il s'agit du paramètre par défaut de Microsoft Word pour les anciens formats tels que DOC, WML et RTF.

### FIRST_COLUMN {#FIRST-COLUMN}
```
public static int FIRST_COLUMN
```


Appliquer le formatage conditionnel de la première colonne.

### FIRST_ROW {#FIRST-ROW}
```
public static int FIRST_ROW
```


Appliquer le formatage conditionnel de la première ligne.

### LAST_COLUMN {#LAST-COLUMN}
```
public static int LAST_COLUMN
```


Appliquer le formatage conditionnel de la dernière colonne.

### LAST_ROW {#LAST-ROW}
```
public static int LAST_ROW
```


Appliquer le formatage conditionnel de la dernière ligne.

### NONE {#NONE}
```
public static int NONE
```


Aucun formatage de style de tableau n'est appliqué.

### ROW_BANDS {#ROW-BANDS}
```
public static int ROW_BANDS
```


Appliquer le formatage conditionnel de bandes de lignes.

### length {#length}
```
public static int length
```


### fromName(String tableStyleOptionsName) {#fromName-java.lang.String}
```
public static int fromName(String tableStyleOptionsName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| tableStyleOptionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set tableStyleOptionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set tableStyleOptionsNames)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| tableStyleOptionsNames | java.util.Set |  |

**Returns:**
int
### getName(int tableStyleOptions) {#getName-int}
```
public static String getName(int tableStyleOptions)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| tableStyleOptions | int |  |

**Returns:**
java.lang.String
### getNames(int tableStyleOptions) {#getNames-int}
```
public static Set getNames(int tableStyleOptions)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| tableStyleOptions | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
