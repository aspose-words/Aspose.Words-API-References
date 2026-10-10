---
title: "OdsoFieldMapData"
linktitle: "OdsoFieldMapData"
second_title: "Aspose.Words لـ Java"
description: "يحدد كيفية ربط عمود في مصدر البيانات الخارجي بالحقول المدمجة المعرفة مسبقًا داخل المستند في Java."
type: docs
weight: 489
url: /ar/java/com.aspose.words/odsofieldmapdata/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class OdsoFieldMapData implements Cloneable
```

يحدد كيفية ربط عمود في مصدر البيانات الخارجي بالحقول المدمجة المحددة مسبقًا داخل المستند.

لمزيد من المعلومات، قم بزيارة [ Mail Merge and Reporting ][Mail Merge and Reporting] مقالة التوثيق.

 **Remarks:** 

يوفر Microsoft Word بعض أسماء الحقول المدمجة المعرفة مسبقًا التي يسمح بإدراجها في مستند كـ MERGEFIELD أو استخدامها في حقول ADDRESSBLOCK أو GREETINGLINE. المعلومات المحددة في [OdsoFieldMapData](../../com.aspose.words/odsofieldmapdata/) تتيح ربط عمود واحد في مصدر البيانات الخارجي بحقل مدمج معرف مسبقًا.


[Mail Merge and Reporting]: https://docs.aspose.com/words/java/mail-merge-and-reporting/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [deepClone()](#deepClone) | إرجاع نسخة عميقة من هذا الكائن. |
| [getColumn()](#getColumn) | يحدد الفهرس الصفري للعمود داخل مصدر البيانات الخارجي الذي يجب ربطه بالاسم المحلي لحقل MERGEFIELD محدد. |
| [getMappedName()](#getMappedName) | يحدد اسم الحقل المدمج المعرفة مسبقًا الذي يجب ربطه برقم العمود المحدد بواسطة الخاصية [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) ضمن هذا الربط. |
| [getName()](#getName) | يحدد اسم العمود داخل مصدر البيانات الخارجي للعمود الذي يتم تحديد فهرسه بواسطة الخاصية [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int). |
| [getType()](#getType) | يحدد ما إذا تم ربط حقل دمج البريد المحدد بعمود في مصدر البيانات الخارجي المحدد أم لا. |
| [setColumn(int value)](#setColumn-int) | يحدد الفهرس الصفري للعمود داخل مصدر البيانات الخارجي الذي يجب ربطه بالاسم المحلي لحقل MERGEFIELD محدد. |
| [setMappedName(String value)](#setMappedName-java.lang.String) | يحدد اسم الحقل المدمج المعرفة مسبقًا الذي يجب ربطه برقم العمود المحدد بواسطة الخاصية [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) ضمن هذا الربط. |
| [setName(String value)](#setName-java.lang.String) | يحدد اسم العمود داخل مصدر البيانات الخارجي للعمود الذي يتم تحديد فهرسه بواسطة الخاصية [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int). |
| [setType(int value)](#setType-int) | يحدد ما إذا تم ربط حقل دمج البريد المحدد بعمود في مصدر البيانات الخارجي المحدد أم لا. |
### deepClone() {#deepClone}
```
public OdsoFieldMapData deepClone()
```


إرجاع نسخة عميقة من هذا الكائن.

**Returns:**
[OdsoFieldMapData](../../com.aspose.words/odsofieldmapdata/)
### getColumn() {#getColumn}
```
public int getColumn()
```


يحدد الفهرس الصفري للعمود داخل مصدر البيانات الخارجي الذي يجب ربطه بالاسم المحلي لحقل MERGEFIELD محدد. القيمة الافتراضية هي 0.

**Returns:**
int - القيمة المقابلة  int .
### getMappedName() {#getMappedName}
```
public String getMappedName()
```


يحدد اسم الحقل المدمج المعرفة مسبقًا الذي يجب ربطه برقم العمود المحدد بواسطة الخاصية [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) ضمن هذا الربط. القيمة الافتراضية هي سلسلة فارغة.

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getName() {#getName}
```
public String getName()
```


يحدد اسم العمود داخل مصدر البيانات الخارجي للعمود الذي يتم تحديد فهرسه بواسطة الخاصية [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int). القيمة الافتراضية هي سلسلة فارغة.

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getType() {#getType}
```
public int getType()
```


يحدد ما إذا تم ربط حقل دمج البريد المحدد بعمود في مصدر البيانات الخارجي المحدد أم لا. القيمة الافتراضية هي [OdsoFieldMappingType.DEFAULT](../../com.aspose.words/odsofieldmappingtype/\#DEFAULT).

**Returns:**
int - القيمة المقابلة من نوع  int . القيمة المرجعة هي واحدة من ثوابت [OdsoFieldMappingType](../../com.aspose.words/odsofieldmappingtype/).
### setColumn(int value) {#setColumn-int}
```
public void setColumn(int value)
```


يحدد الفهرس الصفري للعمود داخل مصدر البيانات الخارجي الذي يجب ربطه بالاسم المحلي لحقل MERGEFIELD محدد. القيمة الافتراضية هي 0.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | القيمة  int  المقابلة. |

### setMappedName(String value) {#setMappedName-java.lang.String}
```
public void setMappedName(String value)
```


يحدد اسم الحقل المدمج المعرفة مسبقًا الذي يجب ربطه برقم العمود المحدد بواسطة الخاصية [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int) ضمن هذا الربط. القيمة الافتراضية هي سلسلة فارغة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


يحدد اسم العمود داخل مصدر البيانات الخارجي للعمود الذي يتم تحديد فهرسه بواسطة الخاصية [getColumn()](../../com.aspose.words/odsofieldmapdata/\#getColumn) / [setColumn(int)](../../com.aspose.words/odsofieldmapdata/\#setColumn-int). القيمة الافتراضية هي سلسلة فارغة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

### setType(int value) {#setType-int}
```
public void setType(int value)
```


يحدد ما إذا تم ربط حقل دمج البريد المحدد بعمود في مصدر البيانات الخارجي المحدد أم لا. القيمة الافتراضية هي [OdsoFieldMappingType.DEFAULT](../../com.aspose.words/odsofieldmappingtype/\#DEFAULT).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | القيمة المقابلة من نوع  int . يجب أن تكون القيمة واحدة من ثوابت [OdsoFieldMappingType](../../com.aspose.words/odsofieldmappingtype/). |

