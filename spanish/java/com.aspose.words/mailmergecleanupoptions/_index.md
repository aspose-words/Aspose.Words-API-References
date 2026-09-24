---
title: "MailMergeCleanupOptions"
linktitle: "MailMergeCleanupOptions"
second_title: "Aspose.Words para Java"
description: "Especifica opciones que determinan qué elementos se eliminan durante la combinación de correspondencia en Java."
type: docs
weight: 438
url: /es/java/com.aspose.words/mailmergecleanupoptions/
---

**Inheritance:**
java.lang.Object
```
public class MailMergeCleanupOptions
```

Especifica opciones que determinan qué elementos se eliminan durante la combinación de correspondencia.

 **Examples:** 

Muestra cómo instruir al motor de combinación de correspondencia para que elimine cualquier campo contenedor alrededor de un campo de combinación durante la combinación de correspondencia.

```

 doc.getMailMerge().setCleanupOptions(MailMergeCleanupOptions.REMOVE_CONTAINING_FIELDS);
 
```

Muestra cómo eliminar automáticamente los campos de combinación no fusionados durante la combinación de correspondencia.

```

 doc.getMailMerge().setCleanupOptions(MailMergeCleanupOptions.REMOVE_UNUSED_FIELDS);
 
```

Muestra cómo asegurarse de que los párrafos vacíos que resultan de combinar campos sin datos se eliminen del documento.

```

 doc.getMailMerge().setCleanupOptions(MailMergeCleanupOptions.REMOVE_EMPTY_PARAGRAPHS);
 
```

Muestra cómo eliminar una tabla vacía completa durante la combinación de correspondencia.

```

 DataTable tableCustomers = new DataTable("A");
 tableCustomers.getColumns().add("CustomerID");
 tableCustomers.getColumns().add("CustomerName");
 tableCustomers.getRows().add(new Object[] { 1, "John Doe" });
 tableCustomers.getRows().add(new Object[] { 2, "Jane Doe" });

 DataSet ds = new DataSet();
 ds.getTables().add(tableCustomers);

 Document doc = new Document(getMyDir() + "Mail merge tables.docx");
 Assert.assertEquals(2, doc.getChildNodes(NodeType.TABLE, true).getCount());

 doc.getMailMerge().setMergeDuplicateRegions(false);
 doc.getMailMerge().setCleanupOptions(MailMergeCleanupOptions.REMOVE_EMPTY_TABLES | MailMergeCleanupOptions.REMOVE_UNUSED_REGIONS);
 doc.getMailMerge().executeWithRegions(ds.getTables().get("A"));

 doc.save(getArtifactsDir() + "MailMerge.RemoveEmptyTables.docx");

 doc = new Document(getArtifactsDir() + "MailMerge.RemoveEmptyTables.docx");
 Assert.assertEquals(1, doc.getChildNodes(NodeType.TABLE, true).getCount());
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [NONE](#NONE) | Especifica un valor predeterminado. |
| [REMOVE_CONTAINING_FIELDS](#REMOVE-CONTAINING-FIELDS) | Especifica si los campos que contienen campos de combinación (por ejemplo, IFs) deben eliminarse del documento si se eliminan los campos de combinación anidados. |
| [REMOVE_EMPTY_PARAGRAPHS](#REMOVE-EMPTY-PARAGRAPHS) | Especifica si los párrafos que contenían campos de combinación sin datos deben eliminarse del documento. |
| [REMOVE_EMPTY_TABLES](#REMOVE-EMPTY-TABLES) | Especifica si se deben eliminar del documento las tablas que contienen regiones de combinación de correspondencia que fueron eliminadas usando la opción [REMOVE\_UNUSED\_REGIONS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-UNUSED-REGIONS) o la opción [REMOVE\_EMPTY\_TABLE\_ROWS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-EMPTY-TABLE-ROWS). |
| [REMOVE_EMPTY_TABLE_ROWS](#REMOVE-EMPTY-TABLE-ROWS) | Especifica si las filas vacías que contienen regiones de combinación de correspondencia deben eliminarse del documento. |
| [REMOVE_STATIC_FIELDS](#REMOVE-STATIC-FIELDS) | Especifica si los campos estáticos deben eliminarse del documento. |
| [REMOVE_UNUSED_FIELDS](#REMOVE-UNUSED-FIELDS) | Especifica si los campos de combinación no utilizados deben eliminarse del documento. |
| [REMOVE_UNUSED_REGIONS](#REMOVE-UNUSED-REGIONS) | Especifica si las regiones de combinación de correspondencia no utilizadas deben eliminarse del documento. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String mailMergeCleanupOptionsName)](#fromName-java.lang.String) |  |
| [fromNames(Set mailMergeCleanupOptionsNames)](#fromNames-java.util.Set) |  |
| [getName(int mailMergeCleanupOptions)](#getName-int) |  |
| [getNames(int mailMergeCleanupOptions)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [toString(int mailMergeCleanupOptions)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
### NONE {#NONE}
```
public static int NONE
```


Especifica un valor predeterminado.

### REMOVE_CONTAINING_FIELDS {#REMOVE-CONTAINING-FIELDS}
```
public static int REMOVE_CONTAINING_FIELDS
```


Especifica si los campos que contienen campos de combinación (por ejemplo, IFs) deben eliminarse del documento si se eliminan los campos de combinación anidados.

### REMOVE_EMPTY_PARAGRAPHS {#REMOVE-EMPTY-PARAGRAPHS}
```
public static int REMOVE_EMPTY_PARAGRAPHS
```


Especifica si los párrafos que contenían campos de combinación sin datos deben eliminarse del documento. Cuando esta opción está activada, también se eliminan los párrafos que contienen campos de inicio y fin de región que, de otro modo, están vacíos.

### REMOVE_EMPTY_TABLES {#REMOVE-EMPTY-TABLES}
```
public static int REMOVE_EMPTY_TABLES
```


Especifica si se deben eliminar del documento las tablas que contienen regiones de combinación de correspondencia que fueron eliminadas usando la opción [REMOVE\_UNUSED\_REGIONS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-UNUSED-REGIONS) o la opción [REMOVE\_EMPTY\_TABLE\_ROWS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-EMPTY-TABLE-ROWS).

 **Remarks:** 

Esta opción se aplica solo a la combinación de correspondencia con regiones.

### REMOVE_EMPTY_TABLE_ROWS {#REMOVE-EMPTY-TABLE-ROWS}
```
public static int REMOVE_EMPTY_TABLE_ROWS
```


Especifica si las filas vacías que contienen regiones de combinación de correspondencia deben eliminarse del documento.

 **Remarks:** 

Esta opción se aplica solo a la combinación de correspondencia con regiones.

### REMOVE_STATIC_FIELDS {#REMOVE-STATIC-FIELDS}
```
public static int REMOVE_STATIC_FIELDS
```


Especifica si los campos estáticos deben eliminarse del documento. Los campos estáticos son campos cuyos resultados permanecen iguales ante cualquier cambio del documento. Los campos que no almacenan sus resultados en un documento y se calculan al vuelo (como [FieldType.FIELD\_LIST\_NUM](../../com.aspose.words/fieldtype/\#FIELD-LIST-NUM), [FieldType.FIELD\_SYMBOL](../../com.aspose.words/fieldtype/\#FIELD-SYMBOL), etc.) no se consideran estáticos.

 **Remarks:** 

Aquí está la lista completa de tipos de campo que no se consideran estáticos:

 *  [FieldType.FIELD\_ADVANCE](../../com.aspose.words/fieldtype/\#FIELD-ADVANCE)
 *  [FieldType.FIELD\_AUTO\_NUM](../../com.aspose.words/fieldtype/\#FIELD-AUTO-NUM)
 *  [FieldType.FIELD\_AUTO\_NUM\_LEGAL](../../com.aspose.words/fieldtype/\#FIELD-AUTO-NUM-LEGAL)
 *  [FieldType.FIELD\_AUTO\_NUM\_OUTLINE](../../com.aspose.words/fieldtype/\#FIELD-AUTO-NUM-OUTLINE)
 *  [FieldType.FIELD\_BARCODE](../../com.aspose.words/fieldtype/\#FIELD-BARCODE)
 *  [FieldType.FIELD\_BIDI\_OUTLINE](../../com.aspose.words/fieldtype/\#FIELD-BIDI-OUTLINE)
 *  [FieldType.FIELD\_DATE](../../com.aspose.words/fieldtype/\#FIELD-DATE)
 *  [FieldType.FIELD\_DISPLAY\_BARCODE](../../com.aspose.words/fieldtype/\#FIELD-DISPLAY-BARCODE)
 *  [FieldType.FIELD\_MERGE\_BARCODE](../../com.aspose.words/fieldtype/\#FIELD-MERGE-BARCODE)
 *  [FieldType.FIELD\_FORM\_CHECK\_BOX](../../com.aspose.words/fieldtype/\#FIELD-FORM-CHECK-BOX)
 *  [FieldType.FIELD\_FORM\_DROP\_DOWN](../../com.aspose.words/fieldtype/\#FIELD-FORM-DROP-DOWN)
 *  [FieldType.FIELD\_FORMULA](../../com.aspose.words/fieldtype/\#FIELD-FORMULA)
 *  [FieldType.FIELD\_GO\_TO\_BUTTON](../../com.aspose.words/fieldtype/\#FIELD-GO-TO-BUTTON)
 *  [FieldType.FIELD\_HYPERLINK](../../com.aspose.words/fieldtype/\#FIELD-HYPERLINK)
 *  [FieldType.FIELD\_INCLUDE\_TEXT](../../com.aspose.words/fieldtype/\#FIELD-INCLUDE-TEXT)
 *  [FieldType.FIELD\_INDEX\_ENTRY](../../com.aspose.words/fieldtype/\#FIELD-INDEX-ENTRY)
 *  [FieldType.FIELD\_LINK](../../com.aspose.words/fieldtype/\#FIELD-LINK)
 *  [FieldType.FIELD\_LIST\_NUM](../../com.aspose.words/fieldtype/\#FIELD-LIST-NUM)
 *  [FieldType.FIELD\_MACRO\_BUTTON](../../com.aspose.words/fieldtype/\#FIELD-MACRO-BUTTON)
 *  [FieldType.FIELD\_NOTE\_REF](../../com.aspose.words/fieldtype/\#FIELD-NOTE-REF)
 *  [FieldType.FIELD\_NUM\_PAGES](../../com.aspose.words/fieldtype/\#FIELD-NUM-PAGES)
 *  [FieldType.FIELD\_PAGE](../../com.aspose.words/fieldtype/\#FIELD-PAGE)
 *  [FieldType.FIELD\_PAGE\_REF](../../com.aspose.words/fieldtype/\#FIELD-PAGE-REF)
 *  [FieldType.FIELD\_PRINT](../../com.aspose.words/fieldtype/\#FIELD-PRINT)
 *  [FieldType.FIELD\_PRINT\_DATE](../../com.aspose.words/fieldtype/\#FIELD-PRINT-DATE)
 *  [FieldType.FIELD\_PRIVATE](../../com.aspose.words/fieldtype/\#FIELD-PRIVATE)
 *  [FieldType.FIELD\_REF\_DOC](../../com.aspose.words/fieldtype/\#FIELD-REF-DOC)
 *  [FieldType.FIELD\_SECTION](../../com.aspose.words/fieldtype/\#FIELD-SECTION)
 *  [FieldType.FIELD\_SECTION\_PAGES](../../com.aspose.words/fieldtype/\#FIELD-SECTION-PAGES)
 *  [FieldType.FIELD\_SYMBOL](../../com.aspose.words/fieldtype/\#FIELD-SYMBOL)
 *  [FieldType.FIELD\_TIME](../../com.aspose.words/fieldtype/\#FIELD-TIME)
 *  [FieldType.FIELD\_TOA\_ENTRY](../../com.aspose.words/fieldtype/\#FIELD-TOA-ENTRY)
 *  [FieldType.FIELD\_TOC\_ENTRY](../../com.aspose.words/fieldtype/\#FIELD-TOC-ENTRY)

### REMOVE_UNUSED_FIELDS {#REMOVE-UNUSED-FIELDS}
```
public static int REMOVE_UNUSED_FIELDS
```


Especifica si los campos de combinación no utilizados deben eliminarse del documento.

### REMOVE_UNUSED_REGIONS {#REMOVE-UNUSED-REGIONS}
```
public static int REMOVE_UNUSED_REGIONS
```


Especifica si las regiones de combinación de correspondencia no utilizadas deben eliminarse del documento.

 **Remarks:** 

Esta opción se aplica solo a la combinación de correspondencia con regiones.

### length {#length}
```
public static int length
```


### fromName(String mailMergeCleanupOptionsName) {#fromName-java.lang.String}
```
public static int fromName(String mailMergeCleanupOptionsName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| mailMergeCleanupOptionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set mailMergeCleanupOptionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set mailMergeCleanupOptionsNames)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| mailMergeCleanupOptionsNames | java.util.Set |  |

**Returns:**
int
### getName(int mailMergeCleanupOptions) {#getName-int}
```
public static String getName(int mailMergeCleanupOptions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| mailMergeCleanupOptions | int |  |

**Returns:**
java.lang.String
### getNames(int mailMergeCleanupOptions) {#getNames-int}
```
public static Set getNames(int mailMergeCleanupOptions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| mailMergeCleanupOptions | int |  |

**Returns:**
java.util.Set
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int mailMergeCleanupOptions) {#toString-int}
```
public static String toString(int mailMergeCleanupOptions)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| mailMergeCleanupOptions | int |  |

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
