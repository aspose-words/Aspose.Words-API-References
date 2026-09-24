---
title: "TextColumnCollection"
linktitle: "TextColumnCollection"
second_title: "Aspose.Words Java için"
description: "Java'da bir belgenin bölümündeki tüm metin sütunlarını temsil eden TextColumn nesnelerinin bir koleksiyonu."
type: docs
weight: 671
url: /tr/java/com.aspose.words/textcolumncollection/
---

**Inheritance:**
java.lang.Object
```
public class TextColumnCollection
```

Bir belgenin bölümündeki tüm metin sütunlarını temsil eden [TextColumn](../../com.aspose.words/textcolumn/) nesnelerinin bir koleksiyonu.

Daha fazla bilgi edinmek için, [ Working with Sections ][Working with Sections] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Metin sütunlarının sayısını ayarlamak için [setCount(int)](../../com.aspose.words/textcolumncollection/\#setCount-int) kullanın.

Tüm sütunların eşit genişlikte ve eşit aralıkta olmasını sağlamak için, [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) değerini  true  olarak ayarlayın ve sütunlar arasındaki boşluk miktarını [getSpacing()](../../com.aspose.words/textcolumncollection/\#getSpacing) / [setSpacing(double)](../../com.aspose.words/textcolumncollection/\#setSpacing-double) ile belirtin. MS Word otomatik olarak sütun genişliklerini hesaplayacaktır.

Eğer [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) değerini  false  olarak ayarladıysanız, her sütun için genişlik ve boşluğu ayrı ayrı belirtmeniz gerekir. Tek tek [TextColumn](../../com.aspose.words/textcolumn/) nesnelerine erişmek için indeksleyiciyi kullanın.

Özel sütun genişlikleri kullanırken, tüm sütun genişlikleri ve aralarındaki boşlukların toplamının sayfa genişliğinden sol ve sağ sayfa kenar boşlukları çıkarıldıktan sonra kalan değere eşit olduğundan emin olun.

 **Examples:** 

Bir bölümde birden fazla eşit aralıklı sütun oluşturmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```


[Working with Sections]: https://docs.aspose.com/words/java/working-with-sections/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get(int index)](#get-int) | Belirtilen indeksteki bir metin sütununu döndürür. |
| [getCount()](#getCount) | Bir belgenin bölümündeki sütun sayısını alır. |
| [getEvenlySpaced()](#getEvenlySpaced) | Metin sütunları eşit genişlikte ve eşit aralıkta ise true döner. |
| [getLineBetween()](#getLineBetween) | true olduğunda, sütunlar arasında dikey bir çizgi ekler. |
| [getSpacing()](#getSpacing) | Sütunlar eşit aralıkta olduğunda, her sütun arasındaki boşluk miktarını nokta cinsinden alır veya ayarlar. |
| [getWidth()](#getWidth) | Sütunlar eşit aralıkta olduğunda, sütunların genişliğini alır. |
| [setCount(int newCount)](#setCount-int) | Metni belirtilen sayıda metin sütununa düzenler. |
| [setEvenlySpaced(boolean value)](#setEvenlySpaced-boolean) | Metin sütunları eşit genişlikte ve eşit aralıkta ise true döner. |
| [setLineBetween(boolean value)](#setLineBetween-boolean) | true olduğunda, sütunlar arasında dikey bir çizgi ekler. |
| [setSpacing(double value)](#setSpacing-double) | Sütunlar eşit aralıkta olduğunda, her sütun arasındaki boşluk miktarını nokta cinsinden alır veya ayarlar. |
### get(int index) {#get-int}
```
public TextColumn get(int index)
```


Belirtilen indeksteki bir metin sütununu döndürür.

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
| indeks | int |  |

**Returns:**
[TextColumn](../../com.aspose.words/textcolumn/) - A text column at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Bir belgenin bölümündeki sütun sayısını alır.

 **Examples:** 

Bir bölümde birden fazla eşit aralıklı sütun oluşturmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```

**Returns:**
int - Bir belgenin bölümündeki sütun sayısı.
### getEvenlySpaced() {#getEvenlySpaced}
```
public boolean getEvenlySpaced()
```


Metin sütunları eşit genişlikte ve eşit aralıkta ise true döner.

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
boolean - İlgili  boolean  değeri.
### getLineBetween() {#getLineBetween}
```
public boolean getLineBetween()
```


true olduğunda, sütunlar arasında dikey bir çizgi ekler.

 **Examples:** 

Sütunları dikey bir çizgiyle ayırmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Configure the current section's PageSetup object to divide the text into several columns.
 // Set the "LineBetween" property to "true" to put a dividing line between columns.
 // Set the "LineBetween" property to "false" to leave the space between columns blank.
 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setLineBetween(lineBetween);
 columns.setCount(3);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 3.");

 doc.save(getArtifactsDir() + "PageSetup.VerticalLineBetweenColumns.docx");
 
```

**Returns:**
boolean - İlgili  boolean  değeri.
### getSpacing() {#getSpacing}
```
public double getSpacing()
```


Sütunlar eşit aralıkta olduğunda, her sütun arasındaki boşluk miktarını nokta cinsinden alır veya ayarlar.

 **Remarks:** 

Yalnızca [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) true olarak ayarlandığında etkili olur.

 **Examples:** 

Bir bölümde birden fazla eşit aralıklı sütun oluşturmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```

**Returns:**
double - İlgili  double  değeri.
### getWidth() {#getWidth}
```
public double getWidth()
```


Sütunlar eşit aralıkta olduğunda, sütunların genişliğini alır.

 **Remarks:** 

Yalnızca [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) true olarak ayarlandığında etkili olur.

 **Examples:** 

Bir bölümde birden fazla eşit aralıklı sütun oluşturmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```

**Returns:**
double - İlgili  double  değeri.
### setCount(int newCount) {#setCount-int}
```
public void setCount(int newCount)
```


Metni belirtilen sayıda metin sütununa düzenler.

 **Remarks:** 

Eğer [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) false ise ve sütun sayısını artırırsanız, yeni [TextColumn](../../com.aspose.words/textcolumn/) nesneleri sıfır genişlik ve boşlukla oluşturulur. Yeni sütunlar için genişlik ve boşluğu ayarlamanız gerekir.

 **Examples:** 

Bir bölümde birden fazla eşit aralıklı sütun oluşturmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| newCount | int | Metnin düzenleneceği sütun sayısı. |

### setEvenlySpaced(boolean value) {#setEvenlySpaced-boolean}
```
public void setEvenlySpaced(boolean value)
```


Metin sütunları eşit genişlikte ve eşit aralıkta ise true döner.

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
| değer | boolean | İlgili  boolean  değeri. |

### setLineBetween(boolean value) {#setLineBetween-boolean}
```
public void setLineBetween(boolean value)
```


true olduğunda, sütunlar arasında dikey bir çizgi ekler.

 **Examples:** 

Sütunları dikey bir çizgiyle ayırmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Configure the current section's PageSetup object to divide the text into several columns.
 // Set the "LineBetween" property to "true" to put a dividing line between columns.
 // Set the "LineBetween" property to "false" to leave the space between columns blank.
 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setLineBetween(lineBetween);
 columns.setCount(3);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 3.");

 doc.save(getArtifactsDir() + "PageSetup.VerticalLineBetweenColumns.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setSpacing(double value) {#setSpacing-double}
```
public void setSpacing(double value)
```


Sütunlar eşit aralıkta olduğunda, her sütun arasındaki boşluk miktarını nokta cinsinden alır veya ayarlar.

 **Remarks:** 

Yalnızca [getEvenlySpaced()](../../com.aspose.words/textcolumncollection/\#getEvenlySpaced) / [setEvenlySpaced(boolean)](../../com.aspose.words/textcolumncollection/\#setEvenlySpaced-boolean) true olarak ayarlandığında etkili olur.

 **Examples:** 

Bir bölümde birden fazla eşit aralıklı sütun oluşturmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 TextColumnCollection columns = builder.getPageSetup().getTextColumns();
 columns.setSpacing(100.0);
 columns.setCount(2);

 builder.writeln("Column 1.");
 builder.insertBreak(BreakType.COLUMN_BREAK);
 builder.writeln("Column 2.");

 doc.save(getArtifactsDir() + "PageSetup.ColumnsSameWidth.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | double | İlgili  double  değeri. |

