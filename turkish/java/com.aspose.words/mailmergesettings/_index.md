---
title: "MailMergeSettings"
linktitle: "MailMergeSettings"
second_title: "Aspose.Words Java için"
description: "Java'da bir belge için tüm posta birleştirme bilgilerini belirtir."
type: docs
weight: 445
url: /tr/java/com.aspose.words/mailmergesettings/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class MailMergeSettings implements Cloneable
```

Bir belge için tüm posta birleştirme bilgilerini belirtir.

Daha fazla bilgi edinmek için, [ Mail Merge and Reporting ][Mail Merge and Reporting] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Bu nesneyi bir belge için posta birleştirme veri kaynağını belirtmek için kullanabilirsiniz ve bu bilgi (mevcut veri alanlarıyla birlikte) kullanıcı bu belgeyi açtığında Microsoft Word'de görünecektir. Ya da bu nesneyi, kullanıcının bu belge için Microsoft Word'de belirttiği posta birleştirme ayarlarını sorgulamak için kullanabilirsiniz.

Bu sınıfın nesnelerini doğrudan oluşturmanız genellikle gerekmez çünkü bir belgenin posta birleştirme ayarları her zaman [Document.getMailMergeSettings()](../../com.aspose.words/document/\#getMailMergeSettings) / [Document.setMailMergeSettings(com.aspose.words.MailMergeSettings)](../../com.aspose.words/document/\#setMailMergeSettings-com.aspose.words.MailMergeSettings) özelliği aracılığıyla kullanılabilir.

Bu belgenin posta birleştirme ana belge olup olmadığını tespit etmek için [getMainDocumentType()](../../com.aspose.words/mailmergesettings/\#getMainDocumentType) / [setMainDocumentType(int)](../../com.aspose.words/mailmergesettings/\#setMainDocumentType-int) özelliğinin değerini kontrol edin.

Bir belgeden posta birleştirme ayarlarını ve veri kaynağı bilgilerini kaldırmak için [clear()](../../com.aspose.words/mailmergesettings/\#clear) metodunu kullanabilirsiniz. Aspose.Words, [getMainDocumentType()](../../com.aspose.words/mailmergesettings/\#getMainDocumentType) / [setMainDocumentType(int)](../../com.aspose.words/mailmergesettings/\#setMainDocumentType-int) özelliği [MailMergeMainDocumentType.NOT\_A\_MERGE\_DOCUMENT](../../com.aspose.words/mailmergemaindocumenttype/\#NOT-A-MERGE-DOCUMENT) olarak ayarlanmışsa veya [getDataType()](../../com.aspose.words/mailmergesettings/\#getDataType) / [setDataType(int)](../../com.aspose.words/mailmergesettings/\#setDataType-int) özelliği [MailMergeDataType.NONE](../../com.aspose.words/mailmergedatatype/\#NONE) olarak ayarlanmışsa, Aspose.Words belgeye posta birleştirme ayarlarını yazmayacaktır.

Bu nesnenin özelliklerini nasıl kullanacağınızı öğrenmenin en iyi yolu, istenen veri kaynağıyla bir belgeyi Microsoft Word'de manuel olarak oluşturup ardından o belgeyi Aspose.Words ile açarak [Document.getMailMergeSettings()](../../com.aspose.words/document/\#getMailMergeSettings) / [Document.setMailMergeSettings(com.aspose.words.MailMergeSettings)](../../com.aspose.words/document/\#setMailMergeSettings-com.aspose.words.MailMergeSettings) ve [getOdso()](../../com.aspose.words/mailmergesettings/\#getOdso) / [setOdso(com.aspose.words.Odso)](../../com.aspose.words/mailmergesettings/\#setOdso-com.aspose.words.Odso) nesnelerinin özelliklerini incelemektir. Örneğin, bir veri kaynağını programlı olarak yapılandırmayı öğrenmek istiyorsanız bu iyi bir yaklaşımdır.

Aspose.Words, belgeleri farklı formatlar arasında yüklerken, kaydederken ve dönüştürürken posta birleştirme bilgilerini korur, ancak kendi posta birleştirmesini [MailMerge](../../com.aspose.words/mailmerge/) nesnesiyle gerçekleştirirken bu bilgileri kullanmaz.


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [clear()](#clear) | Belge kaydedildiğinde posta birleştirme ayarları kaydedilmeyecek ve belge normal bir belge haline gelecektir şekilde posta birleştirme ayarlarını temizler. |
| [deepClone()](#deepClone) | Bu nesnenin derin bir klonunu döndürür. |
| [getActiveRecord()](#getActiveRecord) | Microsoft Word'de görüntülenecek veri kaynağındaki kaydın bir‑bazlı indeksini belirtir. |
| [getAddressFieldName()](#getAddressFieldName) | E-posta adreslerini içeren veri kaynağındaki sütunu belirtir. |
| [getCheckErrors()](#getCheckErrors) | Posta birleştirme gerçekleştirildiğinde Microsoft Word tarafından yapılacak hata raporlama türünü belirtir. |
| [getConnectString()](#getConnectString) | Harici bir veri kaynağına bağlanmak için kullanılan bağlantı dizesini belirtir. |
| [getDataSource()](#getDataSource) | Posta birleştirme veri kaynağının yolunu belirtir. |
| [getDataType()](#getDataType) | Posta birleştirme veri kaynağının türünü ve veri erişim yöntemini belirtir. |
| [getDestination()](#getDestination) | Microsoft Word'ün bir birleştirme işleminin sonuçlarını nasıl çıkartacağını belirtir. |
| [getDoNotSupressBlankLines()](#getDoNotSupressBlankLines) | Birleştirme işlemini gerçekleştiren bir uygulamanın, birleştirme sonucunda oluşan belgelerdeki boş satırları nasıl işleyeceğini belirtir. |
| [getHeaderSource()](#getHeaderSource) | Birleştirme başlık kaynağına giden yolu belirtir. |
| [getLinkToQuery()](#getLinkToQuery) | Bu konuda emin değilim. |
| [getMailAsAttachment()](#getMailAsAttachment) | Birleştirme işlemi sırasında üretilen belgelerin, gerçek e-postanın gövdesi yerine ek olarak e-posta ile gönderilmesi gerektiğini belirtir. |
| [getMailSubject()](#getMailSubject) | Birleştirme sırasında üretilen e-postaların veya faksların konu satırında görünecek metni belirtir. |
| [getMainDocumentType()](#getMainDocumentType) | Birleştirme ana belge türünü belirtir. |
| [getOdso()](#getOdso) | Office Data Source Object (ODSO) ayarlarını belirten nesneyi alır. |
| [getQuery()](#getQuery) | Birleştirme işlemi gerçekleştirildiğinde belgeye aktarılacak kayıt kümesini döndürmek için belirtilen dış veri kaynağına çalıştırılacak Structured Query Language dizesini içerir. |
| [getViewMergedData()](#getViewMergedData) | Microsoft Word'ün, birleştirme alanlarının eklendiği yerde belirtilen dış veri kaynağının verilerini göstermesi gerektiğini belirtir (örneğin. |
| [setActiveRecord(int value)](#setActiveRecord-int) | Microsoft Word'de görüntülenecek veri kaynağındaki kaydın bir‑bazlı indeksini belirtir. |
| [setAddressFieldName(String value)](#setAddressFieldName-java.lang.String) | E-posta adreslerini içeren veri kaynağındaki sütunu belirtir. |
| [setCheckErrors(int value)](#setCheckErrors-int) | Posta birleştirme gerçekleştirildiğinde Microsoft Word tarafından yapılacak hata raporlama türünü belirtir. |
| [setConnectString(String value)](#setConnectString-java.lang.String) | Harici bir veri kaynağına bağlanmak için kullanılan bağlantı dizesini belirtir. |
| [setDataSource(String value)](#setDataSource-java.lang.String) | Posta birleştirme veri kaynağının yolunu belirtir. |
| [setDataType(int value)](#setDataType-int) | Posta birleştirme veri kaynağının türünü ve veri erişim yöntemini belirtir. |
| [setDestination(int value)](#setDestination-int) | Microsoft Word'ün bir birleştirme işleminin sonuçlarını nasıl çıkartacağını belirtir. |
| [setDoNotSupressBlankLines(boolean value)](#setDoNotSupressBlankLines-boolean) | Birleştirme işlemini gerçekleştiren bir uygulamanın, birleştirme sonucunda oluşan belgelerdeki boş satırları nasıl işleyeceğini belirtir. |
| [setHeaderSource(String value)](#setHeaderSource-java.lang.String) | Birleştirme başlık kaynağına giden yolu belirtir. |
| [setLinkToQuery(boolean value)](#setLinkToQuery-boolean) | Bu konuda emin değilim. |
| [setMailAsAttachment(boolean value)](#setMailAsAttachment-boolean) | Birleştirme işlemi sırasında üretilen belgelerin, gerçek e-postanın gövdesi yerine ek olarak e-posta ile gönderilmesi gerektiğini belirtir. |
| [setMailSubject(String value)](#setMailSubject-java.lang.String) | Birleştirme sırasında üretilen e-postaların veya faksların konu satırında görünecek metni belirtir. |
| [setMainDocumentType(int value)](#setMainDocumentType-int) | Birleştirme ana belge türünü belirtir. |
| [setOdso(Odso value)](#setOdso-com.aspose.words.Odso) | Office Data Source Object (ODSO) ayarlarını belirten nesneyi ayarlar. |
| [setQuery(String value)](#setQuery-java.lang.String) | Birleştirme işlemi gerçekleştirildiğinde belgeye aktarılacak kayıt kümesini döndürmek için belirtilen dış veri kaynağına çalıştırılacak Structured Query Language dizesini içerir. |
| [setViewMergedData(boolean value)](#setViewMergedData-boolean) | Microsoft Word'ün, birleştirme alanlarının eklendiği yerde belirtilen dış veri kaynağının verilerini göstermesi gerektiğini belirtir (örneğin. |
### clear() {#clear}
```
public void clear()
```


Belge kaydedildiğinde posta birleştirme ayarları kaydedilmeyecek ve belge normal bir belge haline gelecektir şekilde posta birleştirme ayarlarını temizler.

### deepClone() {#deepClone}
```
public MailMergeSettings deepClone()
```


Bu nesnenin derin bir klonunu döndürür.

**Returns:**
[MailMergeSettings](../../com.aspose.words/mailmergesettings/)
### getActiveRecord() {#getActiveRecord}
```
public int getActiveRecord()
```


Veri kaynağından Microsoft Word'de gösterilecek kaydın bir‑tabanlı indeksini belirtir. Varsayılan değer 1'dir.

**Returns:**
int - İlgili  int  değeri.
### getAddressFieldName() {#getAddressFieldName}
```
public String getAddressFieldName()
```


Veri kaynağında e-posta adreslerini içeren sütunu belirtir. Varsayılan değer boş bir dizedir.

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getCheckErrors() {#getCheckErrors}
```
public int getCheckErrors()
```


Microsoft Word birleştirme işlemi gerçekleştirirken yapacağı hata raporlama türünü belirtir. Varsayılan değer [MailMergeCheckErrors.DEFAULT](../../com.aspose.words/mailmergecheckerrors/\#DEFAULT).

**Returns:**
int - İlgili `int` değeri. Döndürülen değer, [MailMergeCheckErrors](../../com.aspose.words/mailmergecheckerrors/) sabitlerinden biridir.
### getConnectString() {#getConnectString}
```
public String getConnectString()
```


Harici bir veri kaynağına bağlanmak için kullanılan bağlantı dizesini belirtir. Varsayılan değer boş bir dizedir.

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getDataSource() {#getDataSource}
```
public String getDataSource()
```


Birleştirme veri kaynağına giden yolu belirtir. Varsayılan değer boş bir dizedir.

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getDataType() {#getDataType}
```
public int getDataType()
```


Birleştirme veri kaynağının türünü ve veri erişim yöntemini belirtir. Varsayılan değer [MailMergeDataType.DEFAULT](../../com.aspose.words/mailmergedatatype/\#DEFAULT).

**Returns:**
int - İlgili `int` değeri. Döndürülen değer, [MailMergeDataType](../../com.aspose.words/mailmergedatatype/) sabitlerinden biridir.
### getDestination() {#getDestination}
```
public int getDestination()
```


Microsoft Word'ün bir birleştirme işleminin sonuçlarını nasıl çıkartacağını belirtir. Varsayılan değer [MailMergeDestination.DEFAULT](../../com.aspose.words/mailmergedestination/\#DEFAULT).

**Returns:**
int - İlgili `int` değeri. Döndürülen değer, [MailMergeDestination](../../com.aspose.words/mailmergedestination/) sabitlerinden biridir.
### getDoNotSupressBlankLines() {#getDoNotSupressBlankLines}
```
public boolean getDoNotSupressBlankLines()
```


Birleştirme işlemini gerçekleştiren bir uygulamanın, birleştirme sonucunda oluşan belgelerdeki boş satırları nasıl işleyeceğini belirtir. Varsayılan değer false.

**Returns:**
boolean - İlgili  boolean  değeri.
### getHeaderSource() {#getHeaderSource}
```
public String getHeaderSource()
```


Birleştirme başlık kaynağına giden yolu belirtir. Varsayılan değer boş bir dizedir.

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getLinkToQuery() {#getLinkToQuery}
```
public boolean getLinkToQuery()
```


Bu konuda emin değilim. Microsoft Word Automation Reference, bunun sorgunun Microsoft Word'de belge her açıldığında çalıştırıldığını belirttiğini öne sürüyor. Ancak OOXML spesifikasyonu, bunun sorgunun gerçek sorguyu içeren harici bir sorgu dosyasına referans içerdiğini belirttiğini öne sürüyor. Varsayılan değer false.

**Returns:**
boolean - İlgili  boolean  değeri.
### getMailAsAttachment() {#getMailAsAttachment}
```
public boolean getMailAsAttachment()
```


Birleştirme işlemi sırasında üretilen belgelerin, gerçek e-postanın gövdesi yerine ek olarak e-posta ile gönderilmesi gerektiğini belirtir. Varsayılan değer false.

**Returns:**
boolean - İlgili  boolean  değeri.
### getMailSubject() {#getMailSubject}
```
public String getMailSubject()
```


Posta birleştirme sırasında oluşturulan e-posta veya faksların konu satırında görünecek metni belirtir. Varsayılan değer boş bir dizedir.

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getMainDocumentType() {#getMainDocumentType}
```
public int getMainDocumentType()
```


Posta birleştirme ana belge türünü belirtir. Varsayılan değer [MailMergeMainDocumentType.DEFAULT](../../com.aspose.words/mailmergemaindocumenttype/\#DEFAULT) dir.

 **Remarks:** 

Ana belge, birleştirilmiş belgenin her sürümü için aynı olan bilgileri içeren belgedir.

**Returns:**
int - İlgili int değeri. Döndürülen değer, [MailMergeMainDocumentType](../../com.aspose.words/mailmergemaindocumenttype/) sabitlerinden biridir.
### getOdso() {#getOdso}
```
public Odso getOdso()
```


Office Data Source Object (ODSO) ayarlarını belirten nesneyi alır.

 **Remarks:** 

Bu nesne asla null değildir.

**Returns:**
[Odso](../../com.aspose.words/odso/) - The object that specifies the Office Data Source Object (ODSO) settings.
### getQuery() {#getQuery}
```
public String getQuery()
```


Posta birleştirme işlemi gerçekleştirildiğinde belgeye aktarılacak kayıt kümesini döndürmek için belirtilen dış veri kaynağına çalıştırılacak Structured Query Language dizesini içerir. Varsayılan değer boş bir dizedir.

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getViewMergedData() {#getViewMergedData}
```
public boolean getViewMergedData()
```


Microsoft Word'ün birleştirme alanlarının eklendiği yerde belirtilen dış veri kaynağından gelen verileri görüntülemesini (ör. birleştirilmiş veriyi önizleme) belirtir. Varsayılan değer false'tur.

**Returns:**
boolean - İlgili  boolean  değeri.
### setActiveRecord(int value) {#setActiveRecord-int}
```
public void setActiveRecord(int value)
```


Veri kaynağından Microsoft Word'de gösterilecek kaydın bir‑tabanlı indeksini belirtir. Varsayılan değer 1'dir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | İlgili  int  değeri. |

### setAddressFieldName(String value) {#setAddressFieldName-java.lang.String}
```
public void setAddressFieldName(String value)
```


Veri kaynağında e-posta adreslerini içeren sütunu belirtir. Varsayılan değer boş bir dizedir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setCheckErrors(int value) {#setCheckErrors-int}
```
public void setCheckErrors(int value)
```


Microsoft Word birleştirme işlemi gerçekleştirirken yapacağı hata raporlama türünü belirtir. Varsayılan değer [MailMergeCheckErrors.DEFAULT](../../com.aspose.words/mailmergecheckerrors/\#DEFAULT).

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili int değeri. Değer, [MailMergeCheckErrors](../../com.aspose.words/mailmergecheckerrors/) sabitlerinden biri olmalıdır. |

### setConnectString(String value) {#setConnectString-java.lang.String}
```
public void setConnectString(String value)
```


Harici bir veri kaynağına bağlanmak için kullanılan bağlantı dizesini belirtir. Varsayılan değer boş bir dizedir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setDataSource(String value) {#setDataSource-java.lang.String}
```
public void setDataSource(String value)
```


Birleştirme veri kaynağına giden yolu belirtir. Varsayılan değer boş bir dizedir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setDataType(int value) {#setDataType-int}
```
public void setDataType(int value)
```


Birleştirme veri kaynağının türünü ve veri erişim yöntemini belirtir. Varsayılan değer [MailMergeDataType.DEFAULT](../../com.aspose.words/mailmergedatatype/\#DEFAULT).

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili int değeri. Değer, [MailMergeDataType](../../com.aspose.words/mailmergedatatype/) sabitlerinden biri olmalıdır. |

### setDestination(int value) {#setDestination-int}
```
public void setDestination(int value)
```


Microsoft Word'ün bir birleştirme işleminin sonuçlarını nasıl çıkartacağını belirtir. Varsayılan değer [MailMergeDestination.DEFAULT](../../com.aspose.words/mailmergedestination/\#DEFAULT).

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili int değeri. Değer, [MailMergeDestination](../../com.aspose.words/mailmergedestination/) sabitlerinden biri olmalıdır. |

### setDoNotSupressBlankLines(boolean value) {#setDoNotSupressBlankLines-boolean}
```
public void setDoNotSupressBlankLines(boolean value)
```


Birleştirme işlemini gerçekleştiren bir uygulamanın, birleştirme sonucunda oluşan belgelerdeki boş satırları nasıl işleyeceğini belirtir. Varsayılan değer false.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setHeaderSource(String value) {#setHeaderSource-java.lang.String}
```
public void setHeaderSource(String value)
```


Birleştirme başlık kaynağına giden yolu belirtir. Varsayılan değer boş bir dizedir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setLinkToQuery(boolean value) {#setLinkToQuery-boolean}
```
public void setLinkToQuery(boolean value)
```


Bu konuda emin değilim. Microsoft Word Automation Reference, bunun sorgunun Microsoft Word'de belge her açıldığında çalıştırıldığını belirttiğini öne sürüyor. Ancak OOXML spesifikasyonu, bunun sorgunun gerçek sorguyu içeren harici bir sorgu dosyasına referans içerdiğini belirttiğini öne sürüyor. Varsayılan değer false.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setMailAsAttachment(boolean value) {#setMailAsAttachment-boolean}
```
public void setMailAsAttachment(boolean value)
```


Birleştirme işlemi sırasında üretilen belgelerin, gerçek e-postanın gövdesi yerine ek olarak e-posta ile gönderilmesi gerektiğini belirtir. Varsayılan değer false.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setMailSubject(String value) {#setMailSubject-java.lang.String}
```
public void setMailSubject(String value)
```


Posta birleştirme sırasında oluşturulan e-posta veya faksların konu satırında görünecek metni belirtir. Varsayılan değer boş bir dizedir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setMainDocumentType(int value) {#setMainDocumentType-int}
```
public void setMainDocumentType(int value)
```


Posta birleştirme ana belge türünü belirtir. Varsayılan değer [MailMergeMainDocumentType.DEFAULT](../../com.aspose.words/mailmergemaindocumenttype/\#DEFAULT) dir.

 **Remarks:** 

Ana belge, birleştirilmiş belgenin her sürümü için aynı olan bilgileri içeren belgedir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili int değeri. Değer, [MailMergeMainDocumentType](../../com.aspose.words/mailmergemaindocumenttype/) sabitlerinden biri olmalıdır. |

### setOdso(Odso value) {#setOdso-com.aspose.words.Odso}
```
public void setOdso(Odso value)
```


Office Data Source Object (ODSO) ayarlarını belirten nesneyi ayarlar.

 **Remarks:** 

Bu nesne asla null değildir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [Odso](../../com.aspose.words/odso/) | Office Data Source Object (ODSO) ayarlarını belirten nesne. |

### setQuery(String value) {#setQuery-java.lang.String}
```
public void setQuery(String value)
```


Posta birleştirme işlemi gerçekleştirildiğinde belgeye aktarılacak kayıt kümesini döndürmek için belirtilen dış veri kaynağına çalıştırılacak Structured Query Language dizesini içerir. Varsayılan değer boş bir dizedir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setViewMergedData(boolean value) {#setViewMergedData-boolean}
```
public void setViewMergedData(boolean value)
```


Microsoft Word'ün birleştirme alanlarının eklendiği yerde belirtilen dış veri kaynağından gelen verileri görüntülemesini (ör. birleştirilmiş veriyi önizleme) belirtir. Varsayılan değer false'tur.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

