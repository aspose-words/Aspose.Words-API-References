---
title: "MailMergeCleanupOptions"
linktitle: "MailMergeCleanupOptions"
second_title: "Aspose.Words Java için"
description: "Java'da posta birleştirme sırasında hangi öğelerin kaldırılacağını belirleyen seçenekleri tanımlar."
type: docs
weight: 438
url: /tr/java/com.aspose.words/mailmergecleanupoptions/
---

**Inheritance:**
java.lang.Object
```
public class MailMergeCleanupOptions
```

Posta birleştirme sırasında hangi öğelerin kaldırılacağını belirleyen seçenekleri belirtir.

 **Examples:** 

Posta birleştirme sırasında bir birleştirme alanının etrafındaki kapsayan alanların kaldırılması için birleştirme motoruna nasıl talimat verileceğini gösterir.

```

 doc.getMailMerge().setCleanupOptions(MailMergeCleanupOptions.REMOVE_CONTAINING_FIELDS);
 
```

Posta birleştirme sırasında birleştirilmemiş birleştirme alanlarının otomatik olarak nasıl kaldırılacağını gösterir.

```

 doc.getMailMerge().setCleanupOptions(MailMergeCleanupOptions.REMOVE_UNUSED_FIELDS);
 
```

Veri içermeyen alanların birleştirilmesinden oluşan boş paragrafların belgeden kaldırıldığından emin olmayı gösterir.

```

 doc.getMailMerge().setCleanupOptions(MailMergeCleanupOptions.REMOVE_EMPTY_PARAGRAPHS);
 
```

Posta birleştirme sırasında tamamen boş bir tabloyu nasıl kaldıracağınızı gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [NONE](#NONE) | Varsayılan bir değer belirtir. |
| [REMOVE_CONTAINING_FIELDS](#REMOVE-CONTAINING-FIELDS) | İç içe birleştirme alanları kaldırıldığında, birleştirme alanları (örneğin IF'ler) içeren alanların belgeden kaldırılıp kaldırılmayacağını belirtir. |
| [REMOVE_EMPTY_PARAGRAPHS](#REMOVE-EMPTY-PARAGRAPHS) | Veri içermeyen posta birleştirme alanları içeren paragrafların belgeden kaldırılıp kaldırılmayacağını belirtir. |
| [REMOVE_EMPTY_TABLES](#REMOVE-EMPTY-TABLES) | Belgeden, ya [REMOVE\_UNUSED\_REGIONS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-UNUSED-REGIONS) ya da [REMOVE\_EMPTY\_TABLE\_ROWS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-EMPTY-TABLE-ROWS) seçeneği kullanılarak kaldırılan posta birleştirme bölgelerini içeren tabloların kaldırılıp kaldırılmayacağını belirtir. |
| [REMOVE_EMPTY_TABLE_ROWS](#REMOVE-EMPTY-TABLE-ROWS) | Posta birleştirme bölgelerini içeren boş satırların belgeden kaldırılıp kaldırılmayacağını belirtir. |
| [REMOVE_STATIC_FIELDS](#REMOVE-STATIC-FIELDS) | Statik alanların belgeden kaldırılıp kaldırılmayacağını belirtir. |
| [REMOVE_UNUSED_FIELDS](#REMOVE-UNUSED-FIELDS) | Kullanılmayan birleştirme alanlarının belgeden kaldırılıp kaldırılmayacağını belirtir. |
| [REMOVE_UNUSED_REGIONS](#REMOVE-UNUSED-REGIONS) | Kullanılmayan posta birleştirme bölgelerinin belgeden kaldırılıp kaldırılmayacağını belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
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


Varsayılan bir değer belirtir.

### REMOVE_CONTAINING_FIELDS {#REMOVE-CONTAINING-FIELDS}
```
public static int REMOVE_CONTAINING_FIELDS
```


İç içe birleştirme alanları kaldırıldığında, birleştirme alanları (örneğin IF'ler) içeren alanların belgeden kaldırılıp kaldırılmayacağını belirtir.

### REMOVE_EMPTY_PARAGRAPHS {#REMOVE-EMPTY-PARAGRAPHS}
```
public static int REMOVE_EMPTY_PARAGRAPHS
```


Veri içermeyen posta birleştirme alanları içeren paragrafların belgeden kaldırılıp kaldırılmayacağını belirtir. Bu seçenek ayarlandığında, aksi takdirde boş olan bölge başlangıç ve bitiş birleştirme alanlarını içeren paragraflar da kaldırılır.

### REMOVE_EMPTY_TABLES {#REMOVE-EMPTY-TABLES}
```
public static int REMOVE_EMPTY_TABLES
```


Belgeden, ya [REMOVE\_UNUSED\_REGIONS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-UNUSED-REGIONS) ya da [REMOVE\_EMPTY\_TABLE\_ROWS](../../com.aspose.words/mailmergecleanupoptions/\#REMOVE-EMPTY-TABLE-ROWS) seçeneği kullanılarak kaldırılan posta birleştirme bölgelerini içeren tabloların kaldırılıp kaldırılmayacağını belirtir.

 **Remarks:** 

Bu seçenek yalnızca bölgelerle yapılan posta birleştirmesine uygulanır.

### REMOVE_EMPTY_TABLE_ROWS {#REMOVE-EMPTY-TABLE-ROWS}
```
public static int REMOVE_EMPTY_TABLE_ROWS
```


Posta birleştirme bölgelerini içeren boş satırların belgeden kaldırılıp kaldırılmayacağını belirtir.

 **Remarks:** 

Bu seçenek yalnızca bölgelerle yapılan posta birleştirmesine uygulanır.

### REMOVE_STATIC_FIELDS {#REMOVE-STATIC-FIELDS}
```
public static int REMOVE_STATIC_FIELDS
```


Belgenin statik alanlardan temizlenip temizlenmeyeceğini belirtir. Statik alanlar, belge değiştiğinde sonuçları aynı kalan alanlardır. Sonuçlarını belgeye kaydetmeyen ve anlık olarak hesaplanan alanlar (örneğin [FieldType.FIELD\_LIST\_NUM](../../com.aspose.words/fieldtype/\#FIELD-LIST-NUM), [FieldType.FIELD\_SYMBOL](../../com.aspose.words/fieldtype/\#FIELD-SYMBOL), vb.) statik olarak kabul edilmez.

 **Remarks:** 

Statik olarak kabul edilmeyen alan türlerinin tam listesi aşağıdadır:

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


Kullanılmayan birleştirme alanlarının belgeden kaldırılıp kaldırılmayacağını belirtir.

### REMOVE_UNUSED_REGIONS {#REMOVE-UNUSED-REGIONS}
```
public static int REMOVE_UNUSED_REGIONS
```


Kullanılmayan posta birleştirme bölgelerinin belgeden kaldırılıp kaldırılmayacağını belirtir.

 **Remarks:** 

Bu seçenek yalnızca bölgelerle yapılan posta birleştirmesine uygulanır.

### length {#length}
```
public static int length
```


### fromName(String mailMergeCleanupOptionsName) {#fromName-java.lang.String}
```
public static int fromName(String mailMergeCleanupOptionsName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| mailMergeCleanupOptionsName | java.lang.String |  |

**Returns:**
int
### fromNames(Set mailMergeCleanupOptionsNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set mailMergeCleanupOptionsNames)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| mailMergeCleanupOptionsNames | java.util.Set |  |

**Returns:**
int
### getName(int mailMergeCleanupOptions) {#getName-int}
```
public static String getName(int mailMergeCleanupOptions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| mailMergeCleanupOptions | int |  |

**Returns:**
java.lang.String
### getNames(int mailMergeCleanupOptions) {#getNames-int}
```
public static Set getNames(int mailMergeCleanupOptions)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| mailMergeCleanupOptions | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
