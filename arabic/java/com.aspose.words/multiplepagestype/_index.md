---
title: "MultiplePagesType"
linktitle: "MultiplePagesType"
second_title: "Aspose.Words لـ Java"
description: "يحدد كيفية طباعة المستند في Java."
type: docs
weight: 473
url: /ar/java/com.aspose.words/multiplepagestype/
---

**Inheritance:**
java.lang.Object
```
public class MultiplePagesType
```

يحدد كيفية طباعة المستند.

 **Examples:** 

يظهر كيفية تكوين مستند يمكن طباعته كطيّ كتاب.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [BOOK_FOLD_PRINTING](#BOOK-FOLD-PRINTING) | يحدد ما إذا كان سيتم طباعة المستند كطي كتاب. |
| [BOOK_FOLD_PRINTING_REVERSE](#BOOK-FOLD-PRINTING-REVERSE) | يحدد ما إذا كان سيتم طباعة المستند كطي كتاب عكسي. |
| [DEFAULT](#DEFAULT) | القيمة الافتراضية هي [NORMAL](../../com.aspose.words/multiplepagestype/\#NORMAL) |
| [MIRROR_MARGINS](#MIRROR-MARGINS) | يبدل الهوامش اليسرى واليمنى في الصفحات المتقابلة. |
| [NORMAL](#NORMAL) | طباعة عادية، دون تحديد صفحات متعددة. |
| [TWO_PAGES_PER_SHEET](#TWO-PAGES-PER-SHEET) | يطبع صفحتين لكل ورقة. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String multiplePagesTypeName)](#fromName-java.lang.String) |  |
| [getName(int multiplePagesType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int multiplePagesType)](#toString-int) |  |
### BOOK_FOLD_PRINTING {#BOOK-FOLD-PRINTING}
```
public static int BOOK_FOLD_PRINTING
```


يحدد ما إذا كان سيتم طباعة المستند كطي كتاب.

### BOOK_FOLD_PRINTING_REVERSE {#BOOK-FOLD-PRINTING-REVERSE}
```
public static int BOOK_FOLD_PRINTING_REVERSE
```


يحدد ما إذا كان سيتم طباعة المستند كطي كتاب عكسي.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


القيمة الافتراضية هي [NORMAL](../../com.aspose.words/multiplepagestype/\#NORMAL)

### MIRROR_MARGINS {#MIRROR-MARGINS}
```
public static int MIRROR_MARGINS
```


يبدل الهوامش اليسرى واليمنى في الصفحات المتقابلة.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


طباعة عادية، دون تحديد صفحات متعددة.

### TWO_PAGES_PER_SHEET {#TWO-PAGES-PER-SHEET}
```
public static int TWO_PAGES_PER_SHEET
```


يطبع صفحتين لكل ورقة.

### length {#length}
```
public static int length
```


### fromName(String multiplePagesTypeName) {#fromName-java.lang.String}
```
public static int fromName(String multiplePagesTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| multiplePagesTypeName | java.lang.String |  |

**Returns:**
int
### getName(int multiplePagesType) {#getName-int}
```
public static String getName(int multiplePagesType)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| multiplePagesType | int |  |

**Returns:**
java.lang.String
