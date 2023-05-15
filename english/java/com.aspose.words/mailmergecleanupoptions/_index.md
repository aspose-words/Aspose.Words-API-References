---
title: MailMergeCleanupOptions
linktitle: MailMergeCleanupOptions
second_title: Aspose.Words for Java
description: Specifies options that determine what items are removed during mail merge in Java.
type: docs
weight: 394
url: /java/com.aspose.words/mailmergecleanupoptions/
---

**Inheritance:**
java.lang.Object
```
public class MailMergeCleanupOptions
```

Specifies options that determine what items are removed during mail merge.

 **Examples:** 

Shows how to automatically remove unmerged merge fields during mail merge.

```

 doc.getMailMerge().setCleanupOptions(MailMergeCleanupOptions.REMOVE_UNUSED_FIELDS);
 
```

Shows how to make sure empty paragraphs that result from merging fields with no data are removed from the document.

```

 doc.getMailMerge().setCleanupOptions(MailMergeCleanupOptions.REMOVE_EMPTY_PARAGRAPHS);
 
```

Shows how to instruct the mail merge engine to remove any containing fields from around a merge field during mail merge.

```

 doc.getMailMerge().setCleanupOptions(MailMergeCleanupOptions.REMOVE_CONTAINING_FIELDS);
 
```
## Fields

| Field | Description |
| --- | --- |
| [NONE](#NONE) | Specifies a default value. |
| [REMOVE_CONTAINING_FIELDS](#REMOVE-CONTAINING-FIELDS) | Specifies whether fields that contain merge fields (for example, IFs) should be removed from the document if the nested merge fields are removed. |
| [REMOVE_EMPTY_PARAGRAPHS](#REMOVE-EMPTY-PARAGRAPHS) | Specifies whether paragraphs that contained mail merge fields with no data should be removed from the document. |
| [REMOVE_EMPTY_TABLE_ROWS](#REMOVE-EMPTY-TABLE-ROWS) | Specifies whether empty rows that contain mail merge regions should be removed from the document. |
| [REMOVE_STATIC_FIELDS](#REMOVE-STATIC-FIELDS) | Specifies whether static fields should be removed from the document. |
| [REMOVE_UNUSED_FIELDS](#REMOVE-UNUSED-FIELDS) | Specifies whether unused merge fields should be removed from the document. |
| [REMOVE_UNUSED_REGIONS](#REMOVE-UNUSED-REGIONS) | Specifies whether unused mail merge regions should be removed from the document. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String mailMergeCleanupOptionsName)](#fromName-java.lang.String) |  |
| [fromNames(Set mailMergeCleanupOptionsNames)](#fromNames-java.util.Set) |  |
| [getClass()](#getClass) |  |
| [getName(int mailMergeCleanupOptions)](#getName-int) |  |
| [getNames(int mailMergeCleanupOptions)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int mailMergeCleanupOptions)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### NONE {#NONE}
```
public static int NONE
```


Specifies a default value.

### REMOVE_CONTAINING_FIELDS {#REMOVE-CONTAINING-FIELDS}
```
public static int REMOVE_CONTAINING_FIELDS
```


Specifies whether fields that contain merge fields (for example, IFs) should be removed from the document if the nested merge fields are removed.

### REMOVE_EMPTY_PARAGRAPHS {#REMOVE-EMPTY-PARAGRAPHS}
```
public static int REMOVE_EMPTY_PARAGRAPHS
```


Specifies whether paragraphs that contained mail merge fields with no data should be removed from the document. When this option is set, paragraphs which contain region start and end merge fields which are otherwise empty are also removed.

### REMOVE_EMPTY_TABLE_ROWS {#REMOVE-EMPTY-TABLE-ROWS}
```
public static int REMOVE_EMPTY_TABLE_ROWS
```


Specifies whether empty rows that contain mail merge regions should be removed from the document.

 **Remarks:** 

This option applies only to mail merge with regions.

### REMOVE_STATIC_FIELDS {#REMOVE-STATIC-FIELDS}
```
public static int REMOVE_STATIC_FIELDS
```


Specifies whether static fields should be removed from the document. Static fields are fields, which results remain the same upon any document change. Fields, which do not store their results in a document and are calculated on the fly (like [FieldType.FIELD\_LIST\_NUM](../../com.aspose.words/fieldtype/\#FIELD-LIST-NUM), [FieldType.FIELD\_SYMBOL](../../com.aspose.words/fieldtype/\#FIELD-SYMBOL), etc.) are not considered to be static.

 **Remarks:** 

Here is the full list of field types, which are not considered to be static:

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


Specifies whether unused merge fields should be removed from the document.

### REMOVE_UNUSED_REGIONS {#REMOVE-UNUSED-REGIONS}
```
public static int REMOVE_UNUSED_REGIONS
```


Specifies whether unused mail merge regions should be removed from the document.

 **Remarks:** 

This option applies only to mail merge with regions.

### length {#length}
```
public static int length
```


### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### fromName(String mailMergeCleanupOptionsName) {#fromName-java.lang.String}
```
public static int fromName(String mailMergeCleanupOptionsName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| mailMergeCleanupOptionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set mailMergeCleanupOptionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set mailMergeCleanupOptionsNames)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| mailMergeCleanupOptionsNames | java.util.Set |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int mailMergeCleanupOptions) {#getName-int}
```
public static String getName(int mailMergeCleanupOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| mailMergeCleanupOptions | int |  |

**Returns:**
java.lang.String
### getNames(int mailMergeCleanupOptions) {#getNames-int}
```
public static Set getNames(int mailMergeCleanupOptions)
```




**Parameters:**
| Parameter | Type | Description |
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
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### toString(int mailMergeCleanupOptions) {#toString-int}
```
public static String toString(int mailMergeCleanupOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| mailMergeCleanupOptions | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

