---
title: "OdsoRecipientData"
linktitle: "OdsoRecipientData"
second_title: "Aspose.Words لـ Java"
description: "يمثل معلومات حول سجل واحد داخل مصدر بيانات خارجي يجب استبعاده من دمج البريد في Java."
type: docs
weight: 492
url: /ar/java/com.aspose.words/odsorecipientdata/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class OdsoRecipientData implements Cloneable
```

يمثل معلومات حول سجل واحد داخل مصدر بيانات خارجي يجب استثناؤه من دمج البريد.

لمزيد من المعلومات، قم بزيارة [ Mail Merge and Reporting ][Mail Merge and Reporting] مقالة التوثيق.

 **Remarks:** 

إذا كان يجب دمج سجل في مستند مدمج، فلا حاجة إلى أي معلومات حول ذلك السجل. ومع ذلك، إذا كان يجب عدم دمج سجل معين في مستند مدمج، فيجب تخزين قيمة المفتاح الفريد لذلك السجل في خاصية [getUniqueTag()](../../com.aspose.words/odsorecipientdata/\#getUniqueTag) / [setUniqueTag(byte[])](../../com.aspose.words/odsorecipientdata/\#setUniqueTag-byte) لهذا الكائن للإشارة إلى هذا الاستبعاد.


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [deepClone()](#deepClone) | إرجاع نسخة عميقة من هذا الكائن. |
| [getActive()](#getActive) | يحدد ما إذا كان يجب استيراد السجل من مصدر البيانات إلى مستند عند تنفيذ دمج البريد. |
| [getColumn()](#getColumn) | يحدد العمود داخل مصدر البيانات الذي يحتوي على بيانات فريدة للسجل الحالي. |
| [getHash()](#getHash) | يمثل رمز التجزئة لهذا السجل. |
| [getUniqueTag()](#getUniqueTag) | يحدد محتويات سجل معين في العمود الذي يحتوي على بيانات فريدة. |
| [setActive(boolean value)](#setActive-boolean) | يحدد ما إذا كان يجب استيراد السجل من مصدر البيانات إلى مستند عند تنفيذ دمج البريد. |
| [setColumn(int value)](#setColumn-int) | يحدد العمود داخل مصدر البيانات الذي يحتوي على بيانات فريدة للسجل الحالي. |
| [setHash(int value)](#setHash-int) | يمثل رمز التجزئة لهذا السجل. |
| [setUniqueTag(byte[] value)](#setUniqueTag-byte) | يحدد محتويات سجل معين في العمود الذي يحتوي على بيانات فريدة. |
### deepClone() {#deepClone}
```
public OdsoRecipientData deepClone()
```


إرجاع نسخة عميقة من هذا الكائن.

**Returns:**
[OdsoRecipientData](../../com.aspose.words/odsorecipientdata/)
### getActive() {#getActive}
```
public boolean getActive()
```


يحدد ما إذا كان يجب استيراد السجل من مصدر البيانات إلى مستند عند تنفيذ دمج البريد. القيمة الافتراضية هي  true .

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getColumn() {#getColumn}
```
public int getColumn()
```


يحدد العمود داخل مصدر البيانات الذي يحتوي على بيانات فريدة للسجل الحالي. القيمة الافتراضية هي 0.

**Returns:**
int - القيمة المقابلة  int .
### getHash() {#getHash}
```
public int getHash()
```


يمثل رمز التجزئة لهذا السجل. أحيانًا يستخدم Microsoft Word [getHash()](../../com.aspose.words/odsorecipientdata/\#getHash) / [setHash(int)](../../com.aspose.words/odsorecipientdata/\#setHash-int) لسجل كامل بدلاً من قيمة [getUniqueTag()](../../com.aspose.words/odsorecipientdata/\#getUniqueTag) / [setUniqueTag(byte[])](../../com.aspose.words/odsorecipientdata/\#setUniqueTag-byte). القيمة الافتراضية هي 0.

**Returns:**
int - القيمة المقابلة  int .
### getUniqueTag() {#getUniqueTag}
```
public byte[] getUniqueTag()
```


يحدد محتويات سجل معين في العمود الذي يحتوي على بيانات فريدة. القيمة الافتراضية هي  null .

**Returns:**
byte[] - القيمة المقابلة من نوع byte[] .
### setActive(boolean value) {#setActive-boolean}
```
public void setActive(boolean value)
```


يحدد ما إذا كان يجب استيراد السجل من مصدر البيانات إلى مستند عند تنفيذ دمج البريد. القيمة الافتراضية هي  true .

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setColumn(int value) {#setColumn-int}
```
public void setColumn(int value)
```


يحدد العمود داخل مصدر البيانات الذي يحتوي على بيانات فريدة للسجل الحالي. القيمة الافتراضية هي 0.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | القيمة  int  المقابلة. |

### setHash(int value) {#setHash-int}
```
public void setHash(int value)
```


يمثل رمز التجزئة لهذا السجل. أحيانًا يستخدم Microsoft Word [getHash()](../../com.aspose.words/odsorecipientdata/\#getHash) / [setHash(int)](../../com.aspose.words/odsorecipientdata/\#setHash-int) لسجل كامل بدلاً من قيمة [getUniqueTag()](../../com.aspose.words/odsorecipientdata/\#getUniqueTag) / [setUniqueTag(byte[])](../../com.aspose.words/odsorecipientdata/\#setUniqueTag-byte). القيمة الافتراضية هي 0.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | القيمة  int  المقابلة. |

### setUniqueTag(byte[] value) {#setUniqueTag-byte}
```
public void setUniqueTag(byte[] value)
```


يحدد محتويات سجل معين في العمود الذي يحتوي على بيانات فريدة. القيمة الافتراضية هي  null .

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | byte[] | القيمة المقابلة من نوع byte[] . |

