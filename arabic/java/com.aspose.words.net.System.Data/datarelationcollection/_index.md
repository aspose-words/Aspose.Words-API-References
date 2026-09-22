---
title: "DataRelationCollection"
linktitle: "DataRelationCollection"
second_title: "Aspose.Words لـ Java"
description: "يمثل مجموعة كائنات DataRelation لهذا DataSet في Java."
type: docs
weight: 19
url: /ar/java/com.aspose.words.net.system.data/datarelationcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataRelationCollection implements Iterable
```

يمثل مجموعة كائنات [DataRelation](../../com.aspose.words.net.system.data/datarelation/) لهذا [DataSet](../../com.aspose.words.net.system.data/dataset/).
## الطرق

| طريقة | الوصف |
| --- | --- |
| [add(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#add-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | ينشئ [DataRelation](../../com.aspose.words.net.system.data/datarelation/) بعمود أب وأبن محددين، ويضيفه إلى المجموعة. |
| [add(System.Data.DataRelation relation)](#add-com.aspose.words.net.System.Data.DataRelation) | يضيف [DataRelation](../../com.aspose.words.net.system.data/datarelation/) إلى [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/). |
| [add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String parentColumnName, String childColumnName)](#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String-java.lang.String) | يضيف علاقة إلى المجموعة. |
| [add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)](#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String) | يضيف علاقة إلى المجموعة. |
| [add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | ينشئ [DataRelation](../../com.aspose.words.net.system.data/datarelation/) بالاسم المحدد، وعمودي الأب والابن، ويضيفه إلى المجموعة. |
| [add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)](#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean) | ينشئ [DataRelation](../../com.aspose.words.net.system.data/datarelation/) بالاسم المحدد، وعمودي الأب والابن، مع قيود اختيارية وفقًا لقيمة المعامل  createConstraints  ، ويضيفه إلى المجموعة. |
| [clear()](#clear) | يمسح المجموعة من أي علاقات. |
| [contains(System.Data.DataRelation relation)](#contains-com.aspose.words.net.System.Data.DataRelation) | يتحقق مما إذا كان هناك DataRelation بالاسم المحدد (غير حساس لحالة الأحرف) موجودًا في المجموعة. |
| [get(int index)](#get-int) | يحصل على كائن [DataRelation](../../com.aspose.words.net.system.data/datarelation/) عند الفهرس المحدد. |
| [get(String name)](#get-java.lang.String) | يحصل على كائن [DataRelation](../../com.aspose.words.net.system.data/datarelation/) المحدد بالاسم. |
| [getCount()](#getCount) |  |
| [indexOf(System.Data.DataRelation relation)](#indexOf-com.aspose.words.net.System.Data.DataRelation) | يحصل على فهرس كائن [DataRelation](../../com.aspose.words.net.system.data/datarelation/) المحدد. |
| [iterator()](#iterator) |  |
| [removeAt(int index)](#removeAt-int) | يزيل العلاقة عند الفهرس المحدد من المجموعة. |
### add(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#add-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public void add(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


ينشئ [DataRelation](../../com.aspose.words.net.system.data/datarelation/) بعمود أب وأبن محددين، ويضيفه إلى المجموعة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | عمود الأب للعلاقة. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | عمود الابن للعلاقة. |

### add(System.Data.DataRelation relation) {#add-com.aspose.words.net.System.Data.DataRelation}
```
public void add(System.Data.DataRelation relation)
```


يضيف [DataRelation](../../com.aspose.words.net.system.data/datarelation/) إلى [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | DataRelation لإضافته إلى المجموعة. |

### add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String parentColumnName, String childColumnName) {#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String-java.lang.String}
```
public void add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String parentColumnName, String childColumnName)
```


يضيف علاقة إلى المجموعة. لا يجري أي فحوصات على التكرار وما إلى ذلك.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| parentTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | جدول الأب للعلاقة. |
| childTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | جدول الابن للعلاقة. |
| parentColumnName | java.lang.String | اسم العمود الأب للعلاقة. |
| childColumnName | java.lang.String | اسم العمود الابن للعلاقة. |

### add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames) {#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String}
```
public void add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)
```


يضيف علاقة إلى المجموعة. لا يجري أي فحوصات على التكرار وما إلى ذلك.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| parentTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | جدول الأب للعلاقة. |
| childTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | جدول الابن للعلاقة. |
| parentColumnNames | java.lang.String[] | المصفوفة التي تحتوي على أسماء الأعمدة الأب للعلاقة. |
| childColumnNames | java.lang.String[] | المصفوفة التي تحتوي على أسماء الأعمدة الابن للعلاقة. |

### add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public void add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


ينشئ [DataRelation](../../com.aspose.words.net.system.data/datarelation/) بالاسم المحدد، وعمودي الأب والابن، ويضيفه إلى المجموعة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الاسم | java.lang.String | اسم العلاقة. |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | عمود الأب للعلاقة. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | عمود الابن للعلاقة. |

### add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints) {#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean}
```
public void add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)
```


ينشئ [DataRelation](../../com.aspose.words.net.system.data/datarelation/) بالاسم المحدد، وعمودي الأب والابن، مع قيود اختيارية وفقًا لقيمة المعامل  createConstraints  ، ويضيفه إلى المجموعة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الاسم | java.lang.String | اسم العلاقة. |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | عمود الأب للعلاقة. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | عمود الابن للعلاقة. |
| createConstraints | boolean | true لإنشاء القيود؛ وإلا false. (الافتراضي هو true). |

### clear() {#clear}
```
public void clear()
```


يمسح المجموعة من أي علاقات.

### contains(System.Data.DataRelation relation) {#contains-com.aspose.words.net.System.Data.DataRelation}
```
public boolean contains(System.Data.DataRelation relation)
```


يتحقق مما إذا كان هناك DataRelation بالاسم المحدد (غير حساس لحالة الأحرف) موجودًا في المجموعة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | اسم العلاقة للبحث عنها. |

**Returns:**
boolean - true، إذا كان هناك علاقة بالاسم المحدد؛ وإلا false.
### get(int index) {#get-int}
```
public System.Data.DataRelation get(int index)
```


يحصل على كائن [DataRelation](../../com.aspose.words.net.system.data/datarelation/) عند الفهرس المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int | الفهرس الصفري للبحث. |

**Returns:**
[DataRelation](../../com.aspose.words.net.system.data/datarelation/) - The [DataRelation](../../com.aspose.words.net.system.data/datarelation/), or a null value if the specified [DataRelation](../../com.aspose.words.net.system.data/datarelation/) does not exist.
### get(String name) {#get-java.lang.String}
```
public System.Data.DataRelation get(String name)
```


يحصل على كائن [DataRelation](../../com.aspose.words.net.system.data/datarelation/) المحدد بالاسم.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الاسم | java.lang.String | اسم العلاقة للبحث عنها. |

**Returns:**
[DataRelation](../../com.aspose.words.net.system.data/datarelation/) - The named [DataRelation](../../com.aspose.words.net.system.data/datarelation/), or a null value if the specified [DataRelation](../../com.aspose.words.net.system.data/datarelation/) does not exist.
### getCount() {#getCount}
```
public int getCount()
```




**Returns:**
int - إجمالي عدد العناصر في مجموعة
### indexOf(System.Data.DataRelation relation) {#indexOf-com.aspose.words.net.System.Data.DataRelation}
```
public int indexOf(System.Data.DataRelation relation)
```


يحصل على فهرس كائن [DataRelation](../../com.aspose.words.net.system.data/datarelation/) المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | العلاقة للبحث عنها. |

**Returns:**
int - الفهرس الصفري للعلاقة، أو -1 إذا لم يتم العثور على العلاقة في المجموعة.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


يزيل العلاقة عند الفهرس المحدد من المجموعة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int | فهرس العلاقة لإزالتها. |

