---
title: "MailMergeSettings"
linktitle: "MailMergeSettings"
second_title: "Aspose.Words لـ Java"
description: "يحدد جميع معلومات دمج البريد لمستند في جافا."
type: docs
weight: 445
url: /ar/java/com.aspose.words/mailmergesettings/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class MailMergeSettings implements Cloneable
```

يحدد جميع معلومات دمج البريد للمستند.

لمزيد من المعلومات، قم بزيارة [ Mail Merge and Reporting ][Mail Merge and Reporting] مقالة التوثيق.

 **Remarks:** 

يمكنك استخدام هذا الكائن لتحديد مصدر بيانات دمج البريد لمستند، وستظهر هذه المعلومات (مع الحقول المتاحة) في Microsoft Word عندما يفتح المستخدم هذا المستند. أو يمكنك استخدام هذا الكائن لاستعلام إعدادات دمج البريد التي حددها المستخدم في Microsoft Word لهذا المستند.

عادةً لا تحتاج إلى إنشاء كائنات من هذه الفئة مباشرةً لأن إعدادات دمج البريد لمستند تكون دائمًا متاحة عبر الخاصية [Document.getMailMergeSettings()](../../com.aspose.words/document/#getMailMergeSettings) / [Document.setMailMergeSettings(com.aspose.words.MailMergeSettings)](../../com.aspose.words/document/#setMailMergeSettings-com.aspose.words.MailMergeSettings).

لكشف ما إذا كان هذا المستند هو المستند الرئيسي لدمج البريد، تحقق من قيمة الخاصية [getMainDocumentType()](../../com.aspose.words/mailmergesettings/#getMainDocumentType) / [setMainDocumentType(int)](../../com.aspose.words/mailmergesettings/#setMainDocumentType-int).

لإزالة إعدادات دمج البريد ومعلومات مصدر البيانات من مستند، يمكنك استخدام الطريقة [clear()](../../com.aspose.words/mailmergesettings/#clear). لن تقوم Aspose.Words بكتابة إعدادات دمج البريد إلى المستند إذا تم تعيين الخاصية [getMainDocumentType()](../../com.aspose.words/mailmergesettings/#getMainDocumentType) / [setMainDocumentType(int)](../../com.aspose.words/mailmergesettings/#setMainDocumentType-int) إلى [MailMergeMainDocumentType.NOT_A_MERGE_DOCUMENT](../../com.aspose.words/mailmergemaindocumenttype/#NOT-A-MERGE-DOCUMENT) أو تم تعيين الخاصية [getDataType()](../../com.aspose.words/mailmergesettings/#getDataType) / [setDataType(int)](../../com.aspose.words/mailmergesettings/#setDataType-int) إلى [MailMergeDataType.NONE](../../com.aspose.words/mailmergedatatype/#NONE).

أفضل طريقة لتعلم كيفية استخدام خصائص هذا الكائن هي إنشاء مستند بمصدر بيانات مطلوب يدويًا في Microsoft Word ثم فتح ذلك المستند باستخدام Aspose.Words وفحص خصائص الكائنات [Document.getMailMergeSettings()](../../com.aspose.words/document/#getMailMergeSettings) / [Document.setMailMergeSettings(com.aspose.words.MailMergeSettings)](../../com.aspose.words/document/#setMailMergeSettings-com.aspose.words.MailMergeSettings) و [getOdso()](../../com.aspose.words/mailmergesettings/#getOdso) / [setOdso(com.aspose.words.Odso)](../../com.aspose.words/mailmergesettings/#setOdso-com.aspose.words.Odso). هذا نهج جيد إذا كنت ترغب في تعلم كيفية تكوين مصدر بيانات برمجيًا، على سبيل المثال.

تحافظ Aspose.Words على معلومات دمج البريد عند تحميل وحفظ وتحويل المستندات بين صيغ مختلفة، لكنها لا تستخدم هذه المعلومات عند إجراء دمج البريد الخاص بها باستخدام الكائن [MailMerge](../../com.aspose.words/mailmerge/).


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [clear()](#clear) | يمسح إعدادات دمج البريد بطريقة تجعل المستند عند حفظه لا يحتوي على أي إعدادات دمج بريد ويصبح مستندًا عاديًا. |
| [deepClone()](#deepClone) | إرجاع نسخة عميقة من هذا الكائن. |
| [getActiveRecord()](#getActiveRecord) | يحدد الفهرس القائم على الواحد للسجل من مصدر البيانات الذي سيُعرض في Microsoft Word. |
| [getAddressFieldName()](#getAddressFieldName) | يحدد العمود داخل مصدر البيانات الذي يحتوي على عناوين البريد الإلكتروني. |
| [getCheckErrors()](#getCheckErrors) | يحدد نوع تقارير الأخطاء التي سيجريها Microsoft Word عند تنفيذ دمج البريد. |
| [getConnectString()](#getConnectString) | يحدد سلسلة الاتصال المستخدمة للاتصال بمصدر بيانات خارجي. |
| [getDataSource()](#getDataSource) | يحدد المسار إلى مصدر بيانات دمج البريد. |
| [getDataType()](#getDataType) | يحدد نوع مصدر بيانات دمج البريد وطريقة الوصول إلى البيانات. |
| [getDestination()](#getDestination) | يحدد كيفية إخراج Microsoft Word لنتائج دمج البريد. |
| [getDoNotSupressBlankLines()](#getDoNotSupressBlankLines) | يحدد كيفية تعامل التطبيق الذي يقوم بدمج البريد مع الأسطر الفارغة في المستندات المدمجة الناتجة عن دمج البريد. |
| [getHeaderSource()](#getHeaderSource) | يحدد المسار إلى مصدر رأس دمج البريد. |
| [getLinkToQuery()](#getLinkToQuery) | لست متأكدًا من هذا. |
| [getMailAsAttachment()](#getMailAsAttachment) | يحدد أن المستندات التي تُنتج خلال عملية دمج البريد يجب أن تُرسل كملف مرفق بدلاً من أن تكون في نص البريد الإلكتروني الفعلي. |
| [getMailSubject()](#getMailSubject) | يحدد النص الذي سيظهر في سطر الموضوع للبريد الإلكتروني أو الفاكسات التي تُنتج أثناء دمج البريد. |
| [getMainDocumentType()](#getMainDocumentType) | يحدد نوع المستند الرئيسي لدمج البريد. |
| [getOdso()](#getOdso) | يحصل على الكائن الذي يحدد إعدادات Office Data Source Object (ODSO). |
| [getQuery()](#getQuery) | يحتوي على سلسلة Structured Query Language التي سيتم تشغيلها ضد مصدر البيانات الخارجي المحدد لإرجاع مجموعة السجلات التي ستُستورد إلى المستند عند تنفيذ عملية دمج البريد. |
| [getViewMergedData()](#getViewMergedData) | يحدد أن Microsoft Word سيعرض البيانات من مصدر البيانات الخارجي المحدد حيث تم إدراج حقول الدمج (مثالًا |
| [setActiveRecord(int value)](#setActiveRecord-int) | يحدد الفهرس القائم على الواحد للسجل من مصدر البيانات الذي سيُعرض في Microsoft Word. |
| [setAddressFieldName(String value)](#setAddressFieldName-java.lang.String) | يحدد العمود داخل مصدر البيانات الذي يحتوي على عناوين البريد الإلكتروني. |
| [setCheckErrors(int value)](#setCheckErrors-int) | يحدد نوع تقارير الأخطاء التي سيجريها Microsoft Word عند تنفيذ دمج البريد. |
| [setConnectString(String value)](#setConnectString-java.lang.String) | يحدد سلسلة الاتصال المستخدمة للاتصال بمصدر بيانات خارجي. |
| [setDataSource(String value)](#setDataSource-java.lang.String) | يحدد المسار إلى مصدر بيانات دمج البريد. |
| [setDataType(int value)](#setDataType-int) | يحدد نوع مصدر بيانات دمج البريد وطريقة الوصول إلى البيانات. |
| [setDestination(int value)](#setDestination-int) | يحدد كيفية إخراج Microsoft Word لنتائج دمج البريد. |
| [setDoNotSupressBlankLines(boolean value)](#setDoNotSupressBlankLines-boolean) | يحدد كيفية تعامل التطبيق الذي يقوم بدمج البريد مع الأسطر الفارغة في المستندات المدمجة الناتجة عن دمج البريد. |
| [setHeaderSource(String value)](#setHeaderSource-java.lang.String) | يحدد المسار إلى مصدر رأس دمج البريد. |
| [setLinkToQuery(boolean value)](#setLinkToQuery-boolean) | لست متأكدًا من هذا. |
| [setMailAsAttachment(boolean value)](#setMailAsAttachment-boolean) | يحدد أن المستندات التي تُنتج خلال عملية دمج البريد يجب أن تُرسل كملف مرفق بدلاً من أن تكون في نص البريد الإلكتروني الفعلي. |
| [setMailSubject(String value)](#setMailSubject-java.lang.String) | يحدد النص الذي سيظهر في سطر الموضوع للبريد الإلكتروني أو الفاكسات التي تُنتج أثناء دمج البريد. |
| [setMainDocumentType(int value)](#setMainDocumentType-int) | يحدد نوع المستند الرئيسي لدمج البريد. |
| [setOdso(Odso value)](#setOdso-com.aspose.words.Odso) | يضبط الكائن الذي يحدد إعدادات Office Data Source Object (ODSO). |
| [setQuery(String value)](#setQuery-java.lang.String) | يحتوي على سلسلة Structured Query Language التي سيتم تشغيلها ضد مصدر البيانات الخارجي المحدد لإرجاع مجموعة السجلات التي ستُستورد إلى المستند عند تنفيذ عملية دمج البريد. |
| [setViewMergedData(boolean value)](#setViewMergedData-boolean) | يحدد أن Microsoft Word سيعرض البيانات من مصدر البيانات الخارجي المحدد حيث تم إدراج حقول الدمج (مثالًا |
### clear() {#clear}
```
public void clear()
```


يمسح إعدادات دمج البريد بطريقة تجعل المستند عند حفظه لا يحتوي على أي إعدادات دمج بريد ويصبح مستندًا عاديًا.

### deepClone() {#deepClone}
```
public MailMergeSettings deepClone()
```


إرجاع نسخة عميقة من هذا الكائن.

**Returns:**
[MailMergeSettings](../../com.aspose.words/mailmergesettings/)
### getActiveRecord() {#getActiveRecord}
```
public int getActiveRecord()
```


يحدد الفهرس القائم على الواحد للسجل من مصدر البيانات الذي سيُعرض في Microsoft Word. القيمة الافتراضية هي 1.

**Returns:**
int - القيمة المقابلة  int .
### getAddressFieldName() {#getAddressFieldName}
```
public String getAddressFieldName()
```


يحدد العمود داخل مصدر البيانات الذي يحتوي على عناوين البريد الإلكتروني. القيمة الافتراضية هي سلسلة فارغة.

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getCheckErrors() {#getCheckErrors}
```
public int getCheckErrors()
```


يحدد نوع تقارير الأخطاء التي سيجريها Microsoft Word عند تنفيذ دمج البريد. القيمة الافتراضية هي [MailMergeCheckErrors.DEFAULT](../../com.aspose.words/mailmergecheckerrors/\#DEFAULT).

**Returns:**
int - القيمة المقابلة لـ  int . القيمة المرجعة هي واحدة من ثوابت [MailMergeCheckErrors](../../com.aspose.words/mailmergecheckerrors/).
### getConnectString() {#getConnectString}
```
public String getConnectString()
```


يحدد سلسلة الاتصال المستخدمة للاتصال بمصدر بيانات خارجي. القيمة الافتراضية هي سلسلة فارغة.

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getDataSource() {#getDataSource}
```
public String getDataSource()
```


يحدد المسار إلى مصدر بيانات دمج البريد. القيمة الافتراضية هي سلسلة فارغة.

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getDataType() {#getDataType}
```
public int getDataType()
```


يحدد نوع مصدر بيانات دمج البريد وطريقة الوصول إلى البيانات. القيمة الافتراضية هي [MailMergeDataType.DEFAULT](../../com.aspose.words/mailmergedatatype/\#DEFAULT).

**Returns:**
int - القيمة المقابلة لـ  int . القيمة المرجعة هي واحدة من ثوابت [MailMergeDataType](../../com.aspose.words/mailmergedatatype/).
### getDestination() {#getDestination}
```
public int getDestination()
```


يحدد كيفية إخراج Microsoft Word لنتائج دمج البريد. القيمة الافتراضية هي [MailMergeDestination.DEFAULT](../../com.aspose.words/mailmergedestination/\#DEFAULT).

**Returns:**
int - القيمة المقابلة لـ  int . القيمة المرجعة هي واحدة من ثوابت [MailMergeDestination](../../com.aspose.words/mailmergedestination/).
### getDoNotSupressBlankLines() {#getDoNotSupressBlankLines}
```
public boolean getDoNotSupressBlankLines()
```


يحدد كيفية تعامل التطبيق الذي يقوم بدمج البريد مع الأسطر الفارغة في المستندات المدمجة الناتجة عن دمج البريد. القيمة الافتراضية هي false.

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getHeaderSource() {#getHeaderSource}
```
public String getHeaderSource()
```


يحدد المسار إلى مصدر رأس دمج البريد. القيمة الافتراضية هي سلسلة فارغة.

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getLinkToQuery() {#getLinkToQuery}
```
public boolean getLinkToQuery()
```


لست متأكدًا من هذا. تشير مرجع أتمتة Microsoft Word إلى أن هذا يحدد أن الاستعلام يُنفَّذ في كل مرة يُفتح فيها المستند في Microsoft Word. لكن مواصفة OOXML تشير إلى أن هذا يحدد أن الاستعلام يحتوي على إشارة إلى ملف استعلام خارجي يحتوي على الاستعلام الفعلي. القيمة الافتراضية هي false.

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getMailAsAttachment() {#getMailAsAttachment}
```
public boolean getMailAsAttachment()
```


يحدد أن المستندات التي تُنتج خلال عملية دمج البريد يجب أن تُرسل كملف مرفق بدلاً من أن تكون في نص البريد الإلكتروني الفعلي. القيمة الافتراضية هي false.

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getMailSubject() {#getMailSubject}
```
public String getMailSubject()
```


يحدد النص الذي سيظهر في سطر الموضوع للبريد الإلكتروني أو الفاكسات التي يتم إنتاجها أثناء دمج البريد. القيمة الافتراضية هي سلسلة فارغة.

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getMainDocumentType() {#getMainDocumentType}
```
public int getMainDocumentType()
```


يحدد نوع المستند الرئيسي لدمج البريد. القيمة الافتراضية هي [MailMergeMainDocumentType.DEFAULT](../../com.aspose.words/mailmergemaindocumenttype/#DEFAULT).

 **Remarks:** 

المستند الرئيسي هو المستند الذي يحتوي على معلومات تكون نفسها لكل نسخة من المستند المدمج.

**Returns:**
int - القيمة الصحيحة المقابلة. القيمة المرجعة هي واحدة من ثوابت [MailMergeMainDocumentType](../../com.aspose.words/mailmergemaindocumenttype/).
### getOdso() {#getOdso}
```
public Odso getOdso()
```


يحصل على الكائن الذي يحدد إعدادات Office Data Source Object (ODSO).

 **Remarks:** 

هذا الكائن ليس null أبداً.

**Returns:**
[Odso](../../com.aspose.words/odso/) - The object that specifies the Office Data Source Object (ODSO) settings.
### getQuery() {#getQuery}
```
public String getQuery()
```


يحتوي على سلسلة لغة الاستعلام البنيوية (SQL) التي سيتم تشغيلها ضد مصدر البيانات الخارجي المحدد لإرجاع مجموعة السجلات التي سيتم استيرادها إلى المستند عند تنفيذ عملية دمج البريد. القيمة الافتراضية هي سلسلة فارغة.

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getViewMergedData() {#getViewMergedData}
```
public boolean getViewMergedData()
```


يحدد أن Microsoft Word سيعرض البيانات من مصدر البيانات الخارجي المحدد حيث تم إدراج حقول الدمج (مثل معاينة البيانات المدمجة). القيمة الافتراضية هي false.

**Returns:**
boolean - القيمة المنطقية المقابلة.
### setActiveRecord(int value) {#setActiveRecord-int}
```
public void setActiveRecord(int value)
```


يحدد الفهرس القائم على الواحد للسجل من مصدر البيانات الذي سيُعرض في Microsoft Word. القيمة الافتراضية هي 1.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | القيمة  int  المقابلة. |

### setAddressFieldName(String value) {#setAddressFieldName-java.lang.String}
```
public void setAddressFieldName(String value)
```


يحدد العمود داخل مصدر البيانات الذي يحتوي على عناوين البريد الإلكتروني. القيمة الافتراضية هي سلسلة فارغة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

### setCheckErrors(int value) {#setCheckErrors-int}
```
public void setCheckErrors(int value)
```


يحدد نوع تقارير الأخطاء التي سيجريها Microsoft Word عند تنفيذ دمج البريد. القيمة الافتراضية هي [MailMergeCheckErrors.DEFAULT](../../com.aspose.words/mailmergecheckerrors/\#DEFAULT).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | القيمة الصحيحة المقابلة. يجب أن تكون القيمة واحدة من ثوابت [MailMergeCheckErrors](../../com.aspose.words/mailmergecheckerrors/). |

### setConnectString(String value) {#setConnectString-java.lang.String}
```
public void setConnectString(String value)
```


يحدد سلسلة الاتصال المستخدمة للاتصال بمصدر بيانات خارجي. القيمة الافتراضية هي سلسلة فارغة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

### setDataSource(String value) {#setDataSource-java.lang.String}
```
public void setDataSource(String value)
```


يحدد المسار إلى مصدر بيانات دمج البريد. القيمة الافتراضية هي سلسلة فارغة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

### setDataType(int value) {#setDataType-int}
```
public void setDataType(int value)
```


يحدد نوع مصدر بيانات دمج البريد وطريقة الوصول إلى البيانات. القيمة الافتراضية هي [MailMergeDataType.DEFAULT](../../com.aspose.words/mailmergedatatype/\#DEFAULT).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | القيمة الصحيحة المقابلة. يجب أن تكون القيمة واحدة من ثوابت [MailMergeDataType](../../com.aspose.words/mailmergedatatype/). |

### setDestination(int value) {#setDestination-int}
```
public void setDestination(int value)
```


يحدد كيفية إخراج Microsoft Word لنتائج دمج البريد. القيمة الافتراضية هي [MailMergeDestination.DEFAULT](../../com.aspose.words/mailmergedestination/\#DEFAULT).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | القيمة الصحيحة المقابلة. يجب أن تكون القيمة واحدة من ثوابت [MailMergeDestination](../../com.aspose.words/mailmergedestination/). |

### setDoNotSupressBlankLines(boolean value) {#setDoNotSupressBlankLines-boolean}
```
public void setDoNotSupressBlankLines(boolean value)
```


يحدد كيفية تعامل التطبيق الذي يقوم بدمج البريد مع الأسطر الفارغة في المستندات المدمجة الناتجة عن دمج البريد. القيمة الافتراضية هي false.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setHeaderSource(String value) {#setHeaderSource-java.lang.String}
```
public void setHeaderSource(String value)
```


يحدد المسار إلى مصدر رأس دمج البريد. القيمة الافتراضية هي سلسلة فارغة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

### setLinkToQuery(boolean value) {#setLinkToQuery-boolean}
```
public void setLinkToQuery(boolean value)
```


لست متأكدًا من هذا. تشير مرجع أتمتة Microsoft Word إلى أن هذا يحدد أن الاستعلام يُنفَّذ في كل مرة يُفتح فيها المستند في Microsoft Word. لكن مواصفة OOXML تشير إلى أن هذا يحدد أن الاستعلام يحتوي على إشارة إلى ملف استعلام خارجي يحتوي على الاستعلام الفعلي. القيمة الافتراضية هي false.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setMailAsAttachment(boolean value) {#setMailAsAttachment-boolean}
```
public void setMailAsAttachment(boolean value)
```


يحدد أن المستندات التي تُنتج خلال عملية دمج البريد يجب أن تُرسل كملف مرفق بدلاً من أن تكون في نص البريد الإلكتروني الفعلي. القيمة الافتراضية هي false.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setMailSubject(String value) {#setMailSubject-java.lang.String}
```
public void setMailSubject(String value)
```


يحدد النص الذي سيظهر في سطر الموضوع للبريد الإلكتروني أو الفاكسات التي يتم إنتاجها أثناء دمج البريد. القيمة الافتراضية هي سلسلة فارغة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

### setMainDocumentType(int value) {#setMainDocumentType-int}
```
public void setMainDocumentType(int value)
```


يحدد نوع المستند الرئيسي لدمج البريد. القيمة الافتراضية هي [MailMergeMainDocumentType.DEFAULT](../../com.aspose.words/mailmergemaindocumenttype/#DEFAULT).

 **Remarks:** 

المستند الرئيسي هو المستند الذي يحتوي على معلومات تكون نفسها لكل نسخة من المستند المدمج.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | القيمة الصحيحة المقابلة. يجب أن تكون القيمة واحدة من ثوابت [MailMergeMainDocumentType](../../com.aspose.words/mailmergemaindocumenttype/). |

### setOdso(Odso value) {#setOdso-com.aspose.words.Odso}
```
public void setOdso(Odso value)
```


يضبط الكائن الذي يحدد إعدادات Office Data Source Object (ODSO).

 **Remarks:** 

هذا الكائن ليس null أبداً.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [Odso](../../com.aspose.words/odso/) | الكائن الذي يحدد إعدادات Office Data Source Object (ODSO). |

### setQuery(String value) {#setQuery-java.lang.String}
```
public void setQuery(String value)
```


يحتوي على سلسلة لغة الاستعلام البنيوية (SQL) التي سيتم تشغيلها ضد مصدر البيانات الخارجي المحدد لإرجاع مجموعة السجلات التي سيتم استيرادها إلى المستند عند تنفيذ عملية دمج البريد. القيمة الافتراضية هي سلسلة فارغة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

### setViewMergedData(boolean value) {#setViewMergedData-boolean}
```
public void setViewMergedData(boolean value)
```


يحدد أن Microsoft Word سيعرض البيانات من مصدر البيانات الخارجي المحدد حيث تم إدراج حقول الدمج (مثل معاينة البيانات المدمجة). القيمة الافتراضية هي false.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

