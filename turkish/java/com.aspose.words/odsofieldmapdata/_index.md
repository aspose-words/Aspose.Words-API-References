---
title: "OdsoFieldMapData"
linktitle: "OdsoFieldMapData"
second_title: "Aspose.Words Java için"
description: "Harici veri kaynağındaki bir sütunun Java'da belgedeki önceden tanımlı birleştirme alanlarına nasıl eşleneceğini belirtir."
type: docs
weight: 489
url: /tr/java/com.aspose.words/odsofieldmapdata/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class OdsoFieldMapData implements Cloneable
```

Dış veri kaynağındaki bir sütunun belgede önceden tanımlanmış birleştirme alanlarına nasıl eşleneceğini belirtir.

Daha fazla bilgi edinmek için, [ Mail Merge and Reporting ][Mail Merge and Reporting] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Microsoft Word, bir belgeye MERGEFIELD olarak eklenebilen veya ADDRESSBLOCK ya da GREETINGLINE alanlarında kullanılabilen bazı önceden tanımlı birleştirme alanı adları sağlar. [OdsoFieldMapData](../../com.aspose.words/odsofieldmapdata/) içinde belirtilen bilgiler, harici veri kaynağındaki bir sütunu tek bir önceden tanımlı birleştirme alanına eşlemeye olanak tanır.


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [deepClone()](#deepClone) | Bu nesnenin derin bir klonunu döndürür. |
| [getColumn()](#getColumn) | Harici bir veri kaynağındaki sütunun, belirli bir MERGEFIELD alanının yerel adına eşlenecek sıfır tabanlı indeksini belirtir. |
| [getMappedName()](#getMappedName) | Bu alan eşlemesinde, [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) özelliğiyle belirtilen sütun numarasına eşlenecek önceden tanımlı birleştirme alanı adını belirtir. |
| [getName()](#getName) | Bu özellik, [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) özelliğiyle belirtilen indeksli sütun için harici veri kaynağındaki sütun adını belirtir. |
| [getType()](#getType) | Belirli bir posta birleştirme alanının, verilen harici veri kaynağındaki bir sütuna eşlenip eşlenmediğini belirtir. |
| [setColumn(int value)](#setColumn-int) | Harici bir veri kaynağındaki sütunun, belirli bir MERGEFIELD alanının yerel adına eşlenecek sıfır tabanlı indeksini belirtir. |
| [setMappedName(String value)](#setMappedName-java.lang.String) | Bu alan eşlemesinde, [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) özelliğiyle belirtilen sütun numarasına eşlenecek önceden tanımlı birleştirme alanı adını belirtir. |
| [setName(String value)](#setName-java.lang.String) | Bu özellik, [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) özelliğiyle belirtilen indeksli sütun için harici veri kaynağındaki sütun adını belirtir. |
| [setType(int value)](#setType-int) | Belirli bir posta birleştirme alanının, verilen harici veri kaynağındaki bir sütuna eşlenip eşlenmediğini belirtir. |
### deepClone() {#deepClone}
```
public OdsoFieldMapData deepClone()
```


Bu nesnenin derin bir klonunu döndürür.

**Returns:**
[OdsoFieldMapData](../../com.aspose.words/odsofieldmapdata/)
### getColumn() {#getColumn}
```
public int getColumn()
```


Harici bir veri kaynağındaki sütunun, belirli bir MERGEFIELD alanının yerel adına eşlenecek sıfır tabanlı indeksini belirtir. Varsayılan değer 0'dır.

**Returns:**
int - İlgili  int  değeri.
### getMappedName() {#getMappedName}
```
public String getMappedName()
```


Bu alan eşlemesinde, [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) özelliğiyle belirtilen sütun numarasına eşlenecek önceden tanımlı birleştirme alanı adını belirtir. Varsayılan değer boş bir dizedir.

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getName() {#getName}
```
public String getName()
```


Bu özellik, [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) özelliğiyle belirtilen indeksli sütun için harici veri kaynağındaki sütun adını belirtir. Varsayılan değer boş bir dizedir.

**Returns:**
java.lang.String - İlgili java.lang.String değeri.
### getType() {#getType}
```
public int getType()
```


Belirli bir posta birleştirme alanının, verilen harici veri kaynağındaki bir sütuna eşlenip eşlenmediğini belirtir. Varsayılan değer [OdsoFieldMappingType.DEFAULT](../../com.aspose.words/odsofieldmappingtype/\#DEFAULT) 'dır.

**Returns:**
int - İlgili int değer. Döndürülen değer [OdsoFieldMappingType](../../com.aspose.words/odsofieldmappingtype/) sabitlerinden biridir.
### setColumn(int value) {#setColumn-int}
```
public void setColumn(int value)
```


Harici bir veri kaynağındaki sütunun, belirli bir MERGEFIELD alanının yerel adına eşlenecek sıfır tabanlı indeksini belirtir. Varsayılan değer 0'dır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | İlgili  int  değeri. |

### setMappedName(String value) {#setMappedName-java.lang.String}
```
public void setMappedName(String value)
```


Bu alan eşlemesinde, [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) özelliğiyle belirtilen sütun numarasına eşlenecek önceden tanımlı birleştirme alanı adını belirtir. Varsayılan değer boş bir dizedir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Bu özellik, [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) özelliğiyle belirtilen indeksli sütun için harici veri kaynağındaki sütun adını belirtir. Varsayılan değer boş bir dizedir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | İlgili java.lang.String değeri. |

### setType(int value) {#setType-int}
```
public void setType(int value)
```


Belirli bir posta birleştirme alanının, verilen harici veri kaynağındaki bir sütuna eşlenip eşlenmediğini belirtir. Varsayılan değer [OdsoFieldMappingType.DEFAULT](../../com.aspose.words/odsofieldmappingtype/\#DEFAULT) 'dır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | İlgili int değer. Değer, [OdsoFieldMappingType](../../com.aspose.words/odsofieldmappingtype/) sabitlerinden biri olmalıdır. |

