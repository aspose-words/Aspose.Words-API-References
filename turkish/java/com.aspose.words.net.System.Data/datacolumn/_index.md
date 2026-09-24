---
title: "DataColumn"
linktitle: "DataColumn"
second_title: "Aspose.Words Java için"
description: "Java'da bir DataTable içindeki sütunun şemasını temsil eder."
type: docs
weight: 14
url: /tr/java/com.aspose.words.net.system.data/datacolumn/
---

**Inheritance:**
java.lang.Object
```
public class DataColumn
```

Bir [DataTable](../../com.aspose.words.net.system.data/datatable/) içindeki sütunun şemasını temsil eder.
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [DataColumn()](#DataColumn) | Bir [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) sınıfının yeni bir örneğini string türünde başlatır. |
| [DataColumn(String columnName)](#DataColumn-java.lang.String) | Belirtilen sütun adını kullanarak, [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) sınıfının yeni bir örneğini string türünde başlatır. |
| [DataColumn(String name, System.Data.DataTable table)](#DataColumn-java.lang.String-com.aspose.words.net.System.Data.DataTable) | Belirtilen sütun adını ve ait olduğu tabloyu kullanarak @\{link DataColumn\} sınıfının yeni bir örneğini başlatır. |
| [DataColumn(String columnName, Class dataType)](#DataColumn-java.lang.String-java.lang.Class) | Belirtilen sütun adı ve veri tipini kullanarak [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) sınıfının yeni bir örneğini başlatır. |
| [DataColumn(String name, Class type, System.Data.DataTable table)](#DataColumn-java.lang.String-java.lang.Class-com.aspose.words.net.System.Data.DataTable) | Belirtilen sütun adı, veri tipi ve ait olduğu veri tablosunu kullanarak [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) sınıfının yeni bir örneğini başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [areColumnSetsTheSame(System.Data.DataColumn[] columnSet, System.Data.DataColumn[] compareSet)](#areColumnSetsTheSame-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn) |  |
| [getAllowDBNull()](#getAllowDBNull) | Bu sütunda, tabloya ait satırlar için null değerlerin izinli olup olmadığını gösteren bir değeri alır. |
| [getAutoIncrement()](#getAutoIncrement) | Tabloya eklenen yeni satırlar için sütunun değerini otomatik olarak artırıp artırmadığını gösteren bir değeri alır. |
| [getAutoIncrementSeed()](#getAutoIncrementSeed) | Özelliği [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) true olarak ayarlanmış bir sütun için başlangıç değerini alır. |
| [getAutoIncrementStep()](#getAutoIncrementStep) | Özelliği [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) true olarak ayarlanmış bir sütun için kullanılan artışı alır. |
| [getCaption()](#getCaption) | Sütunun başlığını alır. |
| [getColumnMapping()](#getColumnMapping) | Sütunun [MappingType](../../com.aspose.words.net.system.data/mappingtype/) değerini alır. |
| [getColumnName()](#getColumnName) | Sütunun [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) içindeki adını alır. |
| [getDataType()](#getDataType) | Sütunda depolanan veri tipini alır. |
| [getDefaultValue()](#getDefaultValue) | Yeni satırlar oluştururken sütun için varsayılan değeri alır. |
| [getExpression()](#getExpression) | Satırları filtrelemek, bir sütundaki değerleri hesaplamak veya bir toplama sütunu oluşturmak için kullanılan ifadeyi alır. |
| [getMaxLength()](#getMaxLength) | Metin sütununun azami uzunluğunu alır. |
| [getNamespace()](#getNamespace) | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) öğesinin ad alanını alır. |
| [getOrdinal()](#getOrdinal) | Sütunun [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) içindeki konumunu alır. |
| [getPrefix()](#getPrefix) | [DataTable](../../com.aspose.words.net.system.data/datatable/) öğesinin ad alanına takma ad veren bir XML önekini alır. |
| [getReadOnly()](#getReadOnly) | Sütunun bir satır tabloya eklendiği anda değişikliklere izin verip vermediğini gösteren bir değeri alır. |
| [getTable()](#getTable) | Sütunun ait olduğu [DataTable](../../com.aspose.words.net.system.data/datatable/) öğesini alır. |
| [getUnique()](#getUnique) | Sütundaki her satırın değerlerinin benzersiz olması gerektiğini gösteren bir değeri alır. |
| [isReadOnly()](#isReadOnly) |  |
| [isUnique()](#isUnique) |  |
| [setAllowDBNull(boolean value)](#setAllowDBNull-boolean) | Tabloya ait satırlar için bu sütunda null değerlerine izin verilip verilmediğini gösteren bir değeri ayarlar. |
| [setAutoIncrement(boolean value)](#setAutoIncrement-boolean) | Tabloya eklenen yeni satırlar için sütunun değerini otomatik olarak artırıp artırmadığını gösteren bir değeri ayarlar. |
| [setAutoIncrementSeed(long value)](#setAutoIncrementSeed-long) | Özelliği [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) true olarak ayarlanmış bir sütun için başlangıç değerini ayarlar. |
| [setAutoIncrementStep(long value)](#setAutoIncrementStep-long) | Özelliği [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) true olarak ayarlanmış bir sütun için kullanılan artışı ayarlar. |
| [setCaption(String value)](#setCaption-java.lang.String) | Sütunun başlığını ayarlar. |
| [setColumnMapping(int value)](#setColumnMapping-int) | Sütunun [MappingType](../../com.aspose.words.net.system.data/mappingtype/) değerini ayarlar. |
| [setColumnName(String value)](#setColumnName-java.lang.String) | Sütunun [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) içindeki adını ayarlar. |
| [setDataType(Class value)](#setDataType-java.lang.Class) | Sütunda depolanan veri tipini ayarlar. |
| [setDefaultValue(Object value)](#setDefaultValue-java.lang.Object) | Yeni satırlar oluştururken sütun için varsayılan değeri ayarlar. |
| [setMaxLength(int value)](#setMaxLength-int) | Metin sütununun maksimum uzunluğunu ayarlar. |
| [setNamespace(String value)](#setNamespace-java.lang.String) | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). öğesinin ad alanını ayarlar. |
| [setOrdinal(int ordinal)](#setOrdinal-int) | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). öğesinin sıra numarasını veya konumunu belirtilen sıra numarasına veya konuma değiştirir. |
| [setPrefix(String value)](#setPrefix-java.lang.String) | [DataTable](../../com.aspose.words.net.system.data/datatable/). öğesinin ad alanına takma ad veren bir XML önekini ayarlar. |
| [setReadOnly(boolean value)](#setReadOnly-boolean) | Sütunun, tabloya bir satır eklendiği anda değişikliklere izin verip vermediğini gösteren bir değeri ayarlar. |
| [setUnique(boolean value)](#setUnique-boolean) | Sütunun her satırındaki değerlerin benzersiz olması gerekip gerekmediğini gösteren bir değeri ayarlar. |
| [toString()](#toString) | Sütunun [getExpression()](../../com.aspose.words.net.system.data/datacolumn/\\#getExpression) değerini (varsa) alır. |
### DataColumn() {#DataColumn}
```
public DataColumn()
```


Bir [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) sınıfının yeni bir örneğini string türünde başlatır.

### DataColumn(String columnName) {#DataColumn-java.lang.String}
```
public DataColumn(String columnName)
```


Belirtilen sütun adını kullanarak, [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) sınıfının yeni bir örneğini string türünde başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| columnName | java.lang.String | Oluşturulacak sütunun adını temsil eden bir dizedir. Null veya boş bir dize (\"\"), ayarlanırsa, sütun koleksiyonuna eklendiğinde varsayılan bir ad atanır. |

### DataColumn(String name, System.Data.DataTable table) {#DataColumn-java.lang.String-com.aspose.words.net.System.Data.DataTable}
```
public DataColumn(String name, System.Data.DataTable table)
```


Belirtilen sütun adını ve ait olduğu tabloyu kullanarak @\{link DataColumn\} sınıfının yeni bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | DataColumn adı |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | bu sütunun ait olduğu tablo |

### DataColumn(String columnName, Class dataType) {#DataColumn-java.lang.String-java.lang.Class}
```
public DataColumn(String columnName, Class dataType)
```


Belirtilen sütun adı ve veri tipini kullanarak [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) sınıfının yeni bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| columnName | java.lang.String | Oluşturulacak sütunun adını temsil eden bir dizedir. Null veya boş bir dize (\"\"), ayarlanırsa, sütun koleksiyonuna eklendiğinde varsayılan bir ad atanır. |
| dataType | java.lang.Class | Desteklenen bir [getDataType()](../../com.aspose.words.net.system.data/datacolumn/\\#getDataType) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\\#setDataType-java.lang.Class). |

### DataColumn(String name, Class type, System.Data.DataTable table) {#DataColumn-java.lang.String-java.lang.Class-com.aspose.words.net.System.Data.DataTable}
```
public DataColumn(String name, Class type, System.Data.DataTable table)
```


Belirtilen sütun adı, veri tipi ve ait olduğu veri tablosunu kullanarak [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) sınıfının yeni bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | DataColumn adı |
| tip | java.lang.Class | veri türü |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | bu sütunun ait olduğu tablo |

### areColumnSetsTheSame(System.Data.DataColumn[] columnSet, System.Data.DataColumn[] compareSet) {#areColumnSetsTheSame-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn}
```
public static boolean areColumnSetsTheSame(System.Data.DataColumn[] columnSet, System.Data.DataColumn[] compareSet)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| columnSet | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) |  |
| compareSet | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) |  |

**Returns:**
boolean
### getAllowDBNull() {#getAllowDBNull}
```
public boolean getAllowDBNull()
```


Bu sütunda, tabloya ait satırlar için null değerlerin izinli olup olmadığını gösteren bir değeri alır.

**Returns:**
boolean - null değerlerine izin veriliyorsa true; aksi takdirde false. Varsayılan değer true.
### getAutoIncrement() {#getAutoIncrement}
```
public boolean getAutoIncrement()
```


Tabloya eklenen yeni satırlar için sütunun değerini otomatik olarak artırıp artırmadığını gösteren bir değeri alır.

**Returns:**
boolean - sütun değeri otomatik olarak artıyorsa true; aksi takdirde false. Varsayılan değer false.
### getAutoIncrementSeed() {#getAutoIncrementSeed}
```
public long getAutoIncrementSeed()
```


Özelliği [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) true olarak ayarlanmış bir sütun için başlangıç değerini alır.

**Returns:**
long - [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\\#setAutoIncrement-boolean) özelliği için başlangıç değeri.
### getAutoIncrementStep() {#getAutoIncrementStep}
```
public long getAutoIncrementStep()
```


Özelliği [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) true olarak ayarlanmış bir sütun için kullanılan artışı alır.

**Returns:**
long - sütun değerinin otomatik olarak artırıldığı sayı. Varsayılan değer 1.
### getCaption() {#getCaption}
```
public String getCaption()
```


Sütunun başlığını alır.

**Returns:**
java.lang.String - sütunun başlığı. Ayarlanmamışsa, [getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\\#getColumnName) / [setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\\#setColumnName-java.lang.String) değerini döndürür.
### getColumnMapping() {#getColumnMapping}
```
public int getColumnMapping()
```


Sütunun [MappingType](../../com.aspose.words.net.system.data/mappingtype/) değerini alır.

**Returns:**
int - [MappingType](../../com.aspose.words.net.system.data/mappingtype/) değerlerinden biri. Döndürülen değer, [MappingType](../../com.aspose.words.net.system.data/mappingtype/) sabitlerinden biridir.
### getColumnName() {#getColumnName}
```
public String getColumnName()
```


Sütunun [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) içindeki adını alır.

**Returns:**
java.lang.String - Sütunun adı.
### getDataType() {#getDataType}
```
public Class getDataType()
```


Sütunda depolanan veri tipini alır.

**Returns:**
java.lang.Class - sütun veri tipini temsil eden bir java.lang.Class nesnesi.
### getDefaultValue() {#getDefaultValue}
```
public Object getDefaultValue()
```


Yeni satırlar oluştururken sütun için varsayılan değeri alır.

**Returns:**
java.lang.Object - sütunun [getDataType()](../../com.aspose.words.net.system.data/datacolumn/\\#getDataType) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\\#setDataType-java.lang.Class) değerine uygun bir değer.
### getExpression() {#getExpression}
```
public String getExpression()
```


Satırları filtrelemek, bir sütundaki değerleri hesaplamak veya bir toplama sütunu oluşturmak için kullanılan ifadeyi alır.

**Returns:**
java.lang.String - bir sütunun değerini hesaplamak veya toplu bir sütun oluşturmak için bir ifade. Bir ifadenin dönüş tipi, sütunun [getDataType()](../../com.aspose.words.net.system.data/datacolumn/\\#getDataType) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\\#setDataType-java.lang.Class) tarafından belirlenir.
### getMaxLength() {#getMaxLength}
```
public int getMaxLength()
```


Metin sütununun azami uzunluğunu alır.

**Returns:**
int - sütunun karakter cinsinden maksimum uzunluğu. Sütunun maksimum uzunluğu yoksa, değer -1 (varsayılan) olur.
### getNamespace() {#getNamespace}
```
public String getNamespace()
```


[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) öğesinin ad alanını alır.

**Returns:**
java.lang.String - [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). öğesinin ad alanı.
### getOrdinal() {#getOrdinal}
```
public int getOrdinal()
```


Sütunun [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) içindeki konumunu alır.

**Returns:**
int - sütunun konumu. Sütun bir koleksiyonun üyesi değilse -1 döner.
### getPrefix() {#getPrefix}
```
public String getPrefix()
```


[DataTable](../../com.aspose.words.net.system.data/datatable/) öğesinin ad alanına takma ad veren bir XML önekini alır.

**Returns:**
java.lang.String - [DataTable](../../com.aspose.words.net.system.data/datatable/). ad alanı için XML öneki.
### getReadOnly() {#getReadOnly}
```
public boolean getReadOnly()
```


Sütunun bir satır tabloya eklendiği anda değişikliklere izin verip vermediğini gösteren bir değeri alır.

**Returns:**
boolean - sütun yalnızca okunabilir ise true; aksi takdirde false. Varsayılan false'tur.
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Sütunun ait olduğu [DataTable](../../com.aspose.words.net.system.data/datatable/) öğesini alır.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The [DataTable](../../com.aspose.words.net.system.data/datatable/) that the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) belongs to.
### getUnique() {#getUnique}
```
public boolean getUnique()
```


Sütundaki her satırın değerlerinin benzersiz olması gerektiğini gösteren bir değeri alır.

**Returns:**
boolean - değer benzersiz olmalı ise true; aksi takdirde false. Varsayılan false'tur.
### isReadOnly() {#isReadOnly}
```
public boolean isReadOnly()
```




**Returns:**
boolean
### isUnique() {#isUnique}
```
public boolean isUnique()
```




**Returns:**
boolean
### setAllowDBNull(boolean value) {#setAllowDBNull-boolean}
```
public void setAllowDBNull(boolean value)
```


Tabloya ait satırlar için bu sütunda null değerlerine izin verilip verilmediğini gösteren bir değeri ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | null değerlerin izin verilmesi durumunda true; aksi takdirde false. Varsayılan true'tur. |

### setAutoIncrement(boolean value) {#setAutoIncrement-boolean}
```
public void setAutoIncrement(boolean value)
```


Tabloya eklenen yeni satırlar için sütunun değerini otomatik olarak artırıp artırmadığını gösteren bir değeri ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | sütunun değeri otomatik olarak artıyorsa true; aksi takdirde false. Varsayılan false'tur. |

### setAutoIncrementSeed(long value) {#setAutoIncrementSeed-long}
```
public void setAutoIncrementSeed(long value)
```


Özelliği [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) true olarak ayarlanmış bir sütun için başlangıç değerini ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | long | Bu özellik için başlangıç değeri: [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean). |

### setAutoIncrementStep(long value) {#setAutoIncrementStep-long}
```
public void setAutoIncrementStep(long value)
```


Özelliği [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) true olarak ayarlanmış bir sütun için kullanılan artışı ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | long | Sütunun değeri otomatik olarak artırılan sayı. Varsayılan 1'dir. |

### setCaption(String value) {#setCaption-java.lang.String}
```
public void setCaption(String value)
```


Sütunun başlığını ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | java.lang.String | Sütunun başlığı. Ayarlanmamışsa, [getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String) değerini döndürür. |

### setColumnMapping(int value) {#setColumnMapping-int}
```
public void setColumnMapping(int value)
```


Sütunun [MappingType](../../com.aspose.words.net.system.data/mappingtype/) değerini ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | [MappingType](../../com.aspose.words.net.system.data/mappingtype/) değerlerinden biri. Değer, [MappingType](../../com.aspose.words.net.system.data/mappingtype/) sabitlerinden biri olmalıdır. |

### setColumnName(String value) {#setColumnName-java.lang.String}
```
public void setColumnName(String value)
```


Sütunun [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) içindeki adını ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Sütunun adı. |

### setDataType(Class value) {#setDataType-java.lang.Class}
```
public void setDataType(Class value)
```


Sütunda depolanan veri tipini ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.Class | Sütun veri tipini temsil eden bir java.lang.Class nesnesi. |

### setDefaultValue(Object value) {#setDefaultValue-java.lang.Object}
```
public void setDefaultValue(Object value)
```


Yeni satırlar oluştururken sütun için varsayılan değeri ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | java.lang.Object | Sütunun [getDataType()](../../com.aspose.words.net.system.data/datacolumn/\#getDataType) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\#setDataType-java.lang.Class) değerine uygun bir değer. |

### setMaxLength(int value) {#setMaxLength-int}
```
public void setMaxLength(int value)
```


Metin sütununun maksimum uzunluğunu ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Sütunun karakter cinsinden maksimum uzunluğu. Sütunun maksimum uzunluğu yoksa, değer -1'dir (varsayılan). |

### setNamespace(String value) {#setNamespace-java.lang.String}
```
public void setNamespace(String value)
```


[DataColumn](../../com.aspose.words.net.system.data/datacolumn/). öğesinin ad alanını ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | java.lang.String | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) ad alanı. |

### setOrdinal(int ordinal) {#setOrdinal-int}
```
public void setOrdinal(int ordinal)
```


[DataColumn](../../com.aspose.words.net.system.data/datacolumn/). öğesinin sıra numarasını veya konumunu belirtilen sıra numarasına veya konuma değiştirir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sıra | int | Belirtilen sıra numarası. |

### setPrefix(String value) {#setPrefix-java.lang.String}
```
public void setPrefix(String value)
```


[DataTable](../../com.aspose.words.net.system.data/datatable/). öğesinin ad alanına takma ad veren bir XML önekini ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | java.lang.String | [DataTable](../../com.aspose.words.net.system.data/datatable/) ad alanı için XML öneki. |

### setReadOnly(boolean value) {#setReadOnly-boolean}
```
public void setReadOnly(boolean value)
```


Sütunun, tabloya bir satır eklendiği anda değişikliklere izin verip vermediğini gösteren bir değeri ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | sütun yalnızca okunabilir ise true; aksi takdirde false. Varsayılan false'tur. |

### setUnique(boolean value) {#setUnique-boolean}
```
public void setUnique(boolean value)
```


Sütunun her satırındaki değerlerin benzersiz olması gerekip gerekmediğini gösteren bir değeri ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | değer benzersiz olmalı ise true; aksi takdirde false. Varsayılan false'tur. |

### toString() {#toString}
```
public String toString()
```


Sütunun [getExpression()](../../com.aspose.words.net.system.data/datacolumn/\\#getExpression) değerini (varsa) alır.

**Returns:**
java.lang.String - Özellik ayarlanmışsa [getExpression()](../../com.aspose.words.net.system.data/datacolumn/\#getExpression) değeri; aksi takdirde [getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String) özelliği.
