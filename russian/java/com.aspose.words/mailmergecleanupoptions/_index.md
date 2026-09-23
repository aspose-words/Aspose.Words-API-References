---
title: "MailMergeCleanupOptions"
linktitle: "MailMergeCleanupOptions"
second_title: "Aspose.Words для Java"
description: "Указывает параметры, определяющие, какие элементы удаляются во время слияния почты в Java."
type: docs
weight: 438
url: /ru/java/com.aspose.words/mailmergecleanupoptions/
---

**Inheritance:**
java.lang.Object
```
public class MailMergeCleanupOptions
```

Указывает параметры, определяющие, какие элементы удаляются во время слияния почты.

 **Examples:** 

Показывает, как указать движку слияния почты удалять любые содержащие поля вокруг поля слияния во время слияния.

```

 doc.getMailMerge().setCleanupOptions(MailMergeCleanupOptions.REMOVE_CONTAINING_FIELDS);
 
```

Показывает, как автоматически удалять неслияные поля слияния во время слияния почты.

```

 doc.getMailMerge().setCleanupOptions(MailMergeCleanupOptions.REMOVE_UNUSED_FIELDS);
 
```

Показывает, как убедиться, что пустые абзацы, полученные в результате слияния полей без данных, удаляются из документа.

```

 doc.getMailMerge().setCleanupOptions(MailMergeCleanupOptions.REMOVE_EMPTY_PARAGRAPHS);
 
```

Показывает, как удалить полностью пустую таблицу во время слияния почты.

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
## Поля

| Поле | Описание |
| --- | --- |
| [NONE](#NONE) | Указывает значение по умолчанию. |
| [REMOVE_CONTAINING_FIELDS](#REMOVE-CONTAINING-FIELDS) | Указывает, следует ли удалять из документа поля, содержащие поля слияния (например, IF), если вложенные поля слияния удалены. |
| [REMOVE_EMPTY_PARAGRAPHS](#REMOVE-EMPTY-PARAGRAPHS) | Указывает, следует ли удалять из документа абзацы, содержащие поля слияния почты без данных. |
| [REMOVE_EMPTY_TABLES](#REMOVE-EMPTY-TABLES) | Указывает, следует ли удалять из документа таблицы, содержащие регионы слияния почты, которые были удалены с помощью параметра [REMOVE\_UNUSED\_REGIONS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-UNUSED-REGIONS) или [REMOVE\_EMPTY\_TABLE\_ROWS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-EMPTY-TABLE-ROWS). |
| [REMOVE_EMPTY_TABLE_ROWS](#REMOVE-EMPTY-TABLE-ROWS) | Указывает, следует ли удалять из документа пустые строки, содержащие регионы слияния почты. |
| [REMOVE_STATIC_FIELDS](#REMOVE-STATIC-FIELDS) | Указывает, следует ли удалять из документа статические поля. |
| [REMOVE_UNUSED_FIELDS](#REMOVE-UNUSED-FIELDS) | Указывает, следует ли удалять из документа неиспользуемые поля слияния. |
| [REMOVE_UNUSED_REGIONS](#REMOVE-UNUSED-REGIONS) | Указывает, следует ли удалять из документа неиспользуемые регионы слияния почты. |
| [length](#length) |  |
## Методы

| Метод | Описание |
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


Указывает значение по умолчанию.

### REMOVE_CONTAINING_FIELDS {#REMOVE-CONTAINING-FIELDS}
```
public static int REMOVE_CONTAINING_FIELDS
```


Указывает, следует ли удалять из документа поля, содержащие поля слияния (например, IF), если вложенные поля слияния удалены.

### REMOVE_EMPTY_PARAGRAPHS {#REMOVE-EMPTY-PARAGRAPHS}
```
public static int REMOVE_EMPTY_PARAGRAPHS
```


Указывает, следует ли удалять из документа абзацы, содержащие поля слияния почты без данных. Когда эта опция включена, также удаляются абзацы, содержащие начальные и конечные поля слияния региона, которые иначе пусты.

### REMOVE_EMPTY_TABLES {#REMOVE-EMPTY-TABLES}
```
public static int REMOVE_EMPTY_TABLES
```


Указывает, следует ли удалять из документа таблицы, содержащие регионы слияния почты, которые были удалены с помощью параметра [REMOVE\_UNUSED\_REGIONS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-UNUSED-REGIONS) или [REMOVE\_EMPTY\_TABLE\_ROWS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-EMPTY-TABLE-ROWS).

 **Remarks:** 

This option applies only to mail merge with regions.

### REMOVE_EMPTY_TABLE_ROWS {#REMOVE-EMPTY-TABLE-ROWS}
```
public static int REMOVE_EMPTY_TABLE_ROWS
```


Указывает, следует ли удалять из документа пустые строки, содержащие регионы слияния почты.

 **Remarks:** 

This option applies only to mail merge with regions.

### REMOVE_STATIC_FIELDS {#REMOVE-STATIC-FIELDS}
```
public static int REMOVE_STATIC_FIELDS
```


Указывает, следует ли удалять статические поля из документа. Статические поля — это поля, результаты которых остаются одинаковыми при любом изменении документа. Поля, которые не сохраняют свои результаты в документе и вычисляются «на лету» (например, [FieldType.FIELD\_LIST\_NUM](../../com.aspose.words/fieldtype/\#FIELD-LIST-NUM), [FieldType.FIELD\_SYMBOL](../../com.aspose.words/fieldtype/\#FIELD-SYMBOL), и т.д.) не считаются статическими.

 **Remarks:** 

Вот полный список типов полей, которые не считаются статическими:

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


Указывает, следует ли удалять из документа неиспользуемые поля слияния.

### REMOVE_UNUSED_REGIONS {#REMOVE-UNUSED-REGIONS}
```
public static int REMOVE_UNUSED_REGIONS
```


Указывает, следует ли удалять из документа неиспользуемые регионы слияния почты.

 **Remarks:** 

This option applies only to mail merge with regions.

### length {#length}
```
public static int length
```


### fromName(String mailMergeCleanupOptionsName) {#fromName-java.lang.String}
```
public static int fromName(String mailMergeCleanupOptionsName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| mailMergeCleanupOptionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set mailMergeCleanupOptionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set mailMergeCleanupOptionsNames)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| mailMergeCleanupOptionsNames | java.util.Set |  |

**Returns:**
int
### getName(int mailMergeCleanupOptions) {#getName-int}
```
public static String getName(int mailMergeCleanupOptions)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| mailMergeCleanupOptions | int |  |

**Returns:**
java.lang.String
### getNames(int mailMergeCleanupOptions) {#getNames-int}
```
public static Set getNames(int mailMergeCleanupOptions)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| mailMergeCleanupOptions | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
