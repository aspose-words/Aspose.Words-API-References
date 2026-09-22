---
title: "DataColumn"
linktitle: "DataColumn"
second_title: "Aspose.Words لـ Java"
description: "يمثل مخطط عمود في DataTable في Java."
type: docs
weight: 14
url: /ar/java/com.aspose.words.net.system.data/datacolumn/
---

**Inheritance:**
java.lang.Object
```
public class DataColumn
```

يمثل مخطط عمود في [DataTable](../../com.aspose.words.net.system.data/datatable/).
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [DataColumn()](#DataColumn) | ينشئ مثيلاً جديداً من الفئة [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) من النوع string. |
| [DataColumn(String columnName)](#DataColumn-java.lang.String) | ينشئ مثيلاً جديداً من الفئة [DataColumn](../../com.aspose.words.net.system.data/datacolumn/)، من النوع string، باستخدام اسم العمود المحدد. |
| [DataColumn(String name, System.Data.DataTable table)](#DataColumn-java.lang.String-com.aspose.words.net.System.Data.DataTable) | ينشئ مثيلاً جديداً من الفئة @\{link DataColumn\} باستخدام اسم العمود المحدد والجدول الذي ينتمي إليه. |
| [DataColumn(String columnName, Class dataType)](#DataColumn-java.lang.String-java.lang.Class) | ينشئ مثيلاً جديداً من الفئة [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) باستخدام اسم العمود المحدد ونوع البيانات. |
| [DataColumn(String name, Class type, System.Data.DataTable table)](#DataColumn-java.lang.String-java.lang.Class-com.aspose.words.net.System.Data.DataTable) | ينشئ مثيلاً جديداً من الفئة [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) باستخدام اسم العمود المحدد، نوع البيانات، وجدول البيانات الذي ينتمي إليه. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [areColumnSetsTheSame(System.Data.DataColumn[] columnSet, System.Data.DataColumn[] compareSet)](#areColumnSetsTheSame-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn) |  |
| [getAllowDBNull()](#getAllowDBNull) | يحصل على قيمة تشير إلى ما إذا كانت قيم null مسموح بها في هذا العمود للصفوف التي تنتمي إلى الجدول. |
| [getAutoIncrement()](#getAutoIncrement) | يحصل على قيمة تشير إلى ما إذا كان العمود يزيد قيمة العمود تلقائيًا للصفوف الجديدة المضافة إلى الجدول. |
| [getAutoIncrementSeed()](#getAutoIncrementSeed) | يحصل على القيمة الابتدائية لعمود تم تعيين خاصية [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) له إلى true. |
| [getAutoIncrementStep()](#getAutoIncrementStep) | يحصل على الزيادة المستخدمة من قبل عمود تم تعيين خاصية [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) له إلى true. |
| [getCaption()](#getCaption) | يحصل على التسمية التوضيحية للعمود. |
| [getColumnMapping()](#getColumnMapping) | يحصل على [MappingType](../../com.aspose.words.net.system.data/mappingtype/) للعمود. |
| [getColumnName()](#getColumnName) | يحصل على اسم العمود في [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [getDataType()](#getDataType) | يحصل على نوع البيانات المخزنة في العمود. |
| [getDefaultValue()](#getDefaultValue) | يحصل على القيمة الافتراضية للعمود عند إنشاء صفوف جديدة. |
| [getExpression()](#getExpression) | يحصل على التعبير المستخدم لتصفية الصفوف، حساب القيم في العمود، أو إنشاء عمود تجميعي. |
| [getMaxLength()](#getMaxLength) | يحصل على الحد الأقصى لطول عمود النص. |
| [getNamespace()](#getNamespace) | يحصل على مساحة الاسم لـ [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| [getOrdinal()](#getOrdinal) | يحصل على موضع العمود في مجموعة [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [getPrefix()](#getPrefix) | يحصل على بادئة XML التي تستبدل مساحة الاسم لـ [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [getReadOnly()](#getReadOnly) | يحصل على قيمة تشير إلى ما إذا كان العمود يسمح بالتغييرات فور إضافة صف إلى الجدول. |
| [getTable()](#getTable) | يحصل على [DataTable](../../com.aspose.words.net.system.data/datatable/) الذي ينتمي إليه العمود. |
| [getUnique()](#getUnique) | يحصل على قيمة تشير إلى ما إذا كانت القيم في كل صف من العمود يجب أن تكون فريدة. |
| [isReadOnly()](#isReadOnly) |  |
| [isUnique()](#isUnique) |  |
| [setAllowDBNull(boolean value)](#setAllowDBNull-boolean) | يضبط قيمة تشير إلى ما إذا كانت القيم الفارغة مسموح بها في هذا العمود للصفوف التي تنتمي إلى الجدول. |
| [setAutoIncrement(boolean value)](#setAutoIncrement-boolean) | يضبط قيمة تشير إلى ما إذا كان العمود يزيد قيمة العمود تلقائيًا للصفوف الجديدة المضافة إلى الجدول. |
| [setAutoIncrementSeed(long value)](#setAutoIncrementSeed-long) | يضبط القيمة الابتدائية لعمود تم تعيين خاصية [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) له إلى true. |
| [setAutoIncrementStep(long value)](#setAutoIncrementStep-long) | يضبط الزيادة المستخدمة من قبل عمود تم تعيين خاصية [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) له إلى true. |
| [setCaption(String value)](#setCaption-java.lang.String) | يضبط التسمية التوضيحية للعمود. |
| [setColumnMapping(int value)](#setColumnMapping-int) | يضبط [MappingType](../../com.aspose.words.net.system.data/mappingtype/) للعمود. |
| [setColumnName(String value)](#setColumnName-java.lang.String) | يضبط اسم العمود في [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [setDataType(Class value)](#setDataType-java.lang.Class) | يضبط نوع البيانات المخزنة في العمود. |
| [setDefaultValue(Object value)](#setDefaultValue-java.lang.Object) | يضبط القيمة الافتراضية للعمود عند إنشاء صفوف جديدة. |
| [setMaxLength(int value)](#setMaxLength-int) | يضبط الحد الأقصى لطول عمود النص. |
| [setNamespace(String value)](#setNamespace-java.lang.String) | يضبط مساحة الاسم لـ [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| [setOrdinal(int ordinal)](#setOrdinal-int) | يغيّر الترتيب أو الموضع لـ [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) إلى الترتيب أو الموضع المحدد. |
| [setPrefix(String value)](#setPrefix-java.lang.String) | يضبط بادئة XML التي تُعطي اسمًا مستعارًا لمساحة الاسم الخاصة بـ [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [setReadOnly(boolean value)](#setReadOnly-boolean) | يضبط قيمة تشير إلى ما إذا كان العمود يسمح بالتغييرات فور إضافة صف إلى الجدول. |
| [setUnique(boolean value)](#setUnique-boolean) | يضبط قيمة تشير إلى ما إذا كانت القيم في كل صف من العمود يجب أن تكون فريدة. |
| [toString()](#toString) | يحصل على [getExpression()](../../com.aspose.words.net.system.data/datacolumn/\\#getExpression) للعمود، إذا كان موجودًا. |
### DataColumn() {#DataColumn}
```
public DataColumn()
```


ينشئ مثيلاً جديداً من الفئة [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) من النوع string.

### DataColumn(String columnName) {#DataColumn-java.lang.String}
```
public DataColumn(String columnName)
```


ينشئ مثيلاً جديداً من الفئة [DataColumn](../../com.aspose.words.net.system.data/datacolumn/)، من النوع string، باستخدام اسم العمود المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| columnName | java.lang.String | سلسلة تمثل اسم العمود الذي سيتم إنشاؤه. إذا تم تعيينها إلى null أو سلسلة فارغة (\"\"), سيتم تحديد اسم افتراضي عند إضافتها إلى مجموعة الأعمدة. |

### DataColumn(String name, System.Data.DataTable table) {#DataColumn-java.lang.String-com.aspose.words.net.System.Data.DataTable}
```
public DataColumn(String name, System.Data.DataTable table)
```


ينشئ مثيلاً جديداً من الفئة @\{link DataColumn\} باستخدام اسم العمود المحدد والجدول الذي ينتمي إليه.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الاسم | java.lang.String | اسم الـ DataColumn |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | الجدول الذي ينتمي إليه هذا العمود |

### DataColumn(String columnName, Class dataType) {#DataColumn-java.lang.String-java.lang.Class}
```
public DataColumn(String columnName, Class dataType)
```


ينشئ مثيلاً جديداً من الفئة [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) باستخدام اسم العمود المحدد ونوع البيانات.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| columnName | java.lang.String | سلسلة تمثل اسم العمود الذي سيتم إنشاؤه. إذا تم تعيينها إلى null أو سلسلة فارغة (\"\"), سيتم تحديد اسم افتراضي عند إضافتها إلى مجموعة الأعمدة. |
| dataType | java.lang.Class | دعم لـ [getDataType()](../../com.aspose.words.net.system.data/datacolumn/\\#getDataType) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\\#setDataType-java.lang.Class). |

### DataColumn(String name, Class type, System.Data.DataTable table) {#DataColumn-java.lang.String-java.lang.Class-com.aspose.words.net.System.Data.DataTable}
```
public DataColumn(String name, Class type, System.Data.DataTable table)
```


ينشئ مثيلاً جديداً من الفئة [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) باستخدام اسم العمود المحدد، نوع البيانات، وجدول البيانات الذي ينتمي إليه.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الاسم | java.lang.String | اسم الـ DataColumn |
| نوع | java.lang.Class | نوع البيانات |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | الجدول الذي ينتمي إليه هذا العمود |

### areColumnSetsTheSame(System.Data.DataColumn[] columnSet, System.Data.DataColumn[] compareSet) {#areColumnSetsTheSame-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn}
```
public static boolean areColumnSetsTheSame(System.Data.DataColumn[] columnSet, System.Data.DataColumn[] compareSet)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| columnSet | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) |  |
| compareSet | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) |  |

**Returns:**
boolean
### getAllowDBNull() {#getAllowDBNull}
```
public boolean getAllowDBNull()
```


يحصل على قيمة تشير إلى ما إذا كانت قيم null مسموح بها في هذا العمود للصفوف التي تنتمي إلى الجدول.

**Returns:**
منطقي - true إذا سُمح بالقيم null؛ وإلا false. القيمة الافتراضية هي true.
### getAutoIncrement() {#getAutoIncrement}
```
public boolean getAutoIncrement()
```


يحصل على قيمة تشير إلى ما إذا كان العمود يزيد قيمة العمود تلقائيًا للصفوف الجديدة المضافة إلى الجدول.

**Returns:**
منطقي - true إذا كانت قيمة العمود تُزاد تلقائيًا؛ وإلا false. القيمة الافتراضية هي false.
### getAutoIncrementSeed() {#getAutoIncrementSeed}
```
public long getAutoIncrementSeed()
```


يحصل على القيمة الابتدائية لعمود تم تعيين خاصية [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) له إلى true.

**Returns:**
طويل - القيمة الأولية لميزة [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\\#setAutoIncrement-boolean).
### getAutoIncrementStep() {#getAutoIncrementStep}
```
public long getAutoIncrementStep()
```


يحصل على الزيادة المستخدمة من قبل عمود تم تعيين خاصية [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) له إلى true.

**Returns:**
طويل - العدد الذي تُزاد به قيمة العمود تلقائيًا. القيمة الافتراضية هي 1.
### getCaption() {#getCaption}
```
public String getCaption()
```


يحصل على التسمية التوضيحية للعمود.

**Returns:**
java.lang.String - تسمية العمود. إذا لم يتم تعيينها، تُعيد قيمة [getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\\#getColumnName) / [setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\\#setColumnName-java.lang.String).
### getColumnMapping() {#getColumnMapping}
```
public int getColumnMapping()
```


يحصل على [MappingType](../../com.aspose.words.net.system.data/mappingtype/) للعمود.

**Returns:**
int - أحد قيم [MappingType](../../com.aspose.words.net.system.data/mappingtype/). القيمة المرجعة هي أحد ثوابت [MappingType](../../com.aspose.words.net.system.data/mappingtype/).
### getColumnName() {#getColumnName}
```
public String getColumnName()
```


يحصل على اسم العمود في [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Returns:**
java.lang.String - اسم العمود.
### getDataType() {#getDataType}
```
public Class getDataType()
```


يحصل على نوع البيانات المخزنة في العمود.

**Returns:**
java.lang.Class - كائن java.lang.Class يمثل نوع بيانات العمود.
### getDefaultValue() {#getDefaultValue}
```
public Object getDefaultValue()
```


يحصل على القيمة الافتراضية للعمود عند إنشاء صفوف جديدة.

**Returns:**
java.lang.Object - قيمة مناسبة لـ [getDataType()](../../com.aspose.words.net.system.data/datacolumn/\\#getDataType) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\\#setDataType-java.lang.Class) الخاص بالعمود.
### getExpression() {#getExpression}
```
public String getExpression()
```


يحصل على التعبير المستخدم لتصفية الصفوف، حساب القيم في العمود، أو إنشاء عمود تجميعي.

**Returns:**
java.lang.String - تعبير لحساب قيمة عمود، أو لإنشاء عمود تجميعي. نوع الإرجاع للتعبير يُحدَّد بواسطة [getDataType()](../../com.aspose.words.net.system.data/datacolumn/\\#getDataType) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\\#setDataType-java.lang.Class) للعمود.
### getMaxLength() {#getMaxLength}
```
public int getMaxLength()
```


يحصل على الحد الأقصى لطول عمود النص.

**Returns:**
int - الحد الأقصى لطول العمود بالأحرف. إذا لم يكن للعمود حد أقصى، تكون القيمة -1 (الافتراضي).
### getNamespace() {#getNamespace}
```
public String getNamespace()
```


يحصل على مساحة الاسم لـ [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).

**Returns:**
java.lang.String - مساحة الاسم لـ [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).
### getOrdinal() {#getOrdinal}
```
public int getOrdinal()
```


يحصل على موضع العمود في مجموعة [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Returns:**
int - موضع العمود. يُعطي -1 إذا لم يكن العمود عضوًا في مجموعة.
### getPrefix() {#getPrefix}
```
public String getPrefix()
```


يحصل على بادئة XML التي تستبدل مساحة الاسم لـ [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Returns:**
java.lang.String - بادئة XML لمساحة الاسم الخاصة بـ [DataTable](../../com.aspose.words.net.system.data/datatable/).
### getReadOnly() {#getReadOnly}
```
public boolean getReadOnly()
```


يحصل على قيمة تشير إلى ما إذا كان العمود يسمح بالتغييرات فور إضافة صف إلى الجدول.

**Returns:**
منطقي - true إذا كان العمود للقراءة فقط؛ وإلا false. القيمة الافتراضية هي false.
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


يحصل على [DataTable](../../com.aspose.words.net.system.data/datatable/) الذي ينتمي إليه العمود.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The [DataTable](../../com.aspose.words.net.system.data/datatable/) that the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) belongs to.
### getUnique() {#getUnique}
```
public boolean getUnique()
```


يحصل على قيمة تشير إلى ما إذا كانت القيم في كل صف من العمود يجب أن تكون فريدة.

**Returns:**
منطقي - true إذا كان يجب أن تكون القيمة فريدة؛ وإلا false. القيمة الافتراضية هي false.
### isReadOnly() {#isReadOnly}
```
public boolean isReadOnly()
```




**Returns:**
boolean
### isUnique() {#isUnique}
```
public boolean isUnique()
```




**Returns:**
boolean
### setAllowDBNull(boolean value) {#setAllowDBNull-boolean}
```
public void setAllowDBNull(boolean value)
```


يضبط قيمة تشير إلى ما إذا كانت القيم الفارغة مسموح بها في هذا العمود للصفوف التي تنتمي إلى الجدول.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | true إذا سُمح بالقيم null؛ وإلا false. القيمة الافتراضية هي true. |

### setAutoIncrement(boolean value) {#setAutoIncrement-boolean}
```
public void setAutoIncrement(boolean value)
```


يضبط قيمة تشير إلى ما إذا كان العمود يزيد قيمة العمود تلقائيًا للصفوف الجديدة المضافة إلى الجدول.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | true إذا كانت قيمة العمود تُزاد تلقائيًا؛ وإلا false. القيمة الافتراضية هي false. |

### setAutoIncrementSeed(long value) {#setAutoIncrementSeed-long}
```
public void setAutoIncrementSeed(long value)
```


يضبط القيمة الابتدائية لعمود تم تعيين خاصية [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) له إلى true.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | long | القيمة الابتدائية للخاصية [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean). |

### setAutoIncrementStep(long value) {#setAutoIncrementStep-long}
```
public void setAutoIncrementStep(long value)
```


يضبط الزيادة المستخدمة من قبل عمود تم تعيين خاصية [getAutoIncrement()](../../com.aspose.words.net.system.data/datacolumn/\#getAutoIncrement) / [setAutoIncrement(boolean)](../../com.aspose.words.net.system.data/datacolumn/\#setAutoIncrement-boolean) له إلى true.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | long | العدد الذي تُزاد به قيمة العمود تلقائيًا. القيمة الافتراضية هي 1. |

### setCaption(String value) {#setCaption-java.lang.String}
```
public void setCaption(String value)
```


يضبط التسمية التوضيحية للعمود.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | java.lang.String | التسمية التوضيحية للعمود. إذا لم يتم تعيينها، تُعيد قيمة [getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String). |

### setColumnMapping(int value) {#setColumnMapping-int}
```
public void setColumnMapping(int value)
```


يضبط [MappingType](../../com.aspose.words.net.system.data/mappingtype/) للعمود.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | إحدى قيم [MappingType](../../com.aspose.words.net.system.data/mappingtype/). يجب أن تكون القيمة واحدة من ثوابت [MappingType](../../com.aspose.words.net.system.data/mappingtype/). |

### setColumnName(String value) {#setColumnName-java.lang.String}
```
public void setColumnName(String value)
```


يضبط اسم العمود في [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | اسم العمود. |

### setDataType(Class value) {#setDataType-java.lang.Class}
```
public void setDataType(Class value)
```


يضبط نوع البيانات المخزنة في العمود.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.Class | كائن java.lang.Class يمثل نوع بيانات العمود. |

### setDefaultValue(Object value) {#setDefaultValue-java.lang.Object}
```
public void setDefaultValue(Object value)
```


يضبط القيمة الافتراضية للعمود عند إنشاء صفوف جديدة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | java.lang.Object | قيمة مناسبة لـ [getDataType()](../../com.aspose.words.net.system.data/datacolumn/\#getDataType) / [setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\#setDataType-java.lang.Class). |

### setMaxLength(int value) {#setMaxLength-int}
```
public void setMaxLength(int value)
```


يضبط الحد الأقصى لطول عمود النص.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | الطول الأقصى للعمود بالأحرف. إذا لم يكن للعمود طول أقصى، تكون القيمة -1 (الافتراضي). |

### setNamespace(String value) {#setNamespace-java.lang.String}
```
public void setNamespace(String value)
```


يضبط مساحة الاسم لـ [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | java.lang.String | مساحة الاسم لـ [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |

### setOrdinal(int ordinal) {#setOrdinal-int}
```
public void setOrdinal(int ordinal)
```


يغيّر الترتيب أو الموضع لـ [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) إلى الترتيب أو الموضع المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الترتيب | int | الترتيب المحدد. |

### setPrefix(String value) {#setPrefix-java.lang.String}
```
public void setPrefix(String value)
```


يضبط بادئة XML التي تُعطي اسمًا مستعارًا لمساحة الاسم الخاصة بـ [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | java.lang.String | بادئة XML لمساحة الاسم الخاصة بـ [DataTable](../../com.aspose.words.net.system.data/datatable/). |

### setReadOnly(boolean value) {#setReadOnly-boolean}
```
public void setReadOnly(boolean value)
```


يضبط قيمة تشير إلى ما إذا كان العمود يسمح بالتغييرات فور إضافة صف إلى الجدول.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | true إذا كان العمود للقراءة فقط؛ وإلا false. القيمة الافتراضية هي false. |

### setUnique(boolean value) {#setUnique-boolean}
```
public void setUnique(boolean value)
```


يضبط قيمة تشير إلى ما إذا كانت القيم في كل صف من العمود يجب أن تكون فريدة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | true إذا كان يجب أن تكون القيمة فريدة؛ وإلا false. القيمة الافتراضية هي false. |

### toString() {#toString}
```
public String toString()
```


يحصل على [getExpression()](../../com.aspose.words.net.system.data/datacolumn/\\#getExpression) للعمود، إذا كان موجودًا.

**Returns:**
java.lang.String - قيمة [getExpression()](../../com.aspose.words.net.system.data/datacolumn/\#getExpression) إذا تم تعيين الخاصية؛ وإلا خاصية [getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String).
