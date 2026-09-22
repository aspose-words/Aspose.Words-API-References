---
title: "PreferredWidth"
linktitle: "PreferredWidth"
second_title: "Aspose.Words لـ Java"
description: "يمثل قيمة ووحدة قياسها المستخدمة لتحديد العرض المفضل لجدول أو خلية في Java."
type: docs
weight: 550
url: /ar/java/com.aspose.words/preferredwidth/
---

**Inheritance:**
java.lang.Object
```
public class PreferredWidth
```

يمثل قيمة ووحدة قياسها المستخدمة لتحديد العرض المفضل لجدول أو خلية.

للتعرف على المزيد، زر مقالة الوثائق [ Working with Tables ][Working with Tables].

 **Remarks:** 

يمكن تحديد العرض المفضل كنسبة مئوية، أو عدد نقاط، أو قيمة خاصة "none/auto".

كائنات هذه الفئة غير قابلة للتغيير.

 **Examples:** 

يوضح كيفية ضبط جدول ليتناسب تلقائيًا مع 50٪ من عرض الصفحة.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell #1");
 builder.insertCell();
 builder.write("Cell #2");
 builder.insertCell();
 builder.write("Cell #3");

 table.setPreferredWidth(PreferredWidth.fromPercent(50.0));

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTableWithPreferredWidth.docx");
 
```

يوضح كيفية ضبط عرض مفضل لخلايا الجدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // There are two ways of applying the "PreferredWidth" class to table cells.
 // 1 -  Set an absolute preferred width based on points:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(40.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.YELLOW);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 // 2 -  Set a relative preferred width based on percent of the table's width:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPercent(20.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.BLUE);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 builder.insertCell();

 // A cell with no preferred width specified will take up the rest of the available space.
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);

 // Each configuration of the "PreferredWidth" property creates a new object.
 Assert.assertNotEquals(table.getFirstRow().getCells().get(1).getCellFormat().getPreferredWidth().hashCode(),
         builder.getCellFormat().getPreferredWidth().hashCode());

 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Automatically sized cell.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
 
```


[Working with Tables]: https://docs.aspose.com/words/java/working-with-tables/
## الحقول

| حقل | الوصف |
| --- | --- |
| [AUTO](#AUTO) | يرجع كائنًا يمثل قيمة "العرض المفضل غير محدد". |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [equals(PreferredWidth other)](#equals-com.aspose.words.PreferredWidth) | يحدد ما إذا كان [PreferredWidth](../../com.aspose.words/preferredwidth/) المحدد يساوي في القيمة [PreferredWidth](../../com.aspose.words/preferredwidth/) الحالي. |
| [equals(Object obj)](#equals-java.lang.Object) | يحدد ما إذا كان الكائن المحدد مساويًا في القيمة للكائن الحالي. |
| [fromPercent(double percent)](#fromPercent-double) | طريقة إنشاء تُعيد كائنًا جديدًا يمثل عرضًا مفضلًا محددًا كنسبة مئوية. |
| [fromPoints(double points)](#fromPoints-double) | طريقة إنشاء تُعيد كائنًا جديدًا يمثل عرضًا مفضلًا محددًا باستخدام عدد من النقاط. |
| [getType()](#getType) | يحصل على وحدة القياس المستخدمة لهذه القيمة المفضلة للعرض. |
| [getValue()](#getValue) | يحصل على قيمة العرض المفضلة. |
| [hashCode()](#hashCode) |  |
| [toString()](#toString) | يعيد سلسلة سهلة القراءة تعرض قيمة هذا الكائن. |
### AUTO {#AUTO}
```
public static PreferredWidth AUTO
```


يرجع كائنًا يمثل قيمة "العرض المفضل غير محدد".

 **Examples:** 

يوضح كيفية ضبط عرض مفضل لخلايا الجدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // There are two ways of applying the "PreferredWidth" class to table cells.
 // 1 -  Set an absolute preferred width based on points:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(40.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.YELLOW);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 // 2 -  Set a relative preferred width based on percent of the table's width:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPercent(20.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.BLUE);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 builder.insertCell();

 // A cell with no preferred width specified will take up the rest of the available space.
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);

 // Each configuration of the "PreferredWidth" property creates a new object.
 Assert.assertNotEquals(table.getFirstRow().getCells().get(1).getCellFormat().getPreferredWidth().hashCode(),
         builder.getCellFormat().getPreferredWidth().hashCode());

 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Automatically sized cell.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
 
```

### equals(PreferredWidth other) {#equals-com.aspose.words.PreferredWidth}
```
public boolean equals(PreferredWidth other)
```


يحدد ما إذا كان [PreferredWidth](../../com.aspose.words/preferredwidth/) المحدد يساوي في القيمة [PreferredWidth](../../com.aspose.words/preferredwidth/) الحالي.

 **Examples:** 

يوضح كيفية ضبط عرض مفضل لخلايا الجدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // There are two ways of applying the "PreferredWidth" class to table cells.
 // 1 -  Set an absolute preferred width based on points:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(40.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.YELLOW);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 // 2 -  Set a relative preferred width based on percent of the table's width:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPercent(20.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.BLUE);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 builder.insertCell();

 // A cell with no preferred width specified will take up the rest of the available space.
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);

 // Each configuration of the "PreferredWidth" property creates a new object.
 Assert.assertNotEquals(table.getFirstRow().getCells().get(1).getCellFormat().getPreferredWidth().hashCode(),
         builder.getCellFormat().getPreferredWidth().hashCode());

 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Automatically sized cell.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| other | [PreferredWidth](../../com.aspose.words/preferredwidth/) |  |

**Returns:**
boolean
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


يحدد ما إذا كان الكائن المحدد مساويًا في القيمة للكائن الحالي.

 **Examples:** 

يوضح كيفية ضبط عرض مفضل لخلايا الجدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // There are two ways of applying the "PreferredWidth" class to table cells.
 // 1 -  Set an absolute preferred width based on points:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(40.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.YELLOW);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 // 2 -  Set a relative preferred width based on percent of the table's width:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPercent(20.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.BLUE);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 builder.insertCell();

 // A cell with no preferred width specified will take up the rest of the available space.
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);

 // Each configuration of the "PreferredWidth" property creates a new object.
 Assert.assertNotEquals(table.getFirstRow().getCells().get(1).getCellFormat().getPreferredWidth().hashCode(),
         builder.getCellFormat().getPreferredWidth().hashCode());

 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Automatically sized cell.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### fromPercent(double percent) {#fromPercent-double}
```
public static PreferredWidth fromPercent(double percent)
```


طريقة إنشاء تُعيد كائنًا جديدًا يمثل عرضًا مفضلًا محددًا كنسبة مئوية.

 **Examples:** 

يوضح كيفية ضبط جدول ليتناسب تلقائيًا مع 50٪ من عرض الصفحة.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell #1");
 builder.insertCell();
 builder.write("Cell #2");
 builder.insertCell();
 builder.write("Cell #3");

 table.setPreferredWidth(PreferredWidth.fromPercent(50.0));

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertTableWithPreferredWidth.docx");
 
```

يوضح كيفية ضبط عرض مفضل لخلايا الجدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // There are two ways of applying the "PreferredWidth" class to table cells.
 // 1 -  Set an absolute preferred width based on points:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(40.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.YELLOW);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 // 2 -  Set a relative preferred width based on percent of the table's width:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPercent(20.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.BLUE);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 builder.insertCell();

 // A cell with no preferred width specified will take up the rest of the available space.
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);

 // Each configuration of the "PreferredWidth" property creates a new object.
 Assert.assertNotEquals(table.getFirstRow().getCells().get(1).getCellFormat().getPreferredWidth().hashCode(),
         builder.getCellFormat().getPreferredWidth().hashCode());

 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Automatically sized cell.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| نسبة مئوية | double | يجب أن تكون القيمة بين 0 و 100. |

**Returns:**
[PreferredWidth](../../com.aspose.words/preferredwidth/)
### fromPoints(double points) {#fromPoints-double}
```
public static PreferredWidth fromPoints(double points)
```


طريقة إنشاء تُعيد كائنًا جديدًا يمثل عرضًا مفضلًا محددًا باستخدام عدد من النقاط.

 **Examples:** 

يوضح كيفية ضبط عرض مفضل لخلايا الجدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // There are two ways of applying the "PreferredWidth" class to table cells.
 // 1 -  Set an absolute preferred width based on points:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(40.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.YELLOW);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 // 2 -  Set a relative preferred width based on percent of the table's width:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPercent(20.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.BLUE);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 builder.insertCell();

 // A cell with no preferred width specified will take up the rest of the available space.
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);

 // Each configuration of the "PreferredWidth" property creates a new object.
 Assert.assertNotEquals(table.getFirstRow().getCells().get(1).getCellFormat().getPreferredWidth().hashCode(),
         builder.getCellFormat().getPreferredWidth().hashCode());

 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Automatically sized cell.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
 
```

يظهر كيفية استخدام أدوات تحويل الوحدات أثناء تحديد عرض مفضل للخلية.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(ConvertUtil.inchToPoint(3.0)));
 builder.insertCell();

 Assert.assertEquals(216.0d, table.getFirstRow().getFirstCell().getCellFormat().getPreferredWidth().getValue());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| نقاط | double | يجب أن تكون القيمة بين 0 و 22 بوصة (22 \* 72 نقطة). |

**Returns:**
[PreferredWidth](../../com.aspose.words/preferredwidth/)
### getType() {#getType}
```
public int getType()
```


يحصل على وحدة القياس المستخدمة لهذه القيمة المفضلة للعرض.

 **Examples:** 

يعرض كيفية التحقق من نوع العرض المفضل وقيمته لخلية جدول.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 Table table = doc.getFirstSection().getBody().getTables().get(0);
 Cell firstCell = table.getFirstRow().getFirstCell();

 Assert.assertEquals(PreferredWidthType.PERCENT, firstCell.getCellFormat().getPreferredWidth().getType());
 Assert.assertEquals(11.16d, firstCell.getCellFormat().getPreferredWidth().getValue());
 
```

**Returns:**
int - وحدة القياس المستخدمة لهذه القيمة المفضلة للعرض. القيمة المرجعة هي واحدة من الثوابت في [PreferredWidthType](../../com.aspose.words/preferredwidthtype/).
### getValue() {#getValue}
```
public double getValue()
```


يحصل على قيمة العرض المفضلة. يتم تحديد وحدة القياس في الخاصية [getType()](../../com.aspose.words/preferredwidth/\#getType).

 **Examples:** 

يعرض كيفية التحقق من نوع العرض المفضل وقيمته لخلية جدول.

```

 Document doc = new Document(getMyDir() + "Tables.docx");

 Table table = doc.getFirstSection().getBody().getTables().get(0);
 Cell firstCell = table.getFirstRow().getFirstCell();

 Assert.assertEquals(PreferredWidthType.PERCENT, firstCell.getCellFormat().getPreferredWidth().getType());
 Assert.assertEquals(11.16d, firstCell.getCellFormat().getPreferredWidth().getValue());
 
```

**Returns:**
double - قيمة العرض المفضلة.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### toString() {#toString}
```
public String toString()
```


يعيد سلسلة سهلة القراءة تعرض قيمة هذا الكائن.

 **Examples:** 

يوضح كيفية ضبط عرض مفضل لخلايا الجدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 Table table = builder.startTable();

 // There are two ways of applying the "PreferredWidth" class to table cells.
 // 1 -  Set an absolute preferred width based on points:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPoints(40.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.YELLOW);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 // 2 -  Set a relative preferred width based on percent of the table's width:
 builder.insertCell();
 builder.getCellFormat().setPreferredWidth(PreferredWidth.fromPercent(20.0));
 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.BLUE);
 builder.writeln(MessageFormat.format("Cell with a width of {0}.", builder.getCellFormat().getPreferredWidth()));

 builder.insertCell();

 // A cell with no preferred width specified will take up the rest of the available space.
 builder.getCellFormat().setPreferredWidth(PreferredWidth.AUTO);

 // Each configuration of the "PreferredWidth" property creates a new object.
 Assert.assertNotEquals(table.getFirstRow().getCells().get(1).getCellFormat().getPreferredWidth().hashCode(),
         builder.getCellFormat().getPreferredWidth().hashCode());

 builder.getCellFormat().getShading().setBackgroundPatternColor(Color.GREEN);
 builder.writeln("Automatically sized cell.");

 doc.save(getArtifactsDir() + "DocumentBuilder.InsertCellsWithPreferredWidths.docx");
 
```

**Returns:**
java.lang.String
