---
title: "XmlReadMode"
linktitle: "XmlReadMode"
second_title: "Aspose.Words Java için"
description: "Java'da XML verilerini ve ilişkisel şemayı bir DataSet'e nasıl okuyacağını belirtir."
type: docs
weight: 37
url: /tr/java/com.aspose.words.net.system.data/xmlreadmode/
---

**Inheritance:**
java.lang.Object, java.lang.Enum
```
public enum XmlReadMode extends Enum<System.Data.XmlReadMode>
```

XML verilerini ve ilişkisel şemayı bir [DataSet](../../com.aspose.words.net.system.data/dataset/) içine nasıl okuyacağını belirtir.
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [AUTO](#AUTO) | Varsayılan. |
| [DIFF_GRAM](#DIFF-GRAM) | Bir DiffGram okur, DiffGram'dan gelen değişiklikleri [DataSet](../../com.aspose.words.net.system.data/dataset/) üzerine uygular ve [DataRow.getRowState()](../../com.aspose.words.net.system.data/datarow/\#getRowState) değerlerini korur. |
| [FRAGMENT](#FRAGMENT) | SQL Server örneği üzerinde FOR XML sorgularının ürettiği gibi XML parçacıklarını okur. |
| [IGNORE_SCHEMA](#IGNORE-SCHEMA) | Herhangi bir satır içi şemayı yok sayar ve verileri mevcut [DataSet](../../com.aspose.words.net.system.data/dataset/) şemasına okur. |
| [INFER_SCHEMA](#INFER-SCHEMA) | Herhangi bir satır içi şemayı yok sayar, şemayı veriden çıkarır ve verileri yükler. |
| [INFER_TYPED_SCHEMA](#INFER-TYPED-SCHEMA) | Herhangi bir satır içi şemayı yok sayar, veriden güçlü tipli bir şema çıkarır ve verileri yükler. |
| [READ_SCHEMA](#READ-SCHEMA) | Herhangi bir satır içi şemayı okur ve verileri yükler. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [<T>valueOf(Class<T> arg0, String arg1)](#-T-valueOf-java.lang.Class-T--java.lang.String) |  |
| [compareTo(E arg0)](#compareTo-E) |  |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getDeclaringClass()](#getDeclaringClass) |  |
| [hashCode()](#hashCode) |  |
| [name()](#name) |  |
| [ordinal()](#ordinal) |  |
| [toString()](#toString) |  |
| [valueOf(String name)](#valueOf-java.lang.String) |  |
| [values()](#values) |  |
### AUTO {#AUTO}
```
public static final System.Data.XmlReadMode AUTO
```


Varsayılan.

### DIFF_GRAM {#DIFF-GRAM}
```
public static final System.Data.XmlReadMode DIFF_GRAM
```


Bir DiffGram okur, DiffGram'dan gelen değişiklikleri [DataSet](../../com.aspose.words.net.system.data/dataset/) üzerine uygular ve [DataRow.getRowState()](../../com.aspose.words.net.system.data/datarow/\#getRowState) değerlerini korur.

### FRAGMENT {#FRAGMENT}
```
public static final System.Data.XmlReadMode FRAGMENT
```


SQL Server örneği üzerinde, FOR XML sorgularının yürütülmesiyle oluşturulan XML parçacıkları gibi XML parçacıklarını okur. [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) Fragment olarak ayarlandığında, varsayılan ad alanı satır içi şema olarak okunur.

### IGNORE_SCHEMA {#IGNORE-SCHEMA}
```
public static final System.Data.XmlReadMode IGNORE_SCHEMA
```


Herhangi bir satır içi şemayı yok sayar ve verileri mevcut [DataSet](../../com.aspose.words.net.system.data/dataset/) şemasına okur. Veri mevcut şemayla eşleşmezse, ( [DataSet] için tanımlanan farklı ad alanlarından gelen veriler dahil) atılır. Veri bir DiffGram ise, IgnoreSchema aynı işlevi DiffGram gibi yerine getirir.

### INFER_SCHEMA {#INFER-SCHEMA}
```
public static final System.Data.XmlReadMode INFER_SCHEMA
```


Herhangi bir satır içi şemayı yok sayar, veriden şema çıkarır ve verileri yükler. [DataSet](../../com.aspose.words.net.system.data/dataset/) zaten bir şema içeriyorsa, mevcut şema yeni tablolar ekleyerek veya mevcut tablolara sütun ekleyerek genişletilir. Çıkarılan tablo zaten mevcut ancak farklı bir ad alanına sahipse veya çıkarılan sütunlar mevcut sütunlarla çakışırsa bir istisna fırlatılır.

### INFER_TYPED_SCHEMA {#INFER-TYPED-SCHEMA}
```
public static final System.Data.XmlReadMode INFER_TYPED_SCHEMA
```


Herhangi bir satır içi şemayı yok sayar, veriden güçlü tipli bir şema çıkarır ve verileri yükler. Tip veri üzerinden çıkarılamazsa, veri dize (string) olarak yorumlanır. [DataSet](../../com.aspose.words.net.system.data/dataset/) zaten bir şema içeriyorsa, mevcut şema yeni tablolar ekleyerek veya mevcut tablolara sütun ekleyerek genişletilir. Çıkarılan tablo zaten mevcut ancak farklı bir ad alanına sahipse veya çıkarılan sütunlar mevcut sütunlarla çakışırsa bir istisna fırlatılır.

### READ_SCHEMA {#READ-SCHEMA}
```
public static final System.Data.XmlReadMode READ_SCHEMA
```


Herhangi bir satır içi şemayı okur ve verileri yükler. [DataSet](../../com.aspose.words.net.system.data/dataset/) zaten bir şema içeriyorsa, şemaya yeni tablolar eklenebilir, ancak satır içi şemadaki tablolar [DataSet] içinde zaten varsa bir istisna fırlatılır.

### <T>valueOf(Class<T> arg0, String arg1) {#-T-valueOf-java.lang.Class-T--java.lang.String}
```
public static T <T>valueOf(Class<T> arg0, String arg1)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| arg0 | java.lang.Class<T> |  |
| arg1 | java.lang.String |  |

**Returns:**
T
### compareTo(E arg0) {#compareTo-E}
```
public final int compareTo(E arg0)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| arg0 | E |  |

**Returns:**
int
### equals(Object arg0) {#equals-java.lang.Object}
```
public final boolean equals(Object arg0)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getDeclaringClass() {#getDeclaringClass}
```
public final Class<E> getDeclaringClass()
```




**Returns:**
java.lang.Class<E>
### hashCode() {#hashCode}
```
public final int hashCode()
```




**Returns:**
int
### name() {#name}
```
public final String name()
```




**Returns:**
java.lang.String
### ordinal() {#ordinal}
```
public final int ordinal()
```




**Returns:**
int
### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### valueOf(String name) {#valueOf-java.lang.String}
```
public static System.Data.XmlReadMode valueOf(String name)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String |  |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/)
### values() {#values}
```
public static System.Data.XmlReadMode[] values()
```




**Returns:**
com.aspose.words.net.System.Data.XmlReadMode[]
