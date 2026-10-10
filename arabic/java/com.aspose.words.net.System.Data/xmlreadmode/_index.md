---
title: "XmlReadMode"
linktitle: "XmlReadMode"
second_title: "Aspose.Words لـ Java"
description: "يحدد كيفية قراءة بيانات XML ومخطط علائقي إلى DataSet في Java."
type: docs
weight: 37
url: /ar/java/com.aspose.words.net.system.data/xmlreadmode/
---

**Inheritance:**
java.lang.Object, java.lang.Enum
```
public enum XmlReadMode extends Enum<System.Data.XmlReadMode>
```

يحدد كيفية قراءة بيانات XML ومخطط علائقي إلى [DataSet](../../com.aspose.words.net.system.data/dataset/).
## الحقول

| حقل | الوصف |
| --- | --- |
| [AUTO](#AUTO) | افتراضي. |
| [DIFF_GRAM](#DIFF-GRAM) | يقرأ DiffGram، ويطبق التغييرات من DiffGram إلى [DataSet](../../com.aspose.words.net.system.data/dataset/) مع الحفاظ على قيم [DataRow.getRowState()](../../com.aspose.words.net.system.data/datarow/\#getRowState). |
| [FRAGMENT](#FRAGMENT) | يقرأ شظايا XML، مثل تلك التي تُنشأ بتنفيذ استعلامات FOR XML، ضد نسخة من SQL Server. |
| [IGNORE_SCHEMA](#IGNORE-SCHEMA) | يتجاهل أي مخطط مضمن ويقرأ البيانات في مخطط [DataSet](../../com.aspose.words.net.system.data/dataset/) الحالي. |
| [INFER_SCHEMA](#INFER-SCHEMA) | يتجاهل أي مخطط مضمن، يستنتج المخطط من البيانات ويحمل البيانات. |
| [INFER_TYPED_SCHEMA](#INFER-TYPED-SCHEMA) | يتجاهل أي مخطط مضمن، يستنتج مخططًا مكتوبًا بنوع قوي من البيانات، ويحمل البيانات. |
| [READ_SCHEMA](#READ-SCHEMA) | يقوم بقراءة أي مخطط مضمن ويحمّل البيانات. |
## الطرق

| طريقة | الوصف |
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


افتراضي.

### DIFF_GRAM {#DIFF-GRAM}
```
public static final System.Data.XmlReadMode DIFF_GRAM
```


يقرأ DiffGram، ويطبق التغييرات من DiffGram إلى [DataSet](../../com.aspose.words.net.system.data/dataset/) مع الحفاظ على قيم [DataRow.getRowState()](../../com.aspose.words.net.system.data/datarow/\#getRowState).

### FRAGMENT {#FRAGMENT}
```
public static final System.Data.XmlReadMode FRAGMENT
```


يقوم بقراءة مقاطع XML، مثل تلك التي تُنشأ عند تنفيذ استعلامات FOR XML، مقابل نسخة من SQL Server. عندما يتم تعيين [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) إلى Fragment، يتم قراءة مساحة الاسم الافتراضية كمخطط مضمن.

### IGNORE_SCHEMA {#IGNORE-SCHEMA}
```
public static final System.Data.XmlReadMode IGNORE_SCHEMA
```


يتجاهل أي مخطط مضمن ويقرأ البيانات في مخطط [DataSet](../../com.aspose.words.net.system.data/dataset/) الموجود. إذا لم تتطابق أي بيانات مع المخطط الموجود، يتم تجاهلها (بما في ذلك البيانات من مساحات أسماء مختلفة معرفة لـ [DataSet](../../com.aspose.words.net.system.data/dataset/)). إذا كانت البيانات من نوع DiffGram، فإن IgnoreSchema لها نفس الوظيفة مثل DiffGram.

### INFER_SCHEMA {#INFER-SCHEMA}
```
public static final System.Data.XmlReadMode INFER_SCHEMA
```


يتجاهل أي مخطط مضمن، يستنتج المخطط من البيانات ويحمّل البيانات. إذا كان [DataSet](../../com.aspose.words.net.system.data/dataset/) يحتوي بالفعل على مخطط، يتم توسيع المخطط الحالي بإضافة جداول جديدة أو إضافة أعمدة إلى الجداول الموجودة. يتم إلقاء استثناء إذا كان الجدول المستنتج موجودًا بالفعل ولكن في مساحة اسم مختلفة، أو إذا كان أي من الأعمدة المستنتجة يتعارض مع الأعمدة الموجودة.

### INFER_TYPED_SCHEMA {#INFER-TYPED-SCHEMA}
```
public static final System.Data.XmlReadMode INFER_TYPED_SCHEMA
```


يتجاهل أي مخطط مضمن، يستنتج مخططًا مكتوبًا بقوة من البيانات، ويحمّل البيانات. إذا تعذر استنتاج النوع من البيانات، يتم تفسيرها كبيانات نصية. إذا كان [DataSet](../../com.aspose.words.net.system.data/dataset/) يحتوي بالفعل على مخطط، يتم توسيع المخطط الحالي إما بإضافة جداول جديدة أو بإضافة أعمدة إلى الجداول الموجودة. يتم إلقاء استثناء إذا كان الجدول المستنتج موجودًا بالفعل ولكن في مساحة اسم مختلفة، أو إذا كان أي من الأعمدة المستنتجة يتعارض مع الأعمدة الموجودة.

### READ_SCHEMA {#READ-SCHEMA}
```
public static final System.Data.XmlReadMode READ_SCHEMA
```


يقوم بقراءة أي مخطط مضمن ويحمّل البيانات. إذا كان [DataSet](../../com.aspose.words.net.system.data/dataset/) يحتوي بالفعل على مخطط، يمكن إضافة جداول جديدة إلى المخطط، لكن يتم إلقاء استثناء إذا كانت أي جداول في المخطط المضمن موجودة بالفعل في [DataSet](../../com.aspose.words.net.system.data/dataset/).

### <T>valueOf(Class<T> arg0, String arg1) {#-T-valueOf-java.lang.Class-T--java.lang.String}
```
public static T <T>valueOf(Class<T> arg0, String arg1)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| arg0 | E |  |

**Returns:**
int
### equals(Object arg0) {#equals-java.lang.Object}
```
public final boolean equals(Object arg0)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| الاسم | java.lang.String |  |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/)
### values() {#values}
```
public static System.Data.XmlReadMode[] values()
```




**Returns:**
com.aspose.words.net.System.Data.XmlReadMode[]
