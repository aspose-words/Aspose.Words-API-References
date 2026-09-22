---
title: "Odso"
linktitle: "Odso"
second_title: "Aspose.Words لـ Java"
description: "يحدد إعدادات كائن مصدر بيانات المكتب ODSO لمصدر بيانات دمج البريد في Java."
type: docs
weight: 487
url: /ar/java/com.aspose.words/odso/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class Odso implements Cloneable
```

يحدد إعدادات كائن مصدر بيانات Office (ODSO) لمصدر بيانات دمج البريد.

لمزيد من المعلومات، قم بزيارة [ Mail Merge and Reporting ][Mail Merge and Reporting] مقالة التوثيق.

 **Remarks:** 

يبدو أن ODSO هو الطريقة "الجديدة" التي تفضل إصدارات Microsoft Word الأحدث استخدامها عند تحديد أنواع معينة من مصادر البيانات لمستند دمج البريد. ربما ظهر ODSO لأول مرة في Microsoft Word 2000.

استخدام ODSO موثق بشكل ضعيف والطريقة الأفضل لتعلم كيفية استخدام خصائص هذا الكائن هي إنشاء مستند بمصدر بيانات مطلوب يدويًا في Microsoft Word ثم فتح ذلك المستند باستخدام Aspose.Words وفحص خصائص كائنات [Document.getMailMergeSettings()](../../com.aspose.words/document/\#getMailMergeSettings) / [Document.setMailMergeSettings(com.aspose.words.MailMergeSettings)](../../com.aspose.words/document/\#setMailMergeSettings-com.aspose.words.MailMergeSettings) و[MailMergeSettings.getOdso()](../../com.aspose.words/mailmergesettings/\#getOdso) / [MailMergeSettings.setOdso(com.aspose.words.Odso)](../../com.aspose.words/mailmergesettings/\#setOdso-com.aspose.words.Odso) . هذه طريقة جيدة إذا كنت تريد تعلم كيفية تكوين مصدر بيانات برمجيًا، على سبيل المثال.

عادةً لا تحتاج إلى إنشاء كائنات من هذه الفئة مباشرة لأن إعدادات ODSO متاحة دائمًا عبر خاصية [MailMergeSettings.getOdso()](../../com.aspose.words/mailmergesettings/\#getOdso) / [MailMergeSettings.setOdso(com.aspose.words.Odso)](../../com.aspose.words/mailmergesettings/\#setOdso-com.aspose.words.Odso) .


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [deepClone()](#deepClone) | إرجاع نسخة عميقة من هذا الكائن. |
| [getColumnDelimiter()](#getColumnDelimiter) | يحدد الحرف الذي سيتم تفسيره كفاصل أعمدة يُستخدم لفصل الأعمدة داخل مصادر البيانات الخارجية. |
| [getDataSource()](#getDataSource) | يحدد موقع مصدر البيانات الخارجي الذي سيتم ربطه بالمستند لتنفيذ دمج البريد. |
| [getDataSourceType()](#getDataSourceType) | يحدد نوع مصدر البيانات الخارجي الذي سيتم ربطه كجزء من معلومات اتصال ODSO لهذا دمج البريد. |
| [getFieldMapDatas()](#getFieldMapDatas) | يحصل على مجموعة من الكائنات التي تحدد كيفية ربط الأعمدة من مصدر البيانات الخارجي بأسماء حقول الدمج المعرفة مسبقًا في المستند. |
| [getFirstRowContainsColumnNames()](#getFirstRowContainsColumnNames) | يحدد أن تطبيق الاستضافة يجب أن يتعامل مع الصف الأول من البيانات في مصدر البيانات الخارجي المحدد كصف رأس يحتوي على أسماء كل عمود في مصدر البيانات. |
| [getRecipientDatas()](#getRecipientDatas) | يحصل على مجموعة من الكائنات التي تحدد تضمين/استبعاد السجلات الفردية في دمج البريد. |
| [getTableName()](#getTableName) | يحدد مجموعة البيانات المحددة التي يجب ربط المصدر بها داخل مصدر بيانات خارجي. |
| [getUdlConnectString()](#getUdlConnectString) | يحدد سلسلة اتصال Universal Data Link (UDL) المستخدمة للاتصال بمصدر بيانات خارجي. |
| [setColumnDelimiter(char value)](#setColumnDelimiter-char) | يحدد الحرف الذي سيتم تفسيره كفاصل أعمدة يُستخدم لفصل الأعمدة داخل مصادر البيانات الخارجية. |
| [setDataSource(String value)](#setDataSource-java.lang.String) | يحدد موقع مصدر البيانات الخارجي الذي سيتم ربطه بالمستند لتنفيذ دمج البريد. |
| [setDataSourceType(int value)](#setDataSourceType-int) | يحدد نوع مصدر البيانات الخارجي الذي سيتم ربطه كجزء من معلومات اتصال ODSO لهذا دمج البريد. |
| [setFieldMapDatas(OdsoFieldMapDataCollection value)](#setFieldMapDatas-com.aspose.words.OdsoFieldMapDataCollection) | يضبط مجموعة من الكائنات التي تحدد كيفية ربط الأعمدة من مصدر البيانات الخارجي بأسماء حقول الدمج المعرفة مسبقًا في المستند. |
| [setFirstRowContainsColumnNames(boolean value)](#setFirstRowContainsColumnNames-boolean) | يحدد أن تطبيق الاستضافة يجب أن يتعامل مع الصف الأول من البيانات في مصدر البيانات الخارجي المحدد كصف رأس يحتوي على أسماء كل عمود في مصدر البيانات. |
| [setRecipientDatas(OdsoRecipientDataCollection value)](#setRecipientDatas-com.aspose.words.OdsoRecipientDataCollection) | يضبط مجموعة من الكائنات التي تحدد تضمين/استبعاد السجلات الفردية في دمج البريد. |
| [setTableName(String value)](#setTableName-java.lang.String) | يحدد مجموعة البيانات المحددة التي يجب ربط المصدر بها داخل مصدر بيانات خارجي. |
| [setUdlConnectString(String value)](#setUdlConnectString-java.lang.String) | يحدد سلسلة اتصال Universal Data Link (UDL) المستخدمة للاتصال بمصدر بيانات خارجي. |
### deepClone() {#deepClone}
```
public Odso deepClone()
```


إرجاع نسخة عميقة من هذا الكائن.

**Returns:**
[Odso](../../com.aspose.words/odso/)
### getColumnDelimiter() {#getColumnDelimiter}
```
public char getColumnDelimiter()
```


يحدد الحرف الذي سيتم تفسيره كفاصل أعمدة يُستخدم لفصل الأعمدة داخل مصادر البيانات الخارجية. القيمة الافتراضية هي 0 مما يعني عدم تعريف فاصل أعمدة.

 **Remarks:** 

RK لم أر هذا مستخدمًا من قبل.

**Returns:**
char - القيمة المقابلة للـ char.
### getDataSource() {#getDataSource}
```
public String getDataSource()
```


يحدد موقع مصدر البيانات الخارجي الذي سيتم ربطه بالمستند لتنفيذ دمج البريد. القيمة الافتراضية هي سلسلة فارغة.

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getDataSourceType() {#getDataSourceType}
```
public int getDataSourceType()
```


يحدد نوع مصدر البيانات الخارجي الذي سيتم ربطه كجزء من معلومات اتصال ODSO لهذا دمج البريد. القيمة الافتراضية هي [OdsoDataSourceType.DEFAULT](../../com.aspose.words/odsodatasourcetype/\#DEFAULT).

 **Remarks:** 

هذا الإعداد هو مجرد اقتراح لنوع مصدر البيانات المستخدم في هذا دمج البريد.

**Returns:**
int - القيمة المقابلة للـ int. القيمة المرجعة هي واحدة من ثوابت [OdsoDataSourceType](../../com.aspose.words/odsodatasourcetype/).
### getFieldMapDatas() {#getFieldMapDatas}
```
public OdsoFieldMapDataCollection getFieldMapDatas()
```


يحصل على مجموعة من الكائنات التي تحدد كيفية ربط الأعمدة من مصدر البيانات الخارجي بأسماء حقول الدمج المعرفة مسبقًا في المستند. هذا الكائن لا يكون أبدًا null.

**Returns:**
[OdsoFieldMapDataCollection](../../com.aspose.words/odsofieldmapdatacollection/) - A collection of objects that specify how columns from the external data source are mapped to the predefined merge field names in the document.
### getFirstRowContainsColumnNames() {#getFirstRowContainsColumnNames}
```
public boolean getFirstRowContainsColumnNames()
```


يحدد أن تطبيق الاستضافة يجب أن يتعامل مع الصف الأول من البيانات في مصدر البيانات الخارجي المحدد كصف رأس يحتوي على أسماء كل عمود في مصدر البيانات. القيمة الافتراضية هي false.

 **Remarks:** 

RK لم أر هذا مستخدمًا من قبل.

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getRecipientDatas() {#getRecipientDatas}
```
public OdsoRecipientDataCollection getRecipientDatas()
```


يحصل على مجموعة من الكائنات التي تحدد تضمين/استبعاد السجلات الفردية في دمج البريد. هذا الكائن لا يكون أبدًا null.

**Returns:**
[OdsoRecipientDataCollection](../../com.aspose.words/odsorecipientdatacollection/) - A collection of objects that specify inclusion/exclusion of individual records in the mail merge.
### getTableName() {#getTableName}
```
public String getTableName()
```


يحدد مجموعة البيانات المحددة التي يجب ربط المصدر بها داخل مصدر بيانات خارجي. القيمة الافتراضية هي سلسلة فارغة.

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getUdlConnectString() {#getUdlConnectString}
```
public String getUdlConnectString()
```


يحدد سلسلة الاتصال Universal Data Link (UDL) المستخدمة للاتصال بمصدر بيانات خارجي. القيمة الافتراضية هي سلسلة فارغة.

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### setColumnDelimiter(char value) {#setColumnDelimiter-char}
```
public void setColumnDelimiter(char value)
```


يحدد الحرف الذي سيتم تفسيره كفاصل أعمدة يُستخدم لفصل الأعمدة داخل مصادر البيانات الخارجية. القيمة الافتراضية هي 0 مما يعني عدم تعريف فاصل أعمدة.

 **Remarks:** 

RK لم أر هذا مستخدمًا من قبل.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | char | القيمة المقابلة للـ char. |

### setDataSource(String value) {#setDataSource-java.lang.String}
```
public void setDataSource(String value)
```


يحدد موقع مصدر البيانات الخارجي الذي سيتم ربطه بالمستند لتنفيذ دمج البريد. القيمة الافتراضية هي سلسلة فارغة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

### setDataSourceType(int value) {#setDataSourceType-int}
```
public void setDataSourceType(int value)
```


يحدد نوع مصدر البيانات الخارجي الذي سيتم ربطه كجزء من معلومات اتصال ODSO لهذا دمج البريد. القيمة الافتراضية هي [OdsoDataSourceType.DEFAULT](../../com.aspose.words/odsodatasourcetype/\#DEFAULT).

 **Remarks:** 

هذا الإعداد هو مجرد اقتراح لنوع مصدر البيانات المستخدم في هذا دمج البريد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | القيمة المقابلة للـ int. يجب أن تكون القيمة واحدة من الثوابت [OdsoDataSourceType](../../com.aspose.words/odsodatasourcetype/). |

### setFieldMapDatas(OdsoFieldMapDataCollection value) {#setFieldMapDatas-com.aspose.words.OdsoFieldMapDataCollection}
```
public void setFieldMapDatas(OdsoFieldMapDataCollection value)
```


يضبط مجموعة من الكائنات التي تحدد كيفية ربط الأعمدة من مصدر البيانات الخارجي بأسماء حقول الدمج المعرفة مسبقًا في المستند. هذا الكائن لا يكون أبدًا null.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [OdsoFieldMapDataCollection](../../com.aspose.words/odsofieldmapdatacollection/) | مجموعة من الكائنات التي تحدد كيفية ربط الأعمدة من مصدر البيانات الخارجي بأسماء حقول الدمج المعرفة مسبقًا في المستند. |

### setFirstRowContainsColumnNames(boolean value) {#setFirstRowContainsColumnNames-boolean}
```
public void setFirstRowContainsColumnNames(boolean value)
```


يحدد أن تطبيق الاستضافة يجب أن يتعامل مع الصف الأول من البيانات في مصدر البيانات الخارجي المحدد كصف رأس يحتوي على أسماء كل عمود في مصدر البيانات. القيمة الافتراضية هي false.

 **Remarks:** 

RK لم أر هذا مستخدمًا من قبل.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setRecipientDatas(OdsoRecipientDataCollection value) {#setRecipientDatas-com.aspose.words.OdsoRecipientDataCollection}
```
public void setRecipientDatas(OdsoRecipientDataCollection value)
```


يضبط مجموعة من الكائنات التي تحدد تضمين/استبعاد السجلات الفردية في دمج البريد. هذا الكائن لا يكون أبدًا null.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [OdsoRecipientDataCollection](../../com.aspose.words/odsorecipientdatacollection/) | مجموعة من الكائنات التي تحدد تضمين/استبعاد السجلات الفردية في دمج البريد. |

### setTableName(String value) {#setTableName-java.lang.String}
```
public void setTableName(String value)
```


يحدد مجموعة البيانات المحددة التي يجب ربط المصدر بها داخل مصدر بيانات خارجي. القيمة الافتراضية هي سلسلة فارغة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

### setUdlConnectString(String value) {#setUdlConnectString-java.lang.String}
```
public void setUdlConnectString(String value)
```


يحدد سلسلة الاتصال Universal Data Link (UDL) المستخدمة للاتصال بمصدر بيانات خارجي. القيمة الافتراضية هي سلسلة فارغة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

