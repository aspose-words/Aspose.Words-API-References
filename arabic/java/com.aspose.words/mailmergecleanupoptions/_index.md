---
title: "MailMergeCleanupOptions"
linktitle: "MailMergeCleanupOptions"
second_title: "Aspose.Words لـ Java"
description: "يحدد الخيارات التي تحدد العناصر التي تُزال أثناء دمج البريد في Java."
type: docs
weight: 438
url: /ar/java/com.aspose.words/mailmergecleanupoptions/
---

**Inheritance:**
java.lang.Object
```
public class MailMergeCleanupOptions
```

يحدد الخيارات التي تحدد ما العناصر التي تُزال أثناء دمج البريد.

 **Examples:** 

يوضح كيفية إرشاد محرك دمج البريد لإزالة أي حقول محتوية حول حقل دمج أثناء دمج البريد.

```

 doc.getMailMerge().setCleanupOptions(MailMergeCleanupOptions.REMOVE_CONTAINING_FIELDS);
 
```

يوضح كيفية إزالة حقول الدمج غير المدمجة تلقائيًا أثناء دمج البريد.

```

 doc.getMailMerge().setCleanupOptions(MailMergeCleanupOptions.REMOVE_UNUSED_FIELDS);
 
```

يوضح كيفية التأكد من إزالة الفقرات الفارغة التي تنتج عن دمج حقول بدون بيانات من المستند.

```

 doc.getMailMerge().setCleanupOptions(MailMergeCleanupOptions.REMOVE_EMPTY_PARAGRAPHS);
 
```

يوضح كيفية إزالة جدول فارغ كامل أثناء دمج البريد.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [NONE](#NONE) | يحدد قيمة افتراضية. |
| [REMOVE_CONTAINING_FIELDS](#REMOVE-CONTAINING-FIELDS) | يحدد ما إذا كان يجب إزالة الحقول التي تحتوي على حقول دمج (مثل IFs) من المستند إذا تم إزالة حقول الدمج المتداخلة. |
| [REMOVE_EMPTY_PARAGRAPHS](#REMOVE-EMPTY-PARAGRAPHS) | يحدد ما إذا كان يجب إزالة الفقرات التي احتوت حقول دمج بريد بدون بيانات من المستند. |
| [REMOVE_EMPTY_TABLES](#REMOVE-EMPTY-TABLES) | يحدد ما إذا كان يجب إزالة الجداول التي تحتوي على مناطق دمج بريد من المستند والتي تم إزالتها باستخدام إما خيار [REMOVE\_UNUSED\_REGIONS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-UNUSED-REGIONS) أو خيار [REMOVE\_EMPTY\_TABLE\_ROWS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-EMPTY-TABLE-ROWS). |
| [REMOVE_EMPTY_TABLE_ROWS](#REMOVE-EMPTY-TABLE-ROWS) | يحدد ما إذا كان يجب إزالة الصفوف الفارغة التي تحتوي على مناطق دمج بريد من المستند. |
| [REMOVE_STATIC_FIELDS](#REMOVE-STATIC-FIELDS) | يحدد ما إذا كان يجب إزالة الحقول الثابتة من المستند. |
| [REMOVE_UNUSED_FIELDS](#REMOVE-UNUSED-FIELDS) | يحدد ما إذا كان يجب إزالة حقول الدمج غير المستخدمة من المستند. |
| [REMOVE_UNUSED_REGIONS](#REMOVE-UNUSED-REGIONS) | يحدد ما إذا كان يجب إزالة مناطق دمج البريد غير المستخدمة من المستند. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
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


يحدد قيمة افتراضية.

### REMOVE_CONTAINING_FIELDS {#REMOVE-CONTAINING-FIELDS}
```
public static int REMOVE_CONTAINING_FIELDS
```


يحدد ما إذا كان يجب إزالة الحقول التي تحتوي على حقول دمج (مثل IFs) من المستند إذا تم إزالة حقول الدمج المتداخلة.

### REMOVE_EMPTY_PARAGRAPHS {#REMOVE-EMPTY-PARAGRAPHS}
```
public static int REMOVE_EMPTY_PARAGRAPHS
```


يحدد ما إذا كان يجب إزالة الفقرات التي احتوت حقول دمج بريد بدون بيانات من المستند. عندما يتم تعيين هذا الخيار، تُزال أيضًا الفقرات التي تحتوي على حقول دمج بداية ونهاية المنطقة والتي تكون فارغة بخلاف ذلك.

### REMOVE_EMPTY_TABLES {#REMOVE-EMPTY-TABLES}
```
public static int REMOVE_EMPTY_TABLES
```


يحدد ما إذا كان يجب إزالة الجداول التي تحتوي على مناطق دمج بريد من المستند والتي تم إزالتها باستخدام إما خيار [REMOVE\_UNUSED\_REGIONS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-UNUSED-REGIONS) أو خيار [REMOVE\_EMPTY\_TABLE\_ROWS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-EMPTY-TABLE-ROWS).

 **Remarks:** 

هذا الخيار ينطبق فقط على دمج البريد مع المناطق.

### REMOVE_EMPTY_TABLE_ROWS {#REMOVE-EMPTY-TABLE-ROWS}
```
public static int REMOVE_EMPTY_TABLE_ROWS
```


يحدد ما إذا كان يجب إزالة الصفوف الفارغة التي تحتوي على مناطق دمج بريد من المستند.

 **Remarks:** 

هذا الخيار ينطبق فقط على دمج البريد مع المناطق.

### REMOVE_STATIC_FIELDS {#REMOVE-STATIC-FIELDS}
```
public static int REMOVE_STATIC_FIELDS
```


يحدد ما إذا كان يجب إزالة الحقول الثابتة من المستند. الحقول الثابتة هي الحقول التي تظل نتائجها كما هي عند أي تغيير في المستند. الحقول التي لا تخزن نتائجها في المستند وتُحسب في الوقت الفعلي (مثل [FieldType.FIELD\_LIST\_NUM](../../com.aspose.words/fieldtype/\#FIELD-LIST-NUM), [FieldType.FIELD\_SYMBOL](../../com.aspose.words/fieldtype/\#FIELD-SYMBOL), إلخ) لا تُعتبر ثابتة.

 **Remarks:** 

إليك القائمة الكاملة لأنواع الحقول التي لا تُعتبر ثابتة:

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


يحدد ما إذا كان يجب إزالة حقول الدمج غير المستخدمة من المستند.

### REMOVE_UNUSED_REGIONS {#REMOVE-UNUSED-REGIONS}
```
public static int REMOVE_UNUSED_REGIONS
```


يحدد ما إذا كان يجب إزالة مناطق دمج البريد غير المستخدمة من المستند.

 **Remarks:** 

هذا الخيار ينطبق فقط على دمج البريد مع المناطق.

### length {#length}
```
public static int length
```


### fromName(String mailMergeCleanupOptionsName) {#fromName-java.lang.String}
```
public static int fromName(String mailMergeCleanupOptionsName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| mailMergeCleanupOptionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set mailMergeCleanupOptionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set mailMergeCleanupOptionsNames)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| mailMergeCleanupOptionsNames | java.util.Set |  |

**Returns:**
int
### getName(int mailMergeCleanupOptions) {#getName-int}
```
public static String getName(int mailMergeCleanupOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| mailMergeCleanupOptions | int |  |

**Returns:**
java.lang.String
### getNames(int mailMergeCleanupOptions) {#getNames-int}
```
public static Set getNames(int mailMergeCleanupOptions)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| mailMergeCleanupOptions | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
