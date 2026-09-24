---
title: "DataSet"
linktitle: "DataSet"
second_title: "Aspose.Words Java için"
description: "Java'da bellekte tutulan bir veri önbelleğini temsil eder."
type: docs
weight: 24
url: /tr/java/com.aspose.words.net.system.data/dataset/
---

**Inheritance:**
java.lang.Object
```
public class DataSet
```

Bellek içi bir veri önbelleğini temsil eder.
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [DataSet()](#DataSet) | Yeni bir [DataSet](../../com.aspose.words.net.system.data/dataset/) sınıfı örneği başlatır. |
| [DataSet(Connection connection)](#DataSet-java.sql.Connection) | DataSet sınıfının yeni bir örneğini Connection'dan alınan verilerle başlatır. |
| [DataSet(Connection connection, String schemaName)](#DataSet-java.sql.Connection-java.lang.String) | DataSet sınıfının yeni bir örneğini Connection'dan alınan verilerle başlatır. |
| [DataSet(String dataSetName)](#DataSet-java.lang.String) | Verilen adla yeni bir [DataSet](../../com.aspose.words.net.system.data/dataset/) sınıfı örneği başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [IsSchemaWasRead()](#IsSchemaWasRead) |  |
| [clear()](#clear) | [DataSet](../../com.aspose.words.net.system.data/dataset/) içindeki tüm verileri, tüm tablolardaki tüm satırları kaldırarak temizler. |
| [close()](#close) |  |
| [getDataSetName()](#getDataSetName) | Mevcut [DataSet](../../com.aspose.words.net.system.data/dataset/) adını alır. |
| [getEnforceConstraints()](#getEnforceConstraints) | Herhangi bir güncelleme işlemi denendiğinde kısıtlama kurallarının uygulanıp uygulanmadığını gösteren bir değer alır. |
| [getNamespace()](#getNamespace) | [DataSet](../../com.aspose.words.net.system.data/dataset/) ad alanını alır. |
| [getRelations()](#getRelations) | Tabloları bağlayan ve üst tablolardan alt tablolara gezinmeye izin veren ilişki koleksiyonunu al. |
| [getTables()](#getTables) | [DataSet](../../com.aspose.words.net.system.data/dataset/) içinde bulunan tablo koleksiyonunu alır. |
| [isLocaleSpecified()](#isLocaleSpecified) |  |
| [readXml(InputStream stream)](#readXml-java.io.InputStream) | Belirtilen java.io.InputStream kullanılarak XML şemasını ve verileri [DataSet](../../com.aspose.words.net.system.data/dataset/) içine okur. |
| [readXml(InputStream xmlStream, System.Data.XmlReadMode mode)](#readXml-java.io.InputStream-com.aspose.words.net.System.Data.XmlReadMode) | Belirtilen java.io.InputStream ve [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) kullanılarak XML şemasını ve verileri DataSet içine okur. |
| [readXml(String fileName)](#readXml-java.lang.String) | Belirtilen dosya kullanılarak XML şemasını ve verileri [DataSet](../../com.aspose.words.net.system.data/dataset/) içine okur. |
| [readXml(String xmlPath, System.Data.XmlReadMode readMode)](#readXml-java.lang.String-com.aspose.words.net.System.Data.XmlReadMode) | Belirtilen dosya ve [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) kullanılarak XML şemasını ve verileri DataSet içine okur. |
| [readXmlSchema(InputStream stream)](#readXmlSchema-java.io.InputStream) | Belirtilen java.io.InputStream'ten XML şemasını [DataSet](../../com.aspose.words.net.system.data/dataset/) içine okur. |
| [readXmlSchema(String fileName)](#readXmlSchema-java.lang.String) | Belirtilen dosyadan XML şemasını [DataSet](../../com.aspose.words.net.system.data/dataset/) içine okur. |
| [reset()](#reset) | [DataSet](../../com.aspose.words.net.system.data/dataset/) öğesini orijinal durumuna sıfırlar. |
| [setDataSetName(String value)](#setDataSetName-java.lang.String) | Mevcut [DataSet](../../com.aspose.words.net.system.data/dataset/) adını ayarlar. |
| [setEnforceConstraints(boolean value)](#setEnforceConstraints-boolean) | Herhangi bir güncelleme işlemi denendiğinde kısıtlama kurallarının uygulanıp uygulanmadığını gösteren bir değeri ayarlar. |
| [setLocale(Locale locale)](#setLocale-java.util.Locale) | Tablodaki dizeleri karşılaştırmak için kullanılan yerel ayar bilgilerini ayarlar. |
### DataSet() {#DataSet}
```
public DataSet()
```


Yeni bir [DataSet](../../com.aspose.words.net.system.data/dataset/) sınıfı örneği başlatır.

### DataSet(Connection connection) {#DataSet-java.sql.Connection}
```
public DataSet(Connection connection)
```


DataSet sınıfının yeni bir örneğini Connection'dan alınan verilerle başlatır. Tablolar, İlişkiler, Kısıtlamalar ve Dizinler DataSet'e kopyalanacaktır.

Varsayılan olarak hiçbir şema adı kullanılmayacaktır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| connection | java.sql.Connection | DB verilerini içerir. |

### DataSet(Connection connection, String schemaName) {#DataSet-java.sql.Connection-java.lang.String}
```
public DataSet(Connection connection, String schemaName)
```


DataSet sınıfının yeni bir örneğini Connection'dan alınan verilerle başlatır. Tablolar, İlişkiler, Kısıtlamalar ve Dizinler DataSet'e kopyalanacaktır.

`DataSet dataSet = new DataSet(conn, "PUBLIC"); // HSQLDB`

veya

`DataSet dataSet = new DataSet(conn); // MYSQL's default schema name.`

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| connection | java.sql.Connection | DB verilerini içerir. |
| schemaName | java.lang.String | aktarılacak tabloları içerir. |

### DataSet(String dataSetName) {#DataSet-java.lang.String}
```
public DataSet(String dataSetName)
```


Verilen adla yeni bir [DataSet](../../com.aspose.words.net.system.data/dataset/) sınıfı örneği başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| dataSetName | java.lang.String | Adı [DataSet](../../com.aspose.words.net.system.data/dataset/). |

### IsSchemaWasRead() {#IsSchemaWasRead}
```
public boolean IsSchemaWasRead()
```




**Returns:**
boolean - şema okunduysa doğru
### clear() {#clear}
```
public void clear()
```


[DataSet](../../com.aspose.words.net.system.data/dataset/) içindeki tüm verileri, tüm tablolardaki tüm satırları kaldırarak temizler.

### close() {#close}
```
public void close()
```




### getDataSetName() {#getDataSetName}
```
public String getDataSetName()
```


Mevcut [DataSet](../../com.aspose.words.net.system.data/dataset/) adını alır.

**Returns:**
java.lang.String - Adı [DataSet](../../com.aspose.words.net.system.data/dataset/).
### getEnforceConstraints() {#getEnforceConstraints}
```
public boolean getEnforceConstraints()
```


Herhangi bir güncelleme işlemi denendiğinde kısıtlama kurallarının uygulanıp uygulanmadığını gösteren bir değer alır.

**Returns:**
boolean - kurallar uygulanıyorsa doğru; aksi takdirde yanlış. Varsayılan değer doğrudur.
### getNamespace() {#getNamespace}
```
public String getNamespace()
```


[DataSet](../../com.aspose.words.net.system.data/dataset/) ad alanını alır.

**Returns:**
java.lang.String - [DataSet](../../com.aspose.words.net.system.data/dataset/) ad alanı.
### getRelations() {#getRelations}
```
public System.Data.DataRelationCollection getRelations()
```


Tabloları bağlayan ve üst tablolardan alt tablolara gezinmeye izin veren ilişki koleksiyonunu al.

**Returns:**
[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) - A [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) that contains a collection of [DataRelation](../../com.aspose.words.net.system.data/datarelation/) objects. An empty collection is returned if no [DataRelation](../../com.aspose.words.net.system.data/datarelation/) objects exist.
### getTables() {#getTables}
```
public System.Data.DataTableCollection getTables()
```


[DataSet](../../com.aspose.words.net.system.data/dataset/) içinde bulunan tablo koleksiyonunu alır.

**Returns:**
[DataTableCollection](../../com.aspose.words.net.system.data/datatablecollection/) - The [DataTableCollection](../../com.aspose.words.net.system.data/datatablecollection/) contained by this [DataSet](../../com.aspose.words.net.system.data/dataset/). An empty collection is returned if no [DataTable](../../com.aspose.words.net.system.data/datatable/) objects exist.
### isLocaleSpecified() {#isLocaleSpecified}
```
public boolean isLocaleSpecified()
```




**Returns:**
boolean - yerel ayar ayarlandıysa doğru
### readXml(InputStream stream) {#readXml-java.io.InputStream}
```
public System.Data.XmlReadMode readXml(InputStream stream)
```


Belirtilen java.io.InputStream kullanılarak XML şemasını ve verileri [DataSet](../../com.aspose.words.net.system.data/dataset/) içine okur.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| stream | java.io.InputStream | java.io.InputStream'den türetilen bir nesne. |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) - The [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) used to read the data. The returned value is one of [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) constants.
### readXml(InputStream xmlStream, System.Data.XmlReadMode mode) {#readXml-java.io.InputStream-com.aspose.words.net.System.Data.XmlReadMode}
```
public System.Data.XmlReadMode readXml(InputStream xmlStream, System.Data.XmlReadMode mode)
```


Belirtilen java.io.InputStream ve [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) kullanılarak XML şemasını ve verileri DataSet içine okur.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| xmlStream | java.io.InputStream | Okunacak akış. |
| mode | [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) | [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) değerlerinden biri. |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) - The XmlReadMode used to read the data.
### readXml(String fileName) {#readXml-java.lang.String}
```
public System.Data.XmlReadMode readXml(String fileName)
```


Belirtilen dosya kullanılarak XML şemasını ve verileri [DataSet](../../com.aspose.words.net.system.data/dataset/) içine okur.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | java.lang.String | Okunacak dosya adı (yol dahil). |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) - The XmlReadMode used to read the data. The returned value is one of [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) constants.
### readXml(String xmlPath, System.Data.XmlReadMode readMode) {#readXml-java.lang.String-com.aspose.words.net.System.Data.XmlReadMode}
```
public System.Data.XmlReadMode readXml(String xmlPath, System.Data.XmlReadMode readMode)
```


Belirtilen dosya ve [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) kullanılarak XML şemasını ve verileri DataSet içine okur.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| xmlPath | java.lang.String | belirtilen dosya |
| readMode | [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) | [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) - mode which was used while reading
### readXmlSchema(InputStream stream) {#readXmlSchema-java.io.InputStream}
```
public void readXmlSchema(InputStream stream)
```


Belirtilen java.io.InputStream'ten XML şemasını [DataSet](../../com.aspose.words.net.system.data/dataset/) içine okur.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| stream | java.io.InputStream | Okunacak java.io.InputStream. |

### readXmlSchema(String fileName) {#readXmlSchema-java.lang.String}
```
public void readXmlSchema(String fileName)
```


Belirtilen dosyadan XML şemasını [DataSet](../../com.aspose.words.net.system.data/dataset/) içine okur.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| fileName | java.lang.String | Okunacak dosya adı (yol dahil). |

### reset() {#reset}
```
public void reset()
```


Orijinal durumuna [DataSet](../../com.aspose.words.net.system.data/dataset/) sıfırlar. Alt sınıflar, bir [DataSet](../../com.aspose.words.net.system.data/dataset/)'i orijinal durumuna geri yüklemek için [reset()](../../com.aspose.words.net.system.data/dataset/\#reset) metodunu geçersiz kılmalıdır.

### setDataSetName(String value) {#setDataSetName-java.lang.String}
```
public void setDataSetName(String value)
```


Mevcut [DataSet](../../com.aspose.words.net.system.data/dataset/) adını ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | java.lang.String | Adı [DataSet](../../com.aspose.words.net.system.data/dataset/). |

### setEnforceConstraints(boolean value) {#setEnforceConstraints-boolean}
```
public void setEnforceConstraints(boolean value)
```


Herhangi bir güncelleme işlemi denendiğinde kısıtlama kurallarının uygulanıp uygulanmadığını gösteren bir değeri ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Kurallar uygulanıyorsa doğru; aksi takdirde yanlış. Varsayılan değer doğrudur. |

### setLocale(Locale locale) {#setLocale-java.util.Locale}
```
public void setLocale(Locale locale)
```


Tablodaki dizeleri karşılaştırmak için kullanılan yerel ayar bilgilerini ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| locale | java.util.Locale | bu veri kümesinin |

