---
title: "TextColumn"
linktitle: "TextColumn"
second_title: "Aspose.Words Java için"
description: "Java'da tek bir metin sütununu temsil eder."
type: docs
weight: 670
url: /tr/java/com.aspose.words/textcolumn/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class TextColumn implements Cloneable
```

Tek bir metin sütununu temsil eder. [TextColumn](../../com.aspose.words/textcolumn/) , [TextColumnCollection](../../com.aspose.words/textcolumncollection/) koleksiyonunun bir üyesidir. [TextColumn](../../com.aspose.words/textcolumn/) koleksiyonu, bir belgenin bölümündeki tüm sütunları içerir.

Daha fazla bilgi edinmek için, [ Working with Sections ][Working with Sections] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

[TextColumn](../../com.aspose.words/textcolumn/) objects are only used to specify columns with custom width and spacing. If you want the columns in the document to be of equal width, set TextColumns. [TextColumnCollection.getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [TextColumnCollection.setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) to  true .

Yeni bir [TextColumn](../../com.aspose.words/textcolumn/) oluşturulduğunda, genişliği ve aralığı sıfır olarak ayarlanır.

 **Examples:** 

Eşit olmayan aralıklı sütunlar oluşturmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 PageSetup pageSetup = builder.getPageSetup();

 TextColumnCollection columns = pageSetup.getTextColumns();
 columns.setEvenlySpaced(false);
 columns.setCount(2);

 // Determine the amount of room that we have available for arranging columns.
 double contentWidth = pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin();

 Assert.assertEquals(468.0d, contentWidth, 0.01d);

 // Set the first column to be narrow.
 TextColumn column = columns.get(0);
 column.setWidth(100.0);
 column.setSpaceAfter(20.0);

 // Set the second column to take the rest of the space available within the margins of the page.
 column = columns.get(1);
 column.setWidth(contentWidth - column.getWidth() - column.getSpaceAfter());

 builder.writeln("Narrow column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Wide column 2.");

 doc.save(getArtifactsDir() + "PageSetup.CustomColumnWidth.docx");
 
```


[Working with Sections]: https://docs.aspose.com/words/java/working-with-sections/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getSpaceAfter()](#getSpaceAfter) | Bu sütun ile sonraki sütun arasındaki boşluğu nokta cinsinden alır. |
| [getWidth()](#getWidth) | Metin sütununun genişliğini nokta cinsinden alır. |
| [setSpaceAfter(double value)](#setSpaceAfter-double) | Bu sütun ile sonraki sütun arasındaki boşluğu nokta cinsinden ayarlar. |
| [setWidth(double value)](#setWidth-double) | Metin sütununun genişliğini nokta cinsinden ayarlar. |
### getSpaceAfter() {#getSpaceAfter}
```
public double getSpaceAfter()
```


Bu sütun ile sonraki sütun arasındaki boşluğu nokta cinsinden alır. Son sütun için gerekli değildir.

 **Examples:** 

Eşit olmayan aralıklı sütunlar oluşturmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 PageSetup pageSetup = builder.getPageSetup();

 TextColumnCollection columns = pageSetup.getTextColumns();
 columns.setEvenlySpaced(false);
 columns.setCount(2);

 // Determine the amount of room that we have available for arranging columns.
 double contentWidth = pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin();

 Assert.assertEquals(468.0d, contentWidth, 0.01d);

 // Set the first column to be narrow.
 TextColumn column = columns.get(0);
 column.setWidth(100.0);
 column.setSpaceAfter(20.0);

 // Set the second column to take the rest of the space available within the margins of the page.
 column = columns.get(1);
 column.setWidth(contentWidth - column.getWidth() - column.getSpaceAfter());

 builder.writeln("Narrow column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Wide column 2.");

 doc.save(getArtifactsDir() + "PageSetup.CustomColumnWidth.docx");
 
```

**Returns:**
double - Bu sütun ile sonraki sütun arasındaki boşluk puan cinsinden.
### getWidth() {#getWidth}
```
public double getWidth()
```


Metin sütununun genişliğini nokta cinsinden alır.

 **Examples:** 

Eşit olmayan aralıklı sütunlar oluşturmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 PageSetup pageSetup = builder.getPageSetup();

 TextColumnCollection columns = pageSetup.getTextColumns();
 columns.setEvenlySpaced(false);
 columns.setCount(2);

 // Determine the amount of room that we have available for arranging columns.
 double contentWidth = pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin();

 Assert.assertEquals(468.0d, contentWidth, 0.01d);

 // Set the first column to be narrow.
 TextColumn column = columns.get(0);
 column.setWidth(100.0);
 column.setSpaceAfter(20.0);

 // Set the second column to take the rest of the space available within the margins of the page.
 column = columns.get(1);
 column.setWidth(contentWidth - column.getWidth() - column.getSpaceAfter());

 builder.writeln("Narrow column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Wide column 2.");

 doc.save(getArtifactsDir() + "PageSetup.CustomColumnWidth.docx");
 
```

**Returns:**
double - Metin sütununun genişliği puan cinsinden.
### setSpaceAfter(double value) {#setSpaceAfter-double}
```
public void setSpaceAfter(double value)
```


Bu sütun ile sonraki sütun arasındaki boşluğu puan cinsinden ayarlar. Son sütun için gerekli değildir.

 **Examples:** 

Eşit olmayan aralıklı sütunlar oluşturmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 PageSetup pageSetup = builder.getPageSetup();

 TextColumnCollection columns = pageSetup.getTextColumns();
 columns.setEvenlySpaced(false);
 columns.setCount(2);

 // Determine the amount of room that we have available for arranging columns.
 double contentWidth = pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin();

 Assert.assertEquals(468.0d, contentWidth, 0.01d);

 // Set the first column to be narrow.
 TextColumn column = columns.get(0);
 column.setWidth(100.0);
 column.setSpaceAfter(20.0);

 // Set the second column to take the rest of the space available within the margins of the page.
 column = columns.get(1);
 column.setWidth(contentWidth - column.getWidth() - column.getSpaceAfter());

 builder.writeln("Narrow column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Wide column 2.");

 doc.save(getArtifactsDir() + "PageSetup.CustomColumnWidth.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Bu sütun ile sonraki sütun arasındaki boşluk puan cinsinden. |

### setWidth(double value) {#setWidth-double}
```
public void setWidth(double value)
```


Metin sütununun genişliğini nokta cinsinden ayarlar.

 **Examples:** 

Eşit olmayan aralıklı sütunlar oluşturmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 PageSetup pageSetup = builder.getPageSetup();

 TextColumnCollection columns = pageSetup.getTextColumns();
 columns.setEvenlySpaced(false);
 columns.setCount(2);

 // Determine the amount of room that we have available for arranging columns.
 double contentWidth = pageSetup.getPageWidth() - pageSetup.getLeftMargin() - pageSetup.getRightMargin();

 Assert.assertEquals(468.0d, contentWidth, 0.01d);

 // Set the first column to be narrow.
 TextColumn column = columns.get(0);
 column.setWidth(100.0);
 column.setSpaceAfter(20.0);

 // Set the second column to take the rest of the space available within the margins of the page.
 column = columns.get(1);
 column.setWidth(contentWidth - column.getWidth() - column.getSpaceAfter());

 builder.writeln("Narrow column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Wide column 2.");

 doc.save(getArtifactsDir() + "PageSetup.CustomColumnWidth.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | Metin sütununun genişliği puan cinsinden. |

