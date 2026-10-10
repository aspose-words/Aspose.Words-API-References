---
title: "OdsoRecipientData"
linktitle: "OdsoRecipientData"
second_title: "Aspose.Words Java için"
description: "Java'da posta birleştirmeden hariç tutulacak harici bir veri kaynağındaki tek bir kayıta ilişkin bilgileri temsil eder."
type: docs
weight: 492
url: /tr/java/com.aspose.words/odsorecipientdata/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class OdsoRecipientData implements Cloneable
```

Birleştirme işleminden hariç tutulacak dış veri kaynağındaki tek bir kayıtla ilgili bilgiyi temsil eder.

Daha fazla bilgi edinmek için, [ Mail Merge and Reporting ][Mail Merge and Reporting] dokümantasyon makalesini ziyaret edin.

 **Remarks:** 

Bir kayıt birleştirilmiş bir belgeye birleştirilecekse, o kayıt hakkında bilgi gerekmez. Ancak, belirli bir kayıt birleştirilmiş bir belgeye birleştirilmeyecekse, bu kaydın benzersiz anahtarının değeri, bu nesnenin [getUniqueTag()](../../com.aspose.words/odsorecipientdata/\#getUniqueTag) / [setUniqueTag(byte[])](../../com.aspose.words/odsorecipientdata/\#setUniqueTag-byte) özelliğinde bu dışlamayı göstermek için saklanmalıdır.


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [deepClone()](#deepClone) | Bu nesnenin derin bir klonunu döndürür. |
| [getActive()](#getActive) | Posta birleştirme gerçekleştirildiğinde veri kaynağından gelen kaydın bir belgeye aktarılıp aktarılmayacağını belirtir. |
| [getColumn()](#getColumn) | Mevcut kayıt için benzersiz verileri içeren veri kaynağındaki sütunu belirtir. |
| [getHash()](#getHash) | Bu kaydın karma kodunu temsil eder. |
| [getUniqueTag()](#getUniqueTag) | Benzersiz veri içeren sütunda verilen bir kaydın içeriğini belirtir. |
| [setActive(boolean value)](#setActive-boolean) | Posta birleştirme gerçekleştirildiğinde veri kaynağından gelen kaydın bir belgeye aktarılıp aktarılmayacağını belirtir. |
| [setColumn(int value)](#setColumn-int) | Mevcut kayıt için benzersiz verileri içeren veri kaynağındaki sütunu belirtir. |
| [setHash(int value)](#setHash-int) | Bu kaydın karma kodunu temsil eder. |
| [setUniqueTag(byte[] value)](#setUniqueTag-byte) | Benzersiz veri içeren sütunda verilen bir kaydın içeriğini belirtir. |
### deepClone() {#deepClone}
```
public OdsoRecipientData deepClone()
```


Bu nesnenin derin bir klonunu döndürür.

**Returns:**
[OdsoRecipientData](../../com.aspose.words/odsorecipientdata/)
### getActive() {#getActive}
```
public boolean getActive()
```


Posta birleştirme gerçekleştirildiğinde veri kaynağından gelen kaydın bir belgeye aktarılıp aktarılmayacağını belirtir. Varsayılan değer true'dur.

**Returns:**
boolean - İlgili  boolean  değeri.
### getColumn() {#getColumn}
```
public int getColumn()
```


Mevcut kayıt için benzersiz verileri içeren veri kaynağındaki sütunu belirtir. Varsayılan değer 0'dır.

**Returns:**
int - İlgili  int  değeri.
### getHash() {#getHash}
```
public int getHash()
```


Bu kaydın karma kodunu temsil eder. Bazen Microsoft Word, bir [getHash()](../../com.aspose.words/odsorecipientdata/\#getHash) / [setHash(int)](../../com.aspose.words/odsorecipientdata/\#setHash-int) değerini, [getUniqueTag()](../../com.aspose.words/odsorecipientdata/\#getUniqueTag) / [setUniqueTag(byte[])](../../com.aspose.words/odsorecipientdata/\#setUniqueTag-byte) değerinin yerine bütün bir kayıt için kullanır. Varsayılan değer 0'dır.

**Returns:**
int - İlgili  int  değeri.
### getUniqueTag() {#getUniqueTag}
```
public byte[] getUniqueTag()
```


Benzersiz veri içeren sütunda verilen bir kaydın içeriğini belirtir. Varsayılan değer null'dur.

**Returns:**
byte[] - İlgili byte[] değeri.
### setActive(boolean value) {#setActive-boolean}
```
public void setActive(boolean value)
```


Posta birleştirme gerçekleştirildiğinde veri kaynağından gelen kaydın bir belgeye aktarılıp aktarılmayacağını belirtir. Varsayılan değer true'dur.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setColumn(int value) {#setColumn-int}
```
public void setColumn(int value)
```


Mevcut kayıt için benzersiz verileri içeren veri kaynağındaki sütunu belirtir. Varsayılan değer 0'dır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | İlgili  int  değeri. |

### setHash(int value) {#setHash-int}
```
public void setHash(int value)
```


Bu kaydın karma kodunu temsil eder. Bazen Microsoft Word, bir [getHash()](../../com.aspose.words/odsorecipientdata/\#getHash) / [setHash(int)](../../com.aspose.words/odsorecipientdata/\#setHash-int) değerini, [getUniqueTag()](../../com.aspose.words/odsorecipientdata/\#getUniqueTag) / [setUniqueTag(byte[])](../../com.aspose.words/odsorecipientdata/\#setUniqueTag-byte) değerinin yerine bütün bir kayıt için kullanır. Varsayılan değer 0'dır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | İlgili  int  değeri. |

### setUniqueTag(byte[] value) {#setUniqueTag-byte}
```
public void setUniqueTag(byte[] value)
```


Benzersiz veri içeren sütunda verilen bir kaydın içeriğini belirtir. Varsayılan değer null'dur.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | byte[] | İlgili byte[] değeri. |

