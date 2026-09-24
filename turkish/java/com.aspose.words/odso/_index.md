---
title: "Odso"
linktitle: "Odso"
second_title: "Aspose.Words Java için"
description: "Java'da bir birleştirme veri kaynağı için Office Data Source Object ODSO ayarlarını belirtir."
type: docs
weight: 487
url: /tr/java/com.aspose.words/odso/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class Odso implements Cloneable
```

Bir birleştirme veri kaynağı için Office Data Source Object (ODSO) ayarlarını belirtir.

Daha fazla bilgi edinmek için, [ Mail Merge and Reporting ][Mail Merge and Reporting] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

ODSO, yeni Microsoft Word sürümlerinin birleştirme belgesi için belirli veri kaynağı türlerini belirtirken tercih ettiği "yeni" yol gibi görünüyor. ODSO muhtemelen Microsoft Word 2000'de ilk kez ortaya çıktı.

ODSO'nun kullanımı kötü belgelenmiştir ve bu nesnenin özelliklerini nasıl kullanacağınızı öğrenmenin en iyi yolu, Microsoft Word'de istenen bir veri kaynağıyla bir belge oluşturmak, ardından bu belgeyi Aspose.Words kullanarak açmak ve [Document.getMailMergeSettings()](../../com.aspose.words/document/\#getMailMergeSettings) / [Document.setMailMergeSettings(com.aspose.words.MailMergeSettings)](../../com.aspose.words/document/\#setMailMergeSettings-com.aspose.words.MailMergeSettings) ve [MailMergeSettings.getOdso()](../../com.aspose.words/mailmergesettings/\#getOdso) / [MailMergeSettings.setOdso(com.aspose.words.Odso)](../../com.aspose.words/mailmergesettings/\#setOdso-com.aspose.words.Odso) nesnelerinin özelliklerini incelemektir. Bu, örneğin bir veri kaynağını programlı olarak yapılandırmayı öğrenmek istediğinizde iyi bir yaklaşımdır.

Bu sınıfın nesnelerini doğrudan oluşturmanız genellikle gerekmez çünkü ODSO ayarları her zaman [MailMergeSettings.getOdso()](../../com.aspose.words/mailmergesettings/\#getOdso) / [MailMergeSettings.setOdso(com.aspose.words.Odso)](../../com.aspose.words/mailmergesettings/\#setOdso-com.aspose.words.Odso) özelliği aracılığıyla mevcuttur.


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [deepClone()](#deepClone) | Bu nesnenin derin bir klonunu döndürür. |
| [getColumnDelimiter()](#getColumnDelimiter) | Harici veri kaynakları içinde sütunları ayırmak için kullanılan sütun sınırlayıcısı olarak yorumlanacak karakteri belirtir. |
| [getDataSource()](#getDataSource) | Posta birleştirme işlemi için bir belgeye bağlanacak harici veri kaynağının konumunu belirtir. |
| [getDataSourceType()](#getDataSourceType) | Bu posta birleştirme için ODSO bağlantı bilgilerinin bir parçası olarak bağlanacak harici veri kaynağının türünü belirtir. |
| [getFieldMapDatas()](#getFieldMapDatas) | Harici veri kaynağındaki sütunların belgede önceden tanımlanmış birleştirme alanı adlarına nasıl eşlendiğini belirten nesneler koleksiyonunu alır. |
| [getFirstRowContainsColumnNames()](#getFirstRowContainsColumnNames) | Barındırma uygulamasının, belirtilen harici veri kaynağındaki ilk veri satırını, veri kaynağındaki her sütunun adını içeren bir başlık satırı olarak ele almasını belirtir. |
| [getRecipientDatas()](#getRecipientDatas) | Posta birleştirmede bireysel kayıtların dahil edilmesini/edilmemesini belirten nesneler koleksiyonunu alır. |
| [getTableName()](#getTableName) | Bir kaynağın harici veri kaynağı içinde bağlanacağı belirli veri kümesini belirtir. |
| [getUdlConnectString()](#getUdlConnectString) | Harici bir veri kaynağına bağlanmak için kullanılan Universal Data Link (UDL) bağlantı dizesini belirtir. |
| [setColumnDelimiter(char value)](#setColumnDelimiter-char) | Harici veri kaynakları içinde sütunları ayırmak için kullanılan sütun sınırlayıcısı olarak yorumlanacak karakteri belirtir. |
| [setDataSource(String value)](#setDataSource-java.lang.String) | Posta birleştirme işlemi için bir belgeye bağlanacak harici veri kaynağının konumunu belirtir. |
| [setDataSourceType(int value)](#setDataSourceType-int) | Bu posta birleştirme için ODSO bağlantı bilgilerinin bir parçası olarak bağlanacak harici veri kaynağının türünü belirtir. |
| [setFieldMapDatas(OdsoFieldMapDataCollection value)](#setFieldMapDatas-com.aspose.words.OdsoFieldMapDataCollection) | Harici veri kaynağındaki sütunların belgede önceden tanımlanmış birleştirme alanı adlarına nasıl eşlendiğini belirten nesneler koleksiyonunu ayarlar. |
| [setFirstRowContainsColumnNames(boolean value)](#setFirstRowContainsColumnNames-boolean) | Barındırma uygulamasının, belirtilen harici veri kaynağındaki ilk veri satırını, veri kaynağındaki her sütunun adını içeren bir başlık satırı olarak ele almasını belirtir. |
| [setRecipientDatas(OdsoRecipientDataCollection value)](#setRecipientDatas-com.aspose.words.OdsoRecipientDataCollection) | Posta birleştirmede bireysel kayıtların dahil edilmesini/edilmemesini belirten nesneler koleksiyonunu ayarlar. |
| [setTableName(String value)](#setTableName-java.lang.String) | Bir kaynağın harici veri kaynağı içinde bağlanacağı belirli veri kümesini belirtir. |
| [setUdlConnectString(String value)](#setUdlConnectString-java.lang.String) | Harici bir veri kaynağına bağlanmak için kullanılan Universal Data Link (UDL) bağlantı dizesini belirtir. |
### deepClone() {#deepClone}
```
public Odso deepClone()
```


Bu nesnenin derin bir klonunu döndürür.

**Returns:**
[Odso](../../com.aspose.words/odso/)
### getColumnDelimiter() {#getColumnDelimiter}
```
public char getColumnDelimiter()
```


Harici veri kaynakları içinde sütunları ayırmak için kullanılan sütun sınırlayıcısı olarak yorumlanacak karakteri belirtir. Varsayılan değer 0'dır ve bu, tanımlı bir sütun sınırlayıcısı olmadığı anlamına gelir.

 **Remarks:** 

RK bunu hiç kullanıldığını görmedim.

**Returns:**
char - İlgili char değerini.
### getDataSource() {#getDataSource}
```
public String getDataSource()
```


Posta birleştirme işlemi için bir belgeye bağlanacak harici veri kaynağının konumunu belirtir. Varsayılan değer boş bir dizedir.

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getDataSourceType() {#getDataSourceType}
```
public int getDataSourceType()
```


Bu posta birleştirme için ODSO bağlantı bilgilerinin bir parçası olarak bağlanacak harici veri kaynağının türünü belirtir. Varsayılan değer [OdsoDataSourceType.DEFAULT](../../com.aspose.words/odsodatasourcetype/\#DEFAULT) 'dır.

 **Remarks:** 

Bu ayar, bu posta birleştirme için kullanılan veri kaynağı türünün yalnızca bir önerisidir.

**Returns:**
int - İlgili int değeri. Döndürülen değer, [OdsoDataSourceType](../../com.aspose.words/odsodatasourcetype/) sabitlerinden biridir.
### getFieldMapDatas() {#getFieldMapDatas}
```
public OdsoFieldMapDataCollection getFieldMapDatas()
```


Harici veri kaynağındaki sütunların belgede önceden tanımlanmış birleştirme alanı adlarına nasıl eşlendiğini belirten nesneler koleksiyonunu alır. Bu nesne hiçbir zaman null değildir.

**Returns:**
[OdsoFieldMapDataCollection](../../com.aspose.words/odsofieldmapdatacollection/) - A collection of objects that specify how columns from the external data source are mapped to the predefined merge field names in the document.
### getFirstRowContainsColumnNames() {#getFirstRowContainsColumnNames}
```
public boolean getFirstRowContainsColumnNames()
```


Barındırma uygulamasının, belirtilen harici veri kaynağındaki ilk veri satırını, veri kaynağındaki her sütunun adını içeren bir başlık satırı olarak ele almasını belirtir. Varsayılan değer false'tur.

 **Remarks:** 

RK bunu hiç kullanıldığını görmedim.

**Returns:**
boolean - İlgili  boolean  değeri.
### getRecipientDatas() {#getRecipientDatas}
```
public OdsoRecipientDataCollection getRecipientDatas()
```


Posta birleştirmede bireysel kayıtların dahil edilmesini/edilmemesini belirten nesneler koleksiyonunu alır. Bu nesne hiçbir zaman null değildir.

**Returns:**
[OdsoRecipientDataCollection](../../com.aspose.words/odsorecipientdatacollection/) - A collection of objects that specify inclusion/exclusion of individual records in the mail merge.
### getTableName() {#getTableName}
```
public String getTableName()
```


Bir kaynağın harici veri kaynağı içinde bağlanacağı belirli veri kümesini belirtir. Varsayılan değer boş bir dizedir.

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getUdlConnectString() {#getUdlConnectString}
```
public String getUdlConnectString()
```


Harici bir veri kaynağına bağlanmak için kullanılan Universal Data Link (UDL) bağlantı dizesini belirtir. Varsayılan değer boş bir dizedir.

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### setColumnDelimiter(char value) {#setColumnDelimiter-char}
```
public void setColumnDelimiter(char value)
```


Harici veri kaynakları içinde sütunları ayırmak için kullanılan sütun sınırlayıcısı olarak yorumlanacak karakteri belirtir. Varsayılan değer 0'dır ve bu, tanımlı bir sütun sınırlayıcısı olmadığı anlamına gelir.

 **Remarks:** 

RK bunu hiç kullanıldığını görmedim.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | char | İlgili char değeri. |

### setDataSource(String value) {#setDataSource-java.lang.String}
```
public void setDataSource(String value)
```


Posta birleştirme işlemi için bir belgeye bağlanacak harici veri kaynağının konumunu belirtir. Varsayılan değer boş bir dizedir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setDataSourceType(int value) {#setDataSourceType-int}
```
public void setDataSourceType(int value)
```


Bu posta birleştirme için ODSO bağlantı bilgilerinin bir parçası olarak bağlanacak harici veri kaynağının türünü belirtir. Varsayılan değer [OdsoDataSourceType.DEFAULT](../../com.aspose.words/odsodatasourcetype/\#DEFAULT) 'dır.

 **Remarks:** 

Bu ayar, bu posta birleştirme için kullanılan veri kaynağı türünün yalnızca bir önerisidir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili int değeri. Değer, [OdsoDataSourceType](../../com.aspose.words/odsodatasourcetype/) sabitlerinden biri olmalıdır. |

### setFieldMapDatas(OdsoFieldMapDataCollection value) {#setFieldMapDatas-com.aspose.words.OdsoFieldMapDataCollection}
```
public void setFieldMapDatas(OdsoFieldMapDataCollection value)
```


Harici veri kaynağından gelen sütunların belgede önceden tanımlanmış birleştirme alanı adlarına nasıl eşlendiğini belirten nesneler koleksiyonunu ayarlar. Bu nesne hiçbir zaman null değildir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [OdsoFieldMapDataCollection](../../com.aspose.words/odsofieldmapdatacollection/) | Harici veri kaynağından gelen sütunların belgede önceden tanımlanmış birleştirme alanı adlarına nasıl eşlendiğini belirten nesneler koleksiyonu. |

### setFirstRowContainsColumnNames(boolean value) {#setFirstRowContainsColumnNames-boolean}
```
public void setFirstRowContainsColumnNames(boolean value)
```


Barındırma uygulamasının, belirtilen harici veri kaynağındaki ilk veri satırını, veri kaynağındaki her sütunun adını içeren bir başlık satırı olarak ele almasını belirtir. Varsayılan değer false'tur.

 **Remarks:** 

RK bunu hiç kullanıldığını görmedim.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setRecipientDatas(OdsoRecipientDataCollection value) {#setRecipientDatas-com.aspose.words.OdsoRecipientDataCollection}
```
public void setRecipientDatas(OdsoRecipientDataCollection value)
```


Posta birleştirmesinde bireysel kayıtların dahil edilmesini/çıkarılmasını belirten nesneler koleksiyonunu ayarlar. Bu nesne hiçbir zaman null değildir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [OdsoRecipientDataCollection](../../com.aspose.words/odsorecipientdatacollection/) | Posta birleştirmesinde bireysel kayıtların dahil edilmesini/çıkarılmasını belirten nesneler koleksiyonu. |

### setTableName(String value) {#setTableName-java.lang.String}
```
public void setTableName(String value)
```


Bir kaynağın harici veri kaynağı içinde bağlanacağı belirli veri kümesini belirtir. Varsayılan değer boş bir dizedir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setUdlConnectString(String value) {#setUdlConnectString-java.lang.String}
```
public void setUdlConnectString(String value)
```


Harici bir veri kaynağına bağlanmak için kullanılan Universal Data Link (UDL) bağlantı dizesini belirtir. Varsayılan değer boş bir dizedir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

