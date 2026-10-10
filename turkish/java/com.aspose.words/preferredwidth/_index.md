---
title: "PreferredWidth"
linktitle: "PreferredWidth"
second_title: "Aspose.Words Java için"
description: "Java'da bir tablo veya hücrenin tercih edilen genişliğini belirtmek için kullanılan bir değeri ve ölçü birimini temsil eder."
type: docs
weight: 550
url: /tr/java/com.aspose.words/preferredwidth/
---

**Inheritance:**
java.lang.Object
```
public class PreferredWidth
```

Bir tablo veya hücrenin tercih edilen genişliğini belirtmek için kullanılan bir değer ve ölçü birimini temsil eder.

Daha fazla bilgi için, [ Working with Tables ][Working with Tables] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Tercih edilen genişlik, yüzde, nokta sayısı veya özel bir \"none/auto\" değeri olarak belirtilebilir.

Bu sınıfın örnekleri değiştirilemezdir.

 **Examples:** 

Bir tablonun sayfa genişliğinin %50'sine otomatik sığdırılmasını nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell #1");
 builder.insertCell();
 builder.write("Cell #2");
 builder.insertCell();
 builder.write("Cell #3");

 table.setPreferredWidth(PreferredWidth.fromPercent(50.0));

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTableWithPreferredWidth.docx");
 
```

Tablo hücreleri için tercih edilen bir genişlik ayarlamanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // There are two ways of applying the "PreferredWidth" class to table cells.
 // 1 -  Set an absolute preferred width based on points:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(40.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.YELLOW);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 // 2 -  Set a relative preferred width based on percent of the table's width:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPercent(20.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.BLUE);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 builder.insertCell();

 // A cell with no preferred width specified will take up the rest of the available space.
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);

 // Each configuration of the "PreferredWidth" property creates a new object.
 Assert.assertNotEquals(table.getFirstRow().getCells().get(1).getCellFormat().getPreferredWidth().hashCode(),
         builder.getCellFormat().getPreferredWidth().hashCode());

 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Automatically sized cell.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
 
```


[Working with Tables]: https://docs.aspose.com/words/java/working-with-tables/
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [AUTO](#AUTO) | \"Tercih edilen genişlik belirtilmemiş\" değerini temsil eden bir örnek döndürür. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [equals(PreferredWidth other)](#equals-com.aspose.words.PreferredWidth) | Belirtilen [PreferredWidth](../../com.aspose.words/preferredwidth/) değerinin, mevcut [PreferredWidth](../../com.aspose.words/preferredwidth/) ile eşit olup olmadığını belirler. |
| [equals(Object obj)](#equals-java.lang.Object) | Belirtilen nesnenin, mevcut nesneyle değer olarak eşit olup olmadığını belirler. |
| [fromPercent(double percent)](#fromPercent-double) | Yüzde olarak belirtilen bir tercih genişliğini temsil eden yeni bir örnek döndüren bir oluşturma yöntemi. |
| [fromPoints(double points)](#fromPoints-double) | Nokta sayısı kullanılarak belirtilen bir tercih genişliğini temsil eden yeni bir örnek döndüren bir oluşturma yöntemi. |
| [getType()](#getType) | Bu tercih edilen genişlik değeri için kullanılan ölçü birimini alır. |
| [getValue()](#getValue) | Tercih edilen genişlik değerini alır. |
| [hashCode()](#hashCode) |  |
| [toString()](#toString) | Bu nesnenin değerini gösteren kullanıcı dostu bir dize döndürür. |
### AUTO {#AUTO}
```
public static PreferredWidth AUTO
```


\"Tercih edilen genişlik belirtilmemiş\" değerini temsil eden bir örnek döndürür.

 **Examples:** 

Tablo hücreleri için tercih edilen bir genişlik ayarlamanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // There are two ways of applying the "PreferredWidth" class to table cells.
 // 1 -  Set an absolute preferred width based on points:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(40.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.YELLOW);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 // 2 -  Set a relative preferred width based on percent of the table's width:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPercent(20.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.BLUE);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 builder.insertCell();

 // A cell with no preferred width specified will take up the rest of the available space.
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);

 // Each configuration of the "PreferredWidth" property creates a new object.
 Assert.assertNotEquals(table.getFirstRow().getCells().get(1).getCellFormat().getPreferredWidth().hashCode(),
         builder.getCellFormat().getPreferredWidth().hashCode());

 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Automatically sized cell.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
 
```

### equals(PreferredWidth other) {#equals-com.aspose.words.PreferredWidth}
```
public boolean equals(PreferredWidth other)
```


Belirtilen [PreferredWidth](../../com.aspose.words/preferredwidth/) değerinin, mevcut [PreferredWidth](../../com.aspose.words/preferredwidth/) ile eşit olup olmadığını belirler.

 **Examples:** 

Tablo hücreleri için tercih edilen bir genişlik ayarlamanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // There are two ways of applying the "PreferredWidth" class to table cells.
 // 1 -  Set an absolute preferred width based on points:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(40.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.YELLOW);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 // 2 -  Set a relative preferred width based on percent of the table's width:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPercent(20.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.BLUE);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 builder.insertCell();

 // A cell with no preferred width specified will take up the rest of the available space.
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);

 // Each configuration of the "PreferredWidth" property creates a new object.
 Assert.assertNotEquals(table.getFirstRow().getCells().get(1).getCellFormat().getPreferredWidth().hashCode(),
         builder.getCellFormat().getPreferredWidth().hashCode());

 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Automatically sized cell.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| other | [PreferredWidth](../../com.aspose.words/preferredwidth/) |  |

**Returns:**
boolean
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Belirtilen nesnenin, mevcut nesneyle değer olarak eşit olup olmadığını belirler.

 **Examples:** 

Tablo hücreleri için tercih edilen bir genişlik ayarlamanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // There are two ways of applying the "PreferredWidth" class to table cells.
 // 1 -  Set an absolute preferred width based on points:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(40.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.YELLOW);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 // 2 -  Set a relative preferred width based on percent of the table's width:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPercent(20.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.BLUE);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 builder.insertCell();

 // A cell with no preferred width specified will take up the rest of the available space.
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);

 // Each configuration of the "PreferredWidth" property creates a new object.
 Assert.assertNotEquals(table.getFirstRow().getCells().get(1).getCellFormat().getPreferredWidth().hashCode(),
         builder.getCellFormat().getPreferredWidth().hashCode());

 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Automatically sized cell.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### fromPercent(double percent) {#fromPercent-double}
```
public static PreferredWidth fromPercent(double percent)
```


Yüzde olarak belirtilen bir tercih genişliğini temsil eden yeni bir örnek döndüren bir oluşturma yöntemi.

 **Examples:** 

Bir tablonun sayfa genişliğinin %50'sine otomatik sığdırılmasını nasıl ayarlayacağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell #1");
 builder.insertCell();
 builder.write("Cell #2");
 builder.insertCell();
 builder.write("Cell #3");

 table.setPreferredWidth(PreferredWidth.fromPercent(50.0));

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTableWithPreferredWidth.docx");
 
```

Tablo hücreleri için tercih edilen bir genişlik ayarlamanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // There are two ways of applying the "PreferredWidth" class to table cells.
 // 1 -  Set an absolute preferred width based on points:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(40.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.YELLOW);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 // 2 -  Set a relative preferred width based on percent of the table's width:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPercent(20.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.BLUE);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 builder.insertCell();

 // A cell with no preferred width specified will take up the rest of the available space.
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);

 // Each configuration of the "PreferredWidth" property creates a new object.
 Assert.assertNotEquals(table.getFirstRow().getCells().get(1).getCellFormat().getPreferredWidth().hashCode(),
         builder.getCellFormat().getPreferredWidth().hashCode());

 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Automatically sized cell.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| yüzde | double | Değer 0 ile 100 arasında olmalıdır. |

**Returns:**
[PreferredWidth](../../com.aspose.words/preferredwidth/)
### fromPoints(double points) {#fromPoints-double}
```
public static PreferredWidth fromPoints(double points)
```


Nokta sayısı kullanılarak belirtilen bir tercih genişliğini temsil eden yeni bir örnek döndüren bir oluşturma yöntemi.

 **Examples:** 

Tablo hücreleri için tercih edilen bir genişlik ayarlamanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // There are two ways of applying the "PreferredWidth" class to table cells.
 // 1 -  Set an absolute preferred width based on points:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(40.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.YELLOW);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 // 2 -  Set a relative preferred width based on percent of the table's width:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPercent(20.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.BLUE);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 builder.insertCell();

 // A cell with no preferred width specified will take up the rest of the available space.
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);

 // Each configuration of the "PreferredWidth" property creates a new object.
 Assert.assertNotEquals(table.getFirstRow().getCells().get(1).getCellFormat().getPreferredWidth().hashCode(),
         builder.getCellFormat().getPreferredWidth().hashCode());

 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Automatically sized cell.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
 
```

Bir hücre için tercih edilen genişliği belirtirken birim dönüşüm araçlarının nasıl kullanılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(ConvertUtil.inchToPoint(3.0)));
 builder.insertCell();

 Assert.assertEquals(216.0d, table.getFirstRow().getFirstCell().getCellFormat().getPreferredWidth().getValue());
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| nokta | double | Değer 0 ile 22 inç arasında olmalıdır (22 \* 72 nokta). |

**Returns:**
[PreferredWidth](../../com.aspose.words/preferredwidth/)
### getType() {#getType}
```
public int getType()
```


Bu tercih edilen genişlik değeri için kullanılan ölçü birimini alır.

 **Examples:** 

Bir tablo hücresinin tercih edilen genişlik türünü ve değerini nasıl doğrulayacağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 Table table = doc.getFirstSection().getBody().getTables().get(0);
 Cell firstCell = table.getFirstRow().getFirstCell();

 Assert.assertEquals(PreferredWidthType.PERCENT, firstCell.getCellFormat().getPreferredWidth().getType());
 Assert.assertEquals(11.16d, firstCell.getCellFormat().getPreferredWidth().getValue());
 
```

**Returns:**
int - Bu tercih edilen genişlik değeri için kullanılan ölçü birimi. Döndürülen değer, [PreferredWidthType](../../com.aspose.words/preferredwidthtype/) sabitlerinden biridir.
### getValue() {#getValue}
```
public double getValue()
```


Tercih edilen genişlik değerini alır. Ölçü birimi, [getType()](../../com.aspose.words/preferredwidth/\#getType) özelliğinde belirtilir.

 **Examples:** 

Bir tablo hücresinin tercih edilen genişlik türünü ve değerini nasıl doğrulayacağınızı gösterir.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 Table table = doc.getFirstSection().getBody().getTables().get(0);
 Cell firstCell = table.getFirstRow().getFirstCell();

 Assert.assertEquals(PreferredWidthType.PERCENT, firstCell.getCellFormat().getPreferredWidth().getType());
 Assert.assertEquals(11.16d, firstCell.getCellFormat().getPreferredWidth().getValue());
 
```

**Returns:**
double - Tercih edilen genişlik değeri.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### toString() {#toString}
```
public String toString()
```


Bu nesnenin değerini gösteren kullanıcı dostu bir dize döndürür.

 **Examples:** 

Tablo hücreleri için tercih edilen bir genişlik ayarlamanın nasıl yapılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // There are two ways of applying the "PreferredWidth" class to table cells.
 // 1 -  Set an absolute preferred width based on points:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(40.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.YELLOW);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 // 2 -  Set a relative preferred width based on percent of the table's width:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPercent(20.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.BLUE);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 builder.insertCell();

 // A cell with no preferred width specified will take up the rest of the available space.
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);

 // Each configuration of the "PreferredWidth" property creates a new object.
 Assert.assertNotEquals(table.getFirstRow().getCells().get(1).getCellFormat().getPreferredWidth().hashCode(),
         builder.getCellFormat().getPreferredWidth().hashCode());

 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Automatically sized cell.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
 
```

**Returns:**
java.lang.String
