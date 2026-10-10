---
title: "MultiplePagesType"
linktitle: "MultiplePagesType"
second_title: "Aspose.Words Java için"
description: "Belgenin Java'da nasıl yazdırılacağını belirtir."
type: docs
weight: 473
url: /tr/java/com.aspose.words/multiplepagestype/
---

**Inheritance:**
java.lang.Object
```
public class MultiplePagesType
```

Belgenin nasıl yazdırılacağını belirtir.

 **Examples:** 

Kitap katlaması olarak yazdırılabilecek bir belgenin nasıl yapılandırılacağını gösterir.

```

 Document doc = new Document();

 // Insert text that spans 16 pages.
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("My Booklet:");

 for (int i = 0; i < 15; i++) {
     builder.insertBreak(BreakType.PAGE_BREAK);
     builder.write(MessageFormat.format("Booklet face #{0}", i));
 }

 // Configure the first section's "PageSetup" property to print the document in the form of a book fold.
 // When we print this document on both sides, we can take the pages to stack them
 // and fold them all down the middle at once. The contents of the document will line up into a book fold.
 PageSetup pageSetup = doc.getSections().get(0).getPageSetup();
 pageSetup.setMultiplePages(MultiplePagesType.BOOK_FOLD_PRINTING);

 // We can only specify the number of sheets in multiples of 4.
 pageSetup.setSheetsPerBooklet(4);

 doc.save(getArtifactsDir() + "PageSetup.Booklet.docx");
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [BOOK_FOLD_PRINTING](#BOOK-FOLD-PRINTING) | Belgeyi kitap katlaması olarak yazdırıp yazdırmayacağını belirtir. |
| [BOOK_FOLD_PRINTING_REVERSE](#BOOK-FOLD-PRINTING-REVERSE) | Belgeyi ters kitap katlaması olarak yazdırıp yazdırmayacağını belirtir. |
| [DEFAULT](#DEFAULT) | Varsayılan değer [NORMAL](../../com.aspose.words/multiplepagestype/\#NORMAL) |
| [MIRROR_MARGINS](#MIRROR-MARGINS) | Karşılıklı sayfalarda sol ve sağ kenar boşluklarını değiştirir. |
| [NORMAL](#NORMAL) | Normal baskı, çoklu sayfa belirtilmedi. |
| [TWO_PAGES_PER_SHEET](#TWO-PAGES-PER-SHEET) | Sayfa başına iki sayfa yazdırır. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String multiplePagesTypeName)](#fromName-java.lang.String) |  |
| [getName(int multiplePagesType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int multiplePagesType)](#toString-int) |  |
### BOOK_FOLD_PRINTING {#BOOK-FOLD-PRINTING}
```
public static int BOOK_FOLD_PRINTING
```


Belgeyi kitap katlaması olarak yazdırıp yazdırmayacağını belirtir.

### BOOK_FOLD_PRINTING_REVERSE {#BOOK-FOLD-PRINTING-REVERSE}
```
public static int BOOK_FOLD_PRINTING_REVERSE
```


Belgeyi ters kitap katlaması olarak yazdırıp yazdırmayacağını belirtir.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Varsayılan değer [NORMAL](../../com.aspose.words/multiplepagestype/\#NORMAL)

### MIRROR_MARGINS {#MIRROR-MARGINS}
```
public static int MIRROR_MARGINS
```


Karşılıklı sayfalarda sol ve sağ kenar boşluklarını değiştirir.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Normal baskı, çoklu sayfa belirtilmedi.

### TWO_PAGES_PER_SHEET {#TWO-PAGES-PER-SHEET}
```
public static int TWO_PAGES_PER_SHEET
```


Sayfa başına iki sayfa yazdırır.

### length {#length}
```
public static int length
```


### fromName(String multiplePagesTypeName) {#fromName-java.lang.String}
```
public static int fromName(String multiplePagesTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| multiplePagesTypeName | java.lang.String |  |

**Returns:**
int
### getName(int multiplePagesType) {#getName-int}
```
public static String getName(int multiplePagesType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| multiplePagesType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int multiplePagesType) {#toString-int}
```
public static String toString(int multiplePagesType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| multiplePagesType | int |  |

**Returns:**
java.lang.String
