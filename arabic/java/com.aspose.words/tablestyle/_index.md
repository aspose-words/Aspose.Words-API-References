---
title: "TableStyle"
linktitle: "TableStyle"
second_title: "Aspose.Words لـ Java"
description: "يمثل نمط جدول في جافا."
type: docs
weight: 660
url: /ar/java/com.aspose.words/tablestyle/
---

**Inheritance:**
java.lang.Object، [com.aspose.words.Style](../../com.aspose.words/style/)
```
public class TableStyle extends Style
```

يمثل نمط جدول.

للتعرف على المزيد، زر مقالة الوثائق [ Working with Tables ][Working with Tables].

 **Examples:** 

يظهر كيفية إنشاء إعدادات نمط مخصصة للجدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```


[Working with Tables]: https://docs.aspose.com/words/java/working-with-tables/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [clearCellAttrs()](#clearCellAttrs) |  |
| [clearParaAttrs()](#clearParaAttrs) |  |
| [clearRowAttrs()](#clearRowAttrs) |  |
| [clearRunAttrs()](#clearRunAttrs) |  |
| [equals(Style style)](#equals-com.aspose.words.Style) | يقارن مع النمط المحدد. |
| [fetchCellAttr(int key)](#fetchCellAttr-int) |  |
| [fetchInheritedBorderAttr(int key)](#fetchInheritedBorderAttr-int) |  |
| [fetchInheritedCellAttr(int key)](#fetchInheritedCellAttr-int) |  |
| [fetchInheritedParaAttr(int key)](#fetchInheritedParaAttr-int) |  |
| [fetchInheritedRowAttr(int key)](#fetchInheritedRowAttr-int) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int) |  |
| [fetchInheritedShadingAttr(int key)](#fetchInheritedShadingAttr-int) |  |
| [fetchParaAttr(int key)](#fetchParaAttr-int) |  |
| [fetchRowAttr(int key)](#fetchRowAttr-int) |  |
| [getAliases()](#getAliases) | يحصل على جميع الأسماء المستعارة لهذا النمط. |
| [getAlignment()](#getAlignment) | يحدد محاذاة نمط الجدول. |
| [getAllowBreakAcrossPages()](#getAllowBreakAcrossPages) | يحصل على علم يشير إلى ما إذا كان مسموحًا للنص في صف الجدول أن ينقسم عبر فاصل صفحة. |
| [getAutomaticallyUpdate()](#getAutomaticallyUpdate) | يحدد ما إذا كان هذا النمط يُعاد تعريفه تلقائيًا بناءً على القيمة المناسبة. |
| [getBaseStyleName()](#getBaseStyleName) | يحصل/يضبط اسم النمط الذي يُستند إليه هذا النمط. |
| [getBorders()](#getBorders) | يحصل على مجموعة حدود الخلايا الافتراضية للنمط. |
| [getBottomPadding()](#getBottomPadding) | يحصل على مقدار المسافة (بالنقاط) لإضافتها أسفل محتويات خلايا الجدول. |
| [getBuiltIn()](#getBuiltIn) | صحيح إذا كان هذا النمط أحد الأنماط المدمجة في MS Word. |
| [getCellSpacing()](#getCellSpacing) | يحصل على مقدار المسافة (بالنقاط) بين الخلايا. |
| [getColumnStripe()](#getColumnStripe) | يحصل على عدد الأعمدة التي يجب تضمينها في التظليل عندما يحدد النمط تظليل الأعمدة الفردية/الزوجية. |
| [getConditionalStyles()](#getConditionalStyles) | مجموعة من الأنماط الشرطية التي يمكن تعريفها لهذا نمط الجدول. |
| [getDirectBorderAttr(int key)](#getDirectBorderAttr-int) |  |
| [getDirectCellAttr(int key)](#getDirectCellAttr-int) |  |
| [getDirectParaAttr(int key)](#getDirectParaAttr-int) |  |
| [getDirectParaAttr(int key, int revisionsView)](#getDirectParaAttr-int-int) |  |
| [getDirectRowAttr(int key)](#getDirectRowAttr-int) |  |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int) |  |
| [getDirectRunAttr(int key, int revisionsView)](#getDirectRunAttr-int-int) |  |
| [getDocument()](#getDocument) | يحصل على المستند المالك. |
| [getFont()](#getFont) | يحصل على تنسيق الأحرف للنمط. |
| [getLeftIndent()](#getLeftIndent) | يحصل على القيمة التي تمثل المسافة البادئة اليسرى للجدول. |
| [getLeftPadding()](#getLeftPadding) | يحصل على مقدار المسافة (بالنقاط) لإضافتها إلى يسار محتويات خلايا الجدول. |
| [getLinkedStyleName()](#getLinkedStyleName) | يحصل/يضبط اسم الـ[Style](../../com.aspose.words/style/) المرتبط بهذا. |
| [getList()](#getList) | يحصل على القائمة التي تحدد تنسيق نمط القائمة هذا. |
| [getListFormat()](#getListFormat) | يوفر الوصول إلى خصائص تنسيق القائمة لنمط الفقرة. |
| [getLocked()](#getLocked) | يحدد ما إذا كان هذا النمط مقفلاً. |
| [getName()](#getName) | يحصل على اسم النمط. |
| [getNextParagraphStyleName()](#getNextParagraphStyleName) | يحصل/يضبط اسم النمط الذي سيُطبق تلقائياً على فقرة جديدة تُدرج بعد فقرة مُنسقة بالنمط المحدد. |
| [getParagraphFormat()](#getParagraphFormat) | يحصل على تنسيق الفقرة للنمط. |
| [getPriority()](#getPriority) | يحصل/يضبط القيمة الصحيحة التي تمثل أولوية فرز الأنماط في لوحة مهام الأنماط. |
| [getRightPadding()](#getRightPadding) | يحصل على مقدار المسافة (بالنقاط) لإضافتها إلى يمين محتويات خلايا الجدول. |
| [getRowStripe()](#getRowStripe) | يحصل على عدد الصفوف التي يجب تضمينها في التظليل عندما يحدد النمط تظليل الصفوف الفردية/الزوجية. |
| [getSemiHidden()](#getSemiHidden) | يحصل/يضبط ما إذا كان النمط مخفياً في معرض الأنماط ومن لوحة مهام الأنماط. |
| [getShading()](#getShading) | يحصل على كائن [Shading](../../com.aspose.words/shading/) الذي يشير إلى تنسيق التظليل لخلايا الجدول. |
| [getStyleIdentifier()](#getStyleIdentifier) | يحصل على معرف النمط المستقل عن اللغة لنمط مدمج. |
| [getStyles()](#getStyles) | يحصل على مجموعة الأنماط التي ينتمي إليها هذا النمط. |
| [getTopPadding()](#getTopPadding) | يحصل على مقدار المسافة (بالنقاط) لإضافتها فوق محتويات خلايا الجدول. |
| [getType()](#getType) | يحصل على نوع النمط (فقرة أو حرف). |
| [getUnhideWhenUsed()](#getUnhideWhenUsed) | يحصل/يضبط ما إذا كان النمط المستخدم في المستند الحالي يُظهر نفسه في معرض الأنماط ومن لوحة مهام الأنماط. |
| [getVerticalAlignment()](#getVerticalAlignment) | يحدد المحاذاة العمودية للخلايا. |
| [isHeading()](#isHeading) | صحيح عندما يكون النمط أحد أنماط العناوين المدمجة. |
| [isQuickStyle()](#isQuickStyle) | يحدد ما إذا كان هذا النمط معروضاً في معرض الأنماط السريعة داخل واجهة MS Word. |
| [isQuickStyle(boolean value)](#isQuickStyle-boolean) | يحدد ما إذا كان هذا النمط معروضاً في معرض الأنماط السريعة داخل واجهة MS Word. |
| [remove()](#remove) | يزيل النمط المحدد من المستند. |
| [removeParaAttr(int key)](#removeParaAttr-int) |  |
| [removeRunAttr(int key)](#removeRunAttr-int) |  |
| [resetToDefaultAttrs()](#resetToDefaultAttrs) |  |
| [setAlignment(int value)](#setAlignment-int) | يحدد محاذاة نمط الجدول. |
| [setAllowBreakAcrossPages(boolean value)](#setAllowBreakAcrossPages-boolean) | يضبط علمًا يشير إلى ما إذا كان مسموحًا للنص في صف الجدول أن ينقسم عبر فاصل صفحة. |
| [setAutomaticallyUpdate(boolean value)](#setAutomaticallyUpdate-boolean) | يحدد ما إذا كان هذا النمط يُعاد تعريفه تلقائيًا بناءً على القيمة المناسبة. |
| [setBaseStyleName(String value)](#setBaseStyleName-java.lang.String) | يحصل/يضبط اسم النمط الذي يُستند إليه هذا النمط. |
| [setBorderAttr(int key, Object value)](#setBorderAttr-int-java.lang.Object) |  |
| [setBottomPadding(double value)](#setBottomPadding-double) | يضبط مقدار المسافة (بالنقاط) لإضافتها أسفل محتويات خلايا الجدول. |
| [setCellAttr(int key, Object value)](#setCellAttr-int-java.lang.Object) |  |
| [setCellSpacing(double value)](#setCellSpacing-double) | يضبط مقدار المسافة (بالنقاط) بين الخلايا. |
| [setColumnStripe(int value)](#setColumnStripe-int) | يضبط عدد الأعمدة التي يجب تضمينها في التظليل عندما يحدد النمط تظليل الأعمدة الفردية/الزوجية. |
| [setLeftIndent(double value)](#setLeftIndent-double) | يضبط القيمة التي تمثل المسافة البادئة اليسرى للجدول. |
| [setLeftPadding(double value)](#setLeftPadding-double) | يضبط مقدار المسافة (بالنقاط) لإضافتها إلى يسار محتويات خلايا الجدول. |
| [setLinkedStyleName(String value)](#setLinkedStyleName-java.lang.String) | يحصل/يضبط اسم الـ[Style](../../com.aspose.words/style/) المرتبط بهذا. |
| [setLocked(boolean value)](#setLocked-boolean) | يحدد ما إذا كان هذا النمط مقفلاً. |
| [setName(String value)](#setName-java.lang.String) | يضبط اسم النمط. |
| [setNextParagraphStyleName(String value)](#setNextParagraphStyleName-java.lang.String) | يحصل/يضبط اسم النمط الذي سيُطبق تلقائياً على فقرة جديدة تُدرج بعد فقرة مُنسقة بالنمط المحدد. |
| [setParaAttr(int key, Object value)](#setParaAttr-int-java.lang.Object) |  |
| [setPriority(int value)](#setPriority-int) | يحصل/يضبط القيمة الصحيحة التي تمثل أولوية فرز الأنماط في لوحة مهام الأنماط. |
| [setRightPadding(double value)](#setRightPadding-double) | يضبط مقدار المسافة (بالنقاط) لإضافتها إلى يمين محتويات خلايا الجدول. |
| [setRowAttr(int key, Object value)](#setRowAttr-int-java.lang.Object) |  |
| [setRowStripe(int value)](#setRowStripe-int) | يضبط عدد الصفوف التي يجب تضمينها في التظليل عندما يحدد النمط تظليل الصفوف الفردية/الزوجية. |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object) |  |
| [setSemiHidden(boolean value)](#setSemiHidden-boolean) | يحصل/يضبط ما إذا كان النمط مخفياً في معرض الأنماط ومن لوحة مهام الأنماط. |
| [setTopPadding(double value)](#setTopPadding-double) | يضبط مقدار المسافة (بالنقاط) لإضافتها فوق محتويات خلايا الجدول. |
| [setUnhideWhenUsed(boolean value)](#setUnhideWhenUsed-boolean) | يحصل/يضبط ما إذا كان النمط المستخدم في المستند الحالي يُظهر نفسه في معرض الأنماط ومن لوحة مهام الأنماط. |
| [setVerticalAlignment(int value)](#setVerticalAlignment-int) | يحدد المحاذاة العمودية للخلايا. |
### clearCellAttrs() {#clearCellAttrs}
```
public void clearCellAttrs()
```




### clearParaAttrs() {#clearParaAttrs}
```
public void clearParaAttrs()
```




### clearRowAttrs() {#clearRowAttrs}
```
public void clearRowAttrs()
```




### clearRunAttrs() {#clearRunAttrs}
```
public void clearRunAttrs()
```




### equals(Style style) {#equals-com.aspose.words.Style}
```
public boolean equals(Style style)
```


يقارن بالنمط المحدد. يتم مقارنة معرّفات الأنماط (Istds) للأنماط المدمجة فقط. لا تُضمّن القيم الافتراضية للأنماط في المقارنة. يتم مقارنة النمط الأساسي، والنمط المرتبط، والنمط التالي للفقرة بشكل متكرر.

 **Examples:** 

يوضح كيفية استخدام الأسماء المستعارة للأنماط.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| style | [Style](../../com.aspose.words/style/) |  |

**Returns:**
boolean
### fetchCellAttr(int key) {#fetchCellAttr-int}
```
public Object fetchCellAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedBorderAttr(int key) {#fetchInheritedBorderAttr-int}
```
public Object fetchInheritedBorderAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedCellAttr(int key) {#fetchInheritedCellAttr-int}
```
public Object fetchInheritedCellAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedParaAttr(int key) {#fetchInheritedParaAttr-int}
```
public Object fetchInheritedParaAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRowAttr(int key) {#fetchInheritedRowAttr-int}
```
public Object fetchInheritedRowAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedRunAttr(int key) {#fetchInheritedRunAttr-int}
```
public Object fetchInheritedRunAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchInheritedShadingAttr(int key) {#fetchInheritedShadingAttr-int}
```
public Object fetchInheritedShadingAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchParaAttr(int key) {#fetchParaAttr-int}
```
public Object fetchParaAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### fetchRowAttr(int key) {#fetchRowAttr-int}
```
public Object fetchRowAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getAliases() {#getAliases}
```
public String[] getAliases()
```


يحصل على جميع الأسماء المستعارة لهذا النمط. إذا لم يكن للنمط أي أسماء مستعارة، يتم إرجاع مصفوفة فارغة من السلاسل.

 **Examples:** 

يوضح كيفية استخدام الأسماء المستعارة للأنماط.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

**Returns:**
java.lang.String[] - جميع الأسماء المستعارة لهذا النمط.
### getAlignment() {#getAlignment}
```
public int getAlignment()
```


يحدد محاذاة نمط الجدول.

 **Remarks:** 

القيمة الافتراضية هي [TableAlignment.LEFT](../../com.aspose.words/tablealignment/\#LEFT).

 **Examples:** 

يظهر كيفية ضبط موضع الجدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways of aligning a table horizontally.
 // 1 -  Use the "Alignment" property to align it to a location on the page, such as the center:
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAlignment(TableAlignment.CENTER);
 tableStyle.getBorders().setColor(Color.BLUE);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 // Insert a table and apply the style we created to it.
 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Aligned to the center of the page");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 table.setStyle(tableStyle);

 // 2 -  Use the "LeftIndent" to specify an indent from the left margin of the page:
 tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle2");
 tableStyle.setLeftIndent(55.0);
 tableStyle.getBorders().setColor(Color.GREEN);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 table = builder.startTable();
 builder.insertCell();
 builder.write("Aligned according to left indent");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 table.setStyle(tableStyle);

 doc.save(getArtifactsDir() + "Table.SetTableAlignment.docx");
 
```

**Returns:**
int - القيمة الصحيحة المقابلة. القيمة المرجعة هي واحدة من ثوابت [TableAlignment](../../com.aspose.words/tablealignment/).
### getAllowBreakAcrossPages() {#getAllowBreakAcrossPages}
```
public boolean getAllowBreakAcrossPages()
```


يحصل على علم يشير إلى ما إذا كان مسموحًا للنص في صف الجدول أن ينقسم عبر فاصل صفحة.

 **Remarks:** 

القيمة الافتراضية هي  true .

 **Examples:** 

يظهر كيفية إنشاء إعدادات نمط مخصصة للجدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
boolean - علم يشير إلى ما إذا كان مسموحًا للنص في صف الجدول أن ينقسم عبر فاصل صفحة.
### getAutomaticallyUpdate() {#getAutomaticallyUpdate}
```
public boolean getAutomaticallyUpdate()
```


يحدد ما إذا كان هذا النمط يُعاد تعريفه تلقائيًا بناءً على القيمة المناسبة.

 **Remarks:** 

إذا تم ضبط قيمة الخاصية إلى true، يقوم MS Word تلقائياً بإعادة تعريف النمط الحالي عندما يتم تعديل تنسيق الفقرة المناسب.

خاصية AutomaticallyUpdate تنطبق على أنماط الفقرة فقط.

القيمة الافتراضية هي false.

 **Examples:** 

يوضح كيفية إنشاء وتطبيق نمط مخصص.

```

 Document doc = new Document();

 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 style.getFont().setName("Times New Roman");
 style.getFont().setSize(16.0);
 style.getFont().setColor(Color.magenta);
 // Automatically redefine style.
 style.setAutomaticallyUpdate(true);

 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply one of the styles from the document to the paragraph that the document builder is creating.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle"));
 builder.writeln("Hello world!");

 Style firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 Assert.assertEquals(style, firstParagraphStyle);

 // Remove our custom style from the document's styles collection.
 doc.getStyles().get("MyStyle").remove();

 firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 // Any text that used a removed style reverts to the default formatting.
 Assert.assertFalse(IterableUtils.matchesAny(doc.getStyles(), s -> s.getName() == "MyStyle"));
 Assert.assertEquals("Times New Roman", firstParagraphStyle.getFont().getName());
 Assert.assertEquals(12.0d, firstParagraphStyle.getFont().getSize());
 Assert.assertEquals(0, firstParagraphStyle.getFont().getColor().getRGB());
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getBaseStyleName() {#getBaseStyleName}
```
public String getBaseStyleName()
```


يحصل/يضبط اسم النمط الذي يُستند إليه هذا النمط.

 **Remarks:** 

سيكون هذا سلسلة فارغة إذا لم يكن النمط مستندًا إلى أي نمط آخر ويمكن تعيينه كسلسلة فارغة.

 **Examples:** 

يوضح كيفية استخدام الأسماء المستعارة للأنماط.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getBorders() {#getBorders}
```
public BorderCollection getBorders()
```


يحصل على مجموعة حدود الخلايا الافتراضية للنمط.

 **Examples:** 

يظهر كيفية إنشاء إعدادات نمط مخصصة للجدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
[BorderCollection](../../com.aspose.words/bordercollection/) - The collection of default cell borders for the style.
### getBottomPadding() {#getBottomPadding}
```
public double getBottomPadding()
```


يحصل على مقدار المسافة (بالنقاط) لإضافتها أسفل محتويات خلايا الجدول.

 **Examples:** 

يظهر كيفية إنشاء إعدادات نمط مخصصة للجدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
double - مقدار المسافة (بالنقاط) لإضافتها أسفل محتويات خلايا الجدول.
### getBuiltIn() {#getBuiltIn}
```
public boolean getBuiltIn()
```


صحيح إذا كان هذا النمط أحد الأنماط المدمجة في MS Word.

 **Examples:** 

يوضح كيفية التمييز بين الأنماط المخصصة والأنماط المدمجة.

```

 Document doc = new Document();

 // When we create a document using Microsoft Word, or programmatically using Aspose.Words,
 // the document will come with a collection of styles to apply to its text to modify its appearance.
 // We can access these built-in styles via the document's "Styles" collection.
 // These styles will all have the "BuiltIn" flag set to "true".
 Style style = doc.getStyles().get("Emphasis");

 Assert.assertTrue(style.getBuiltIn());

 // Create a custom style and add it to the collection.
 // Custom styles such as this will have the "BuiltIn" flag set to "false".
 style = doc.getStyles().add(StyleType.CHARACTER, "MyStyle");
 style.getFont().setColor(Color.RED);
 style.getFont().setName("Courier New");

 Assert.assertFalse(style.getBuiltIn());
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getCellSpacing() {#getCellSpacing}
```
public double getCellSpacing()
```


يحصل على مقدار المسافة (بالنقاط) بين الخلايا.

 **Examples:** 

يظهر كيفية إنشاء إعدادات نمط مخصصة للجدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
double - مقدار المسافة (بالنقاط) بين الخلايا.
### getColumnStripe() {#getColumnStripe}
```
public int getColumnStripe()
```


يحصل على عدد الأعمدة التي يجب تضمينها في التظليل عندما يحدد النمط تظليل الأعمدة الفردية/الزوجية.

 **Examples:** 

يظهر كيفية إنشاء أنماط جدول شرطية تتناوب بين الصفوف.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can configure a conditional style of a table to apply a different color to the row/column,
 // based on whether the row/column is even or odd, creating an alternating color pattern.
 // We can also apply a number n to the row/column banding,
 // meaning that the color alternates after every n rows/columns instead of one.
 // Create a table where single columns and rows will band the columns will banded in threes.
 Table table = builder.startTable();

 for (int i = 0; i < 15; i++) {
     for (int j = 0; j < 4; j++) {
         builder.insertCell();
         builder.writeln(MessageFormat.format("{0} column.", (j % 2 == 0 ? "Even" : "Odd")));
         builder.write(MessageFormat.format("Row banding {0}.", (i % 3 == 0 ? "start" : "continuation")));
     }
     builder.endRow();
 }

 builder.endTable();

 // Apply a line style to all the borders of the table.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOUBLE);

 // Set the two colors, which will alternate over every 3 rows.
 tableStyle.setRowStripe(3);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.ODD_ROW_BANDING).getShading().setBackgroundPatternColor(Color.BLUE);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.EVEN_ROW_BANDING).getShading().setBackgroundPatternColor(Color.CYAN);

 // Set a color to apply to every even column, which will override any custom row coloring.
 tableStyle.setColumnStripe(1);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.EVEN_COLUMN_BANDING).getShading().setBackgroundPatternColor(Color.RED);

 table.setStyle(tableStyle);

 // The "StyleOptions" property enables row banding by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // Use the "StyleOptions" property also to enable column banding.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.COLUMN_BANDS);

 doc.save(getArtifactsDir() + "Table.AlternatingRowStyles.docx");
 
```

**Returns:**
int - عدد الأعمدة التي يجب تضمينها في التظليل عندما يحدد النمط تظليل الأعمدة الفردية/الزوجية.
### getConditionalStyles() {#getConditionalStyles}
```
public ConditionalStyleCollection getConditionalStyles()
```


مجموعة من الأنماط الشرطية التي يمكن تعريفها لهذا نمط الجدول.

 **Examples:** 

يظهر كيفية العمل مع أنماط مناطق معينة في جدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Cell 1");
 builder.insertCell();
 builder.write("Cell 2");
 builder.endRow();
 builder.insertCell();
 builder.write("Cell 3");
 builder.insertCell();
 builder.write("Cell 4");
 builder.endTable();

 // Create a custom table style.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");

 // Conditional styles are formatting changes that affect only some of the table's cells
 // based on a predicate, such as the cells being in the last row.
 // Below are three ways of accessing a table style's conditional styles from the "ConditionalStyles" collection.
 // 1 -  By style type:
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.FIRST_ROW).getShading().setBackgroundPatternColor(Color.BLUE);

 // 2 -  By index:
 tableStyle.getConditionalStyles().get(0).getBorders().setColor(Color.BLACK);
 tableStyle.getConditionalStyles().get(0).getBorders().setLineStyle(LineStyle.DOT_DASH);
 Assert.assertEquals(ConditionalStyleType.FIRST_ROW, tableStyle.getConditionalStyles().get(0).getType());

 // 3 -  As a property:
 tableStyle.getConditionalStyles().getFirstRow().getParagraphFormat().setAlignment(ParagraphAlignment.CENTER);

 // Apply padding and text formatting to conditional styles.
 tableStyle.getConditionalStyles().getLastRow().setBottomPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setLeftPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setRightPadding(10.0);
 tableStyle.getConditionalStyles().getLastRow().setTopPadding(10.0);
 tableStyle.getConditionalStyles().getLastColumn().getFont().setBold(true);

 // List all possible style conditions.
 Iterator enumerator = tableStyle.getConditionalStyles().iterator();
 while (enumerator.hasNext()) {
     ConditionalStyle currentStyle = enumerator.next();
     if (currentStyle != null) System.out.println(currentStyle.getType());
 }

 // Apply the custom style, which contains all conditional styles, to the table.
 table.setStyle(tableStyle);

 // Our style applies some conditional styles by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // We will need to enable all other styles ourselves via the "StyleOptions" property.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.LAST_ROW | TableStyleOptions.LAST_COLUMN);

 doc.save(getArtifactsDir() + "Table.ConditionalStyles.docx");
 
```

**Returns:**
[ConditionalStyleCollection](../../com.aspose.words/conditionalstylecollection/) - The corresponding [ConditionalStyleCollection](../../com.aspose.words/conditionalstylecollection/) value.
### getDirectBorderAttr(int key) {#getDirectBorderAttr-int}
```
public Object getDirectBorderAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectCellAttr(int key) {#getDirectCellAttr-int}
```
public Object getDirectCellAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectParaAttr(int key) {#getDirectParaAttr-int}
```
public Object getDirectParaAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectParaAttr(int key, int revisionsView) {#getDirectParaAttr-int-int}
```
public Object getDirectParaAttr(int key, int revisionsView)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getDirectRowAttr(int key) {#getDirectRowAttr-int}
```
public Object getDirectRowAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key) {#getDirectRunAttr-int}
```
public Object getDirectRunAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key, int revisionsView) {#getDirectRunAttr-int-int}
```
public Object getDirectRunAttr(int key, int revisionsView)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


يحصل على المستند المالك.

 **Examples:** 

يوضح كيفية الوصول إلى مجموعة أنماط المستند.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase/) - The owner document.
### getFont() {#getFont}
```
public Font getFont()
```


يحصل على تنسيق الأحرف للنمط.

 **Remarks:** 

بالنسبة لأنماط القوائم، تُعيد هذه الخاصية null .

 **Examples:** 

يوضح كيفية إنشاء وتطبيق نمط مخصص.

```

 Document doc = new Document();

 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 style.getFont().setName("Times New Roman");
 style.getFont().setSize(16.0);
 style.getFont().setColor(Color.magenta);
 // Automatically redefine style.
 style.setAutomaticallyUpdate(true);

 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply one of the styles from the document to the paragraph that the document builder is creating.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle"));
 builder.writeln("Hello world!");

 Style firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 Assert.assertEquals(style, firstParagraphStyle);

 // Remove our custom style from the document's styles collection.
 doc.getStyles().get("MyStyle").remove();

 firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 // Any text that used a removed style reverts to the default formatting.
 Assert.assertFalse(IterableUtils.matchesAny(doc.getStyles(), s -> s.getName() == "MyStyle"));
 Assert.assertEquals("Times New Roman", firstParagraphStyle.getFont().getName());
 Assert.assertEquals(12.0d, firstParagraphStyle.getFont().getSize());
 Assert.assertEquals(0, firstParagraphStyle.getFont().getColor().getRGB());
 
```

يوضح كيفية إنشاء واستخدام نمط فقرة مع تنسيق القوائم.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a custom paragraph style.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle1");
 style.getFont().setSize(24.0);
 style.getFont().setName("Verdana");
 style.getParagraphFormat().setSpaceAfter(12.0);

 // Create a list and make sure the paragraphs that use this style will use this list.
 style.getListFormat().setList(doc.getLists().add(ListTemplate.BULLET_DEFAULT));
 style.getListFormat().setListLevelNumber(0);

 // Apply the paragraph style to the document builder's current paragraph, and then add some text.
 builder.getParagraphFormat().setStyle(style);
 builder.writeln("Hello World: MyStyle1, bulleted list.");

 // Change the document builder's style to one that has no list formatting and write another paragraph.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln("Hello World: Normal.");

 builder.getDocument().save(getArtifactsDir() + "Styles.ParagraphStyleBulletedList.docx");
 
```

**Returns:**
[Font](../../com.aspose.words/font/) - The character formatting of the style.
### getLeftIndent() {#getLeftIndent}
```
public double getLeftIndent()
```


يحصل على القيمة التي تمثل المسافة البادئة اليسرى للجدول.

 **Examples:** 

يظهر كيفية ضبط موضع الجدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways of aligning a table horizontally.
 // 1 -  Use the "Alignment" property to align it to a location on the page, such as the center:
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAlignment(TableAlignment.CENTER);
 tableStyle.getBorders().setColor(Color.BLUE);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 // Insert a table and apply the style we created to it.
 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Aligned to the center of the page");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 table.setStyle(tableStyle);

 // 2 -  Use the "LeftIndent" to specify an indent from the left margin of the page:
 tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle2");
 tableStyle.setLeftIndent(55.0);
 tableStyle.getBorders().setColor(Color.GREEN);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 table = builder.startTable();
 builder.insertCell();
 builder.write("Aligned according to left indent");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 table.setStyle(tableStyle);

 doc.save(getArtifactsDir() + "Table.SetTableAlignment.docx");
 
```

**Returns:**
double - القيمة التي تمثل المسافة البادئة اليسرى للجدول.
### getLeftPadding() {#getLeftPadding}
```
public double getLeftPadding()
```


يحصل على مقدار المسافة (بالنقاط) لإضافتها إلى يسار محتويات خلايا الجدول.

 **Examples:** 

يظهر كيفية إنشاء إعدادات نمط مخصصة للجدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
double - مقدار المسافة (بالنقاط) لإضافتها إلى يسار محتويات خلايا الجدول.
### getLinkedStyleName() {#getLinkedStyleName}
```
public String getLinkedStyleName()
```


يحصل/يضبط اسم الـ [Style](../../com.aspose.words/style/) المرتبط بهذا. يُعيد سلسلة فارغة إذا لم يتم ربط أي أنماط.

 **Remarks:** 

يسمح فقط بربط نمط الفقرة بنمط الحرف والعكس بالعكس.

ضبط LinkedStyleName للنمط الحالي يؤدي تلقائيًا إلى ضبط LinkedStyleName للنمط المرتبط.

تعيين السلسلة الفارغة يعادل إلغاء ربط النمط المرتبط مسبقًا.

 **Examples:** 

يوضح كيفية استخدام الأسماء المستعارة للأنماط.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

يوضح كيفية ربط الأنماط ببعضها البعض.

```

 Document doc = new Document();

 Style styleHeading1 = doc.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1);

 Style styleHeading1Char = doc.getStyles().add(StyleType.CHARACTER, "Heading 1 Char");
 styleHeading1Char.getFont().setName("Verdana");
 styleHeading1Char.getFont().setBold(true);
 styleHeading1Char.getFont().getBorder().setLineStyle(LineStyle.DOT);
 styleHeading1Char.getFont().getBorder().setLineWidth(15.0);

 styleHeading1.setLinkedStyleName("Heading 1 Char");

 Assert.assertEquals("Heading 1 Char", styleHeading1.getLinkedStyleName());
 Assert.assertEquals("Heading 1", styleHeading1Char.getLinkedStyleName());
 
```

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getList() {#getList}
```
public List getList()
```


يحصل على القائمة التي تحدد تنسيق نمط القائمة هذا.

 **Remarks:** 

هذه الخاصية صالحة فقط لأنماط القوائم. بالنسبة لأنواع الأنماط الأخرى تُعيد هذه الخاصية null .

 **Examples:** 

يوضح كيفية إنشاء نمط قائمة واستخدامه في مستند.

```

 Document doc = new Document();

 // A list allows us to organize and decorate sets of paragraphs with prefix symbols and indents.
 // We can create nested lists by increasing the indent level.
 // We can begin and end a list by using a document builder's "ListFormat" property.
 // Each paragraph that we add between a list's start and the end will become an item in the list.
 // We can contain an entire List object within a style.
 Style listStyle = doc.getStyles().add(StyleType.LIST, "MyListStyle");

 List list1 = listStyle.getList();

 Assert.assertTrue(list1.isListStyleDefinition());
 Assert.assertFalse(list1.isListStyleReference());
 Assert.assertTrue(list1.isMultiLevel());
 Assert.assertEquals(listStyle, list1.getStyle());

 // Change the appearance of all list levels in our list.
 for (ListLevel level : list1.getListLevels()) {
     level.getFont().setName("Verdana");
     level.getFont().setColor(Color.BLUE);
     level.getFont().setBold(true);
 }

 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Using list style first time:");

 // Create another list from a list within a style.
 List list2 = doc.getLists().add(listStyle);

 Assert.assertFalse(list2.isListStyleDefinition());
 Assert.assertTrue(list2.isListStyleReference());
 Assert.assertEquals(listStyle, list2.getStyle());

 // Add some list items that our list will format.
 builder.getListFormat().setList(list2);
 builder.writeln("Item 1");
 builder.writeln("Item 2");
 builder.getListFormat().removeNumbers();

 builder.writeln("Using list style second time:");

 // Create and apply another list based on the list style.
 List list3 = doc.getLists().add(listStyle);
 builder.getListFormat().setList(list3);
 builder.writeln("Item 1");
 builder.writeln("Item 2");
 builder.getListFormat().removeNumbers();

 builder.getDocument().save(getArtifactsDir() + "Lists.CreateAndUseListStyle.docx");
 
```

**Returns:**
[List](../../com.aspose.words/list/) - The list that defines formatting of this list style.
### getListFormat() {#getListFormat}
```
public ListFormat getListFormat()
```


يوفر الوصول إلى خصائص تنسيق القائمة لنمط الفقرة.

 **Remarks:** 

هذه الخاصية صالحة فقط لأنماط الفقرات. بالنسبة لأنواع الأنماط الأخرى تُعيد هذه الخاصية null .

 **Examples:** 

يوضح كيفية إنشاء واستخدام نمط فقرة مع تنسيق القوائم.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a custom paragraph style.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle1");
 style.getFont().setSize(24.0);
 style.getFont().setName("Verdana");
 style.getParagraphFormat().setSpaceAfter(12.0);

 // Create a list and make sure the paragraphs that use this style will use this list.
 style.getListFormat().setList(doc.getLists().add(ListTemplate.BULLET_DEFAULT));
 style.getListFormat().setListLevelNumber(0);

 // Apply the paragraph style to the document builder's current paragraph, and then add some text.
 builder.getParagraphFormat().setStyle(style);
 builder.writeln("Hello World: MyStyle1, bulleted list.");

 // Change the document builder's style to one that has no list formatting and write another paragraph.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln("Hello World: Normal.");

 builder.getDocument().save(getArtifactsDir() + "Styles.ParagraphStyleBulletedList.docx");
 
```

**Returns:**
[ListFormat](../../com.aspose.words/listformat/) - The corresponding [ListFormat](../../com.aspose.words/listformat/) value.
### getLocked() {#getLocked}
```
public boolean getLocked()
```


يحدد ما إذا كان هذا النمط مقفلاً.

 **Examples:** 

يوضح كيفية قفل النمط.

```

 Document doc = new Document();

 Style styleHeading1 = doc.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1);
 if (!styleHeading1.getLocked())
     styleHeading1.setLocked(true);

 doc.save(getArtifactsDir() + "Styles.LockStyle.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getName() {#getName}
```
public String getName()
```


يحصل على اسم النمط.

 **Remarks:** 

لا يمكن أن تكون سلسلة فارغة.

إذا كان هناك نمط بالفعل بهذا الاسم في المجموعة، فسيتم استبداله بهذا النمط. جميع العقد المتأثرة ستشير إلى النمط الجديد.

 **Examples:** 

يوضح كيفية الوصول إلى مجموعة أنماط المستند.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
java.lang.String - اسم النمط.
### getNextParagraphStyleName() {#getNextParagraphStyleName}
```
public String getNextParagraphStyleName()
```


يحصل/يضبط اسم النمط الذي سيُطبق تلقائياً على فقرة جديدة تُدرج بعد فقرة مُنسقة بالنمط المحدد.

 **Remarks:** 

هذه الخاصية لا يستخدمها Aspose.Words. سيتم تطبيق نمط الفقرة التالي تلقائيًا فقط عندما تقوم بتحرير المستند في MS Word.

 **Examples:** 

يوضح كيفية الوصول إلى مجموعة أنماط المستند.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
java.lang.String - القيمة المقابلة من نوع java.lang.String.
### getParagraphFormat() {#getParagraphFormat}
```
public ParagraphFormat getParagraphFormat()
```


يحصل على تنسيق الفقرة للنمط.

 **Remarks:** 

بالنسبة لأنماط الحرف والقائمة تُعيد هذه الخاصية null .

 **Examples:** 

يوضح كيفية إنشاء واستخدام نمط فقرة مع تنسيق القوائم.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Create a custom paragraph style.
 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle1");
 style.getFont().setSize(24.0);
 style.getFont().setName("Verdana");
 style.getParagraphFormat().setSpaceAfter(12.0);

 // Create a list and make sure the paragraphs that use this style will use this list.
 style.getListFormat().setList(doc.getLists().add(ListTemplate.BULLET_DEFAULT));
 style.getListFormat().setListLevelNumber(0);

 // Apply the paragraph style to the document builder's current paragraph, and then add some text.
 builder.getParagraphFormat().setStyle(style);
 builder.writeln("Hello World: MyStyle1, bulleted list.");

 // Change the document builder's style to one that has no list formatting and write another paragraph.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("Normal"));
 builder.writeln("Hello World: Normal.");

 builder.getDocument().save(getArtifactsDir() + "Styles.ParagraphStyleBulletedList.docx");
 
```

**Returns:**
[ParagraphFormat](../../com.aspose.words/paragraphformat/) - The paragraph formatting of the style.
### getPriority() {#getPriority}
```
public int getPriority()
```


يحصل/يضبط القيمة الصحيحة التي تمثل أولوية فرز الأنماط في لوحة مهام الأنماط.

 **Examples:** 

يوضح كيفية إعطاء أولوية وإخفاء النمط.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Returns:**
int - القيمة المقابلة  int .
### getRightPadding() {#getRightPadding}
```
public double getRightPadding()
```


يحصل على مقدار المسافة (بالنقاط) لإضافتها إلى يمين محتويات خلايا الجدول.

 **Examples:** 

يظهر كيفية إنشاء إعدادات نمط مخصصة للجدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
double - مقدار المسافة (بالنقاط) لإضافتها إلى يمين محتويات خلايا الجدول.
### getRowStripe() {#getRowStripe}
```
public int getRowStripe()
```


يحصل على عدد الصفوف التي يجب تضمينها في التظليل عندما يحدد النمط تظليل الصفوف الفردية/الزوجية.

 **Examples:** 

يظهر كيفية إنشاء أنماط جدول شرطية تتناوب بين الصفوف.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can configure a conditional style of a table to apply a different color to the row/column,
 // based on whether the row/column is even or odd, creating an alternating color pattern.
 // We can also apply a number n to the row/column banding,
 // meaning that the color alternates after every n rows/columns instead of one.
 // Create a table where single columns and rows will band the columns will banded in threes.
 Table table = builder.startTable();

 for (int i = 0; i < 15; i++) {
     for (int j = 0; j < 4; j++) {
         builder.insertCell();
         builder.writeln(MessageFormat.format("{0} column.", (j % 2 == 0 ? "Even" : "Odd")));
         builder.write(MessageFormat.format("Row banding {0}.", (i % 3 == 0 ? "start" : "continuation")));
     }
     builder.endRow();
 }

 builder.endTable();

 // Apply a line style to all the borders of the table.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOUBLE);

 // Set the two colors, which will alternate over every 3 rows.
 tableStyle.setRowStripe(3);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.ODD_ROW_BANDING).getShading().setBackgroundPatternColor(Color.BLUE);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.EVEN_ROW_BANDING).getShading().setBackgroundPatternColor(Color.CYAN);

 // Set a color to apply to every even column, which will override any custom row coloring.
 tableStyle.setColumnStripe(1);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.EVEN_COLUMN_BANDING).getShading().setBackgroundPatternColor(Color.RED);

 table.setStyle(tableStyle);

 // The "StyleOptions" property enables row banding by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // Use the "StyleOptions" property also to enable column banding.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.COLUMN_BANDS);

 doc.save(getArtifactsDir() + "Table.AlternatingRowStyles.docx");
 
```

**Returns:**
int - عدد الصفوف التي يجب تضمينها في التظليل عندما يحدد النمط تظليل الصفوف الفردية/الزوجية.
### getSemiHidden() {#getSemiHidden}
```
public boolean getSemiHidden()
```


يحصل/يضبط ما إذا كان النمط مخفياً في معرض الأنماط ومن لوحة مهام الأنماط.

 **Examples:** 

يوضح كيفية إعطاء أولوية وإخفاء النمط.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getShading() {#getShading}
```
public Shading getShading()
```


يحصل على كائن [Shading](../../com.aspose.words/shading/) الذي يشير إلى تنسيق التظليل لخلايا الجدول.

 **Examples:** 

يظهر كيفية إنشاء إعدادات نمط مخصصة للجدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
[Shading](../../com.aspose.words/shading/) - A [Shading](../../com.aspose.words/shading/) object that refers to the shading formatting for table cells.
### getStyleIdentifier() {#getStyleIdentifier}
```
public int getStyleIdentifier()
```


يحصل على معرف النمط المستقل عن اللغة لنمط مدمج.

 **Remarks:** 

بالنسبة للأنماط المعرفة من قبل المستخدم (المخصصة)، تُعيد هذه الخاصية [StyleIdentifier.USER](../../com.aspose.words/styleidentifier/\\#USER).

 **Examples:** 

يعرض كيفية تعديل موضع علامة التبويب اليمنى في الفقرات المتعلقة بالفهرس.

```

 Document doc = new Document(getMyDir() + "Table of contents.docx");

 // Iterate through all paragraphs with TOC result-based styles; this is any style between TOC and TOC9.
 for (Paragraph para : (Iterable) doc.getChildNodes(NodeType.PARAGRAPH, true)) {
     if (para.getParagraphFormat().getStyle().getStyleIdentifier() >= StyleIdentifier.TOC_1
             && para.getParagraphFormat().getStyle().getStyleIdentifier() <= StyleIdentifier.TOC_9) {
         // Get the first tab used in this paragraph, this should be the tab used to align the page numbers.
         TabStop tab = para.getParagraphFormat().getTabStops().get(0);

         // Replace the first default tab, stop with a custom tab stop.
         para.getParagraphFormat().getTabStops().removeByPosition(tab.getPosition());
         para.getParagraphFormat().getTabStops().add(tab.getPosition() - 50.0, tab.getAlignment(), tab.getLeader());
     }
 }

 doc.save(getArtifactsDir() + "Styles.ChangeTocsTabStops.docx");
 
```

**Returns:**
int - معرف النمط المستقل عن اللغة لمظهر مدمج. القيمة المرجعة هي واحدة من ثوابت [StyleIdentifier](../../com.aspose.words/styleidentifier/).
### getStyles() {#getStyles}
```
public StyleCollection getStyles()
```


يحصل على مجموعة الأنماط التي ينتمي إليها هذا النمط.

 **Examples:** 

يوضح كيفية الوصول إلى مجموعة أنماط المستند.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
[StyleCollection](../../com.aspose.words/stylecollection/) - The collection of styles this style belongs to.
### getTopPadding() {#getTopPadding}
```
public double getTopPadding()
```


يحصل على مقدار المسافة (بالنقاط) لإضافتها فوق محتويات خلايا الجدول.

 **Examples:** 

يظهر كيفية إنشاء إعدادات نمط مخصصة للجدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
double - مقدار المسافة (بالنقاط) لإضافتها فوق محتويات خلايا الجدول.
### getType() {#getType}
```
public int getType()
```


يحصل على نوع النمط (فقرة أو حرف).

 **Examples:** 

يوضح كيفية الوصول إلى مجموعة أنماط المستند.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
int - نوع النمط (فقرة أو حرف). القيمة المرجعة هي واحدة من ثوابت [StyleType](../../com.aspose.words/styletype/).
### getUnhideWhenUsed() {#getUnhideWhenUsed}
```
public boolean getUnhideWhenUsed()
```


يحصل/يضبط ما إذا كان النمط المستخدم في المستند الحالي يُظهر من معرض الأنماط ومن لوحة مهام الأنماط. True عندما يجب إظهار النمط المستخدم في معرض الأنماط.

 **Examples:** 

يوضح كيفية إعطاء أولوية وإخفاء النمط.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getVerticalAlignment() {#getVerticalAlignment}
```
public int getVerticalAlignment()
```


يحدد المحاذاة العمودية للخلايا.

 **Remarks:** 

القيمة الافتراضية هي [CellVerticalAlignment.TOP](../../com.aspose.words/cellverticalalignment/#TOP).

 **Examples:** 

يظهر كيفية إنشاء إعدادات نمط مخصصة للجدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Returns:**
int - القيمة int المقابلة. القيمة المرجعة هي واحدة من ثوابت [CellVerticalAlignment](../../com.aspose.words/cellverticalalignment/).
### isHeading() {#isHeading}
```
public boolean isHeading()
```


صحيح عندما يكون النمط أحد أنماط العناوين المدمجة.

 **Examples:** 

يوضح كيفية الوصول إلى مجموعة أنماط المستند.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### isQuickStyle() {#isQuickStyle}
```
public boolean isQuickStyle()
```


يحدد ما إذا كان هذا النمط معروضاً في معرض الأنماط السريعة داخل واجهة MS Word.

 **Examples:** 

يوضح كيفية الوصول إلى مجموعة أنماط المستند.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### isQuickStyle(boolean value) {#isQuickStyle-boolean}
```
public void isQuickStyle(boolean value)
```


يحدد ما إذا كان هذا النمط معروضاً في معرض الأنماط السريعة داخل واجهة MS Word.

 **Examples:** 

يوضح كيفية الوصول إلى مجموعة أنماط المستند.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### remove() {#remove}
```
public void remove()
```


يزيل النمط المحدد من المستند.

 **Remarks:** 

إزالة النمط لها التأثيرات التالية على نموذج المستند:

 *  All references to the style are removed from corresponding paragraphs, runs and tables.
 *  If base style is removed its formatting is moved to child styles.
 *  If style to be deleted has a linked style, then both of these are deleted.

 **Examples:** 

يوضح كيفية إنشاء وتطبيق نمط مخصص.

```

 Document doc = new Document();

 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 style.getFont().setName("Times New Roman");
 style.getFont().setSize(16.0);
 style.getFont().setColor(Color.magenta);
 // Automatically redefine style.
 style.setAutomaticallyUpdate(true);

 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply one of the styles from the document to the paragraph that the document builder is creating.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle"));
 builder.writeln("Hello world!");

 Style firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 Assert.assertEquals(style, firstParagraphStyle);

 // Remove our custom style from the document's styles collection.
 doc.getStyles().get("MyStyle").remove();

 firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 // Any text that used a removed style reverts to the default formatting.
 Assert.assertFalse(IterableUtils.matchesAny(doc.getStyles(), s -> s.getName() == "MyStyle"));
 Assert.assertEquals("Times New Roman", firstParagraphStyle.getFont().getName());
 Assert.assertEquals(12.0d, firstParagraphStyle.getFont().getSize());
 Assert.assertEquals(0, firstParagraphStyle.getFont().getColor().getRGB());
 
```

### removeParaAttr(int key) {#removeParaAttr-int}
```
public void removeParaAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

### removeRunAttr(int key) {#removeRunAttr-int}
```
public void removeRunAttr(int key)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |

### resetToDefaultAttrs() {#resetToDefaultAttrs}
```
public void resetToDefaultAttrs()
```




### setAlignment(int value) {#setAlignment-int}
```
public void setAlignment(int value)
```


يحدد محاذاة نمط الجدول.

 **Remarks:** 

القيمة الافتراضية هي [TableAlignment.LEFT](../../com.aspose.words/tablealignment/\#LEFT).

 **Examples:** 

يظهر كيفية ضبط موضع الجدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways of aligning a table horizontally.
 // 1 -  Use the "Alignment" property to align it to a location on the page, such as the center:
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAlignment(TableAlignment.CENTER);
 tableStyle.getBorders().setColor(Color.BLUE);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 // Insert a table and apply the style we created to it.
 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Aligned to the center of the page");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 table.setStyle(tableStyle);

 // 2 -  Use the "LeftIndent" to specify an indent from the left margin of the page:
 tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle2");
 tableStyle.setLeftIndent(55.0);
 tableStyle.getBorders().setColor(Color.GREEN);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 table = builder.startTable();
 builder.insertCell();
 builder.write("Aligned according to left indent");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 table.setStyle(tableStyle);

 doc.save(getArtifactsDir() + "Table.SetTableAlignment.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | القيمة int المقابلة. يجب أن تكون القيمة واحدة من ثوابت [TableAlignment](../../com.aspose.words/tablealignment/). |

### setAllowBreakAcrossPages(boolean value) {#setAllowBreakAcrossPages-boolean}
```
public void setAllowBreakAcrossPages(boolean value)
```


يضبط علمًا يشير إلى ما إذا كان مسموحًا للنص في صف الجدول أن ينقسم عبر فاصل صفحة.

 **Remarks:** 

القيمة الافتراضية هي  true .

 **Examples:** 

يظهر كيفية إنشاء إعدادات نمط مخصصة للجدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | علامة تشير إلى ما إذا كان مسموحًا للنص في صف جدول أن ينقسم عبر فاصل صفحة. |

### setAutomaticallyUpdate(boolean value) {#setAutomaticallyUpdate-boolean}
```
public void setAutomaticallyUpdate(boolean value)
```


يحدد ما إذا كان هذا النمط يُعاد تعريفه تلقائيًا بناءً على القيمة المناسبة.

 **Remarks:** 

إذا تم ضبط قيمة الخاصية إلى true، يقوم MS Word تلقائياً بإعادة تعريف النمط الحالي عندما يتم تعديل تنسيق الفقرة المناسب.

خاصية AutomaticallyUpdate تنطبق على أنماط الفقرة فقط.

القيمة الافتراضية هي false.

 **Examples:** 

يوضح كيفية إنشاء وتطبيق نمط مخصص.

```

 Document doc = new Document();

 Style style = doc.getStyles().add(StyleType.PARAGRAPH, "MyStyle");
 style.getFont().setName("Times New Roman");
 style.getFont().setSize(16.0);
 style.getFont().setColor(Color.magenta);
 // Automatically redefine style.
 style.setAutomaticallyUpdate(true);

 DocumentBuilder builder = new DocumentBuilder(doc);

 // Apply one of the styles from the document to the paragraph that the document builder is creating.
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle"));
 builder.writeln("Hello world!");

 Style firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 Assert.assertEquals(style, firstParagraphStyle);

 // Remove our custom style from the document's styles collection.
 doc.getStyles().get("MyStyle").remove();

 firstParagraphStyle = doc.getFirstSection().getBody().getFirstParagraph().getParagraphFormat().getStyle();

 // Any text that used a removed style reverts to the default formatting.
 Assert.assertFalse(IterableUtils.matchesAny(doc.getStyles(), s -> s.getName() == "MyStyle"));
 Assert.assertEquals("Times New Roman", firstParagraphStyle.getFont().getName());
 Assert.assertEquals(12.0d, firstParagraphStyle.getFont().getSize());
 Assert.assertEquals(0, firstParagraphStyle.getFont().getColor().getRGB());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setBaseStyleName(String value) {#setBaseStyleName-java.lang.String}
```
public void setBaseStyleName(String value)
```


يحصل/يضبط اسم النمط الذي يُستند إليه هذا النمط.

 **Remarks:** 

سيكون هذا سلسلة فارغة إذا لم يكن النمط مستندًا إلى أي نمط آخر ويمكن تعيينه كسلسلة فارغة.

 **Examples:** 

يوضح كيفية استخدام الأسماء المستعارة للأنماط.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

### setBorderAttr(int key, Object value) {#setBorderAttr-int-java.lang.Object}
```
public void setBorderAttr(int key, Object value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |
| قيمة | java.lang.Object |  |

### setBottomPadding(double value) {#setBottomPadding-double}
```
public void setBottomPadding(double value)
```


يضبط مقدار المسافة (بالنقاط) لإضافتها أسفل محتويات خلايا الجدول.

 **Examples:** 

يظهر كيفية إنشاء إعدادات نمط مخصصة للجدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | كمية المسافة (بالنقاط) لإضافتها أسفل محتويات خلايا الجدول. |

### setCellAttr(int key, Object value) {#setCellAttr-int-java.lang.Object}
```
public void setCellAttr(int key, Object value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |
| قيمة | java.lang.Object |  |

### setCellSpacing(double value) {#setCellSpacing-double}
```
public void setCellSpacing(double value)
```


يضبط مقدار المسافة (بالنقاط) بين الخلايا.

 **Examples:** 

يظهر كيفية إنشاء إعدادات نمط مخصصة للجدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | كمية المسافة (بالنقاط) بين الخلايا. |

### setColumnStripe(int value) {#setColumnStripe-int}
```
public void setColumnStripe(int value)
```


يضبط عدد الأعمدة التي يجب تضمينها في التظليل عندما يحدد النمط تظليل الأعمدة الفردية/الزوجية.

 **Examples:** 

يظهر كيفية إنشاء أنماط جدول شرطية تتناوب بين الصفوف.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can configure a conditional style of a table to apply a different color to the row/column,
 // based on whether the row/column is even or odd, creating an alternating color pattern.
 // We can also apply a number n to the row/column banding,
 // meaning that the color alternates after every n rows/columns instead of one.
 // Create a table where single columns and rows will band the columns will banded in threes.
 Table table = builder.startTable();

 for (int i = 0; i < 15; i++) {
     for (int j = 0; j < 4; j++) {
         builder.insertCell();
         builder.writeln(MessageFormat.format("{0} column.", (j % 2 == 0 ? "Even" : "Odd")));
         builder.write(MessageFormat.format("Row banding {0}.", (i % 3 == 0 ? "start" : "continuation")));
     }
     builder.endRow();
 }

 builder.endTable();

 // Apply a line style to all the borders of the table.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOUBLE);

 // Set the two colors, which will alternate over every 3 rows.
 tableStyle.setRowStripe(3);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.ODD_ROW_BANDING).getShading().setBackgroundPatternColor(Color.BLUE);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.EVEN_ROW_BANDING).getShading().setBackgroundPatternColor(Color.CYAN);

 // Set a color to apply to every even column, which will override any custom row coloring.
 tableStyle.setColumnStripe(1);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.EVEN_COLUMN_BANDING).getShading().setBackgroundPatternColor(Color.RED);

 table.setStyle(tableStyle);

 // The "StyleOptions" property enables row banding by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // Use the "StyleOptions" property also to enable column banding.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.COLUMN_BANDS);

 doc.save(getArtifactsDir() + "Table.AlternatingRowStyles.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | عدد الأعمدة التي يجب تضمينها في التظليل عندما يحدد النمط تظليل الأعمدة الفردية/الزوجية. |

### setLeftIndent(double value) {#setLeftIndent-double}
```
public void setLeftIndent(double value)
```


يضبط القيمة التي تمثل المسافة البادئة اليسرى للجدول.

 **Examples:** 

يظهر كيفية ضبط موضع الجدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Below are two ways of aligning a table horizontally.
 // 1 -  Use the "Alignment" property to align it to a location on the page, such as the center:
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAlignment(TableAlignment.CENTER);
 tableStyle.getBorders().setColor(Color.BLUE);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 // Insert a table and apply the style we created to it.
 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Aligned to the center of the page");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 table.setStyle(tableStyle);

 // 2 -  Use the "LeftIndent" to specify an indent from the left margin of the page:
 tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle2");
 tableStyle.setLeftIndent(55.0);
 tableStyle.getBorders().setColor(Color.GREEN);
 tableStyle.getBorders().setLineStyle(LineStyle.SINGLE);

 table = builder.startTable();
 builder.insertCell();
 builder.write("Aligned according to left indent");
 builder.endTable();
 table.setPreferredWidth(PreferredWidth.fromPoints(300.0));

 table.setStyle(tableStyle);

 doc.save(getArtifactsDir() + "Table.SetTableAlignment.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | القيمة التي تمثل المسافة البادئة اليسرى للجدول. |

### setLeftPadding(double value) {#setLeftPadding-double}
```
public void setLeftPadding(double value)
```


يضبط مقدار المسافة (بالنقاط) لإضافتها إلى يسار محتويات خلايا الجدول.

 **Examples:** 

يظهر كيفية إنشاء إعدادات نمط مخصصة للجدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | كمية المسافة (بالنقاط) لإضافتها إلى يسار محتويات خلايا الجدول. |

### setLinkedStyleName(String value) {#setLinkedStyleName-java.lang.String}
```
public void setLinkedStyleName(String value)
```


يحصل/يضبط اسم الـ [Style](../../com.aspose.words/style/) المرتبط بهذا. يُعيد سلسلة فارغة إذا لم يتم ربط أي أنماط.

 **Remarks:** 

يسمح فقط بربط نمط الفقرة بنمط الحرف والعكس بالعكس.

ضبط LinkedStyleName للنمط الحالي يؤدي تلقائيًا إلى ضبط LinkedStyleName للنمط المرتبط.

تعيين السلسلة الفارغة يعادل إلغاء ربط النمط المرتبط مسبقًا.

 **Examples:** 

يوضح كيفية استخدام الأسماء المستعارة للأنماط.

```

 Document doc = new Document(getMyDir() + "Style with alias.docx");

 // This document contains a style named "MyStyle,MyStyle Alias 1,MyStyle Alias 2".
 // If a style's name has multiple values separated by commas, each clause is a separate alias.
 Style style = doc.getStyles().get("MyStyle");
 Assert.assertEquals(new String[]{"MyStyle Alias 1", "MyStyle Alias 2"}, style.getAliases());
 Assert.assertEquals("Title", style.getBaseStyleName());
 Assert.assertEquals("MyStyle Char", style.getLinkedStyleName());

 // We can reference a style using its alias, as well as its name.
 Assert.assertEquals(doc.getStyles().get("MyStyle Alias 1"), doc.getStyles().get("MyStyle Alias 2"));

 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.moveToDocumentEnd();
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 1"));
 builder.writeln("Hello world!");
 builder.getParagraphFormat().setStyle(doc.getStyles().get("MyStyle Alias 2"));
 builder.write("Hello again!");

 Assert.assertEquals(doc.getFirstSection().getBody().getParagraphs().get(0).getParagraphFormat().getStyle(),
         doc.getFirstSection().getBody().getParagraphs().get(1).getParagraphFormat().getStyle());
 
```

يوضح كيفية ربط الأنماط ببعضها البعض.

```

 Document doc = new Document();

 Style styleHeading1 = doc.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1);

 Style styleHeading1Char = doc.getStyles().add(StyleType.CHARACTER, "Heading 1 Char");
 styleHeading1Char.getFont().setName("Verdana");
 styleHeading1Char.getFont().setBold(true);
 styleHeading1Char.getFont().getBorder().setLineStyle(LineStyle.DOT);
 styleHeading1Char.getFont().getBorder().setLineWidth(15.0);

 styleHeading1.setLinkedStyleName("Heading 1 Char");

 Assert.assertEquals("Heading 1 Char", styleHeading1.getLinkedStyleName());
 Assert.assertEquals("Heading 1", styleHeading1Char.getLinkedStyleName());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

### setLocked(boolean value) {#setLocked-boolean}
```
public void setLocked(boolean value)
```


يحدد ما إذا كان هذا النمط مقفلاً.

 **Examples:** 

يوضح كيفية قفل النمط.

```

 Document doc = new Document();

 Style styleHeading1 = doc.getStyles().getByStyleIdentifier(StyleIdentifier.HEADING_1);
 if (!styleHeading1.getLocked())
     styleHeading1.setLocked(true);

 doc.save(getArtifactsDir() + "Styles.LockStyle.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


يضبط اسم النمط.

 **Remarks:** 

لا يمكن أن تكون سلسلة فارغة.

إذا كان هناك نمط بالفعل بهذا الاسم في المجموعة، فسيتم استبداله بهذا النمط. جميع العقد المتأثرة ستشير إلى النمط الجديد.

 **Examples:** 

يوضح كيفية الوصول إلى مجموعة أنماط المستند.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | اسم النمط. |

### setNextParagraphStyleName(String value) {#setNextParagraphStyleName-java.lang.String}
```
public void setNextParagraphStyleName(String value)
```


يحصل/يضبط اسم النمط الذي سيُطبق تلقائياً على فقرة جديدة تُدرج بعد فقرة مُنسقة بالنمط المحدد.

 **Remarks:** 

هذه الخاصية لا يستخدمها Aspose.Words. سيتم تطبيق نمط الفقرة التالي تلقائيًا فقط عندما تقوم بتحرير المستند في MS Word.

 **Examples:** 

يوضح كيفية الوصول إلى مجموعة أنماط المستند.

```

 Document doc = new Document();

 Assert.assertEquals(4, doc.getStyles().getCount());

 // Enumerate and list all the styles that a document created using Aspose.Words contains by default.
 Iterator
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | القيمة المقابلة من نوع java.lang.String. |

### setParaAttr(int key, Object value) {#setParaAttr-int-java.lang.Object}
```
public void setParaAttr(int key, Object value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |
| قيمة | java.lang.Object |  |

### setPriority(int value) {#setPriority-int}
```
public void setPriority(int value)
```


يحصل/يضبط القيمة الصحيحة التي تمثل أولوية فرز الأنماط في لوحة مهام الأنماط.

 **Examples:** 

يوضح كيفية إعطاء أولوية وإخفاء النمط.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | القيمة  int  المقابلة. |

### setRightPadding(double value) {#setRightPadding-double}
```
public void setRightPadding(double value)
```


يضبط مقدار المسافة (بالنقاط) لإضافتها إلى يمين محتويات خلايا الجدول.

 **Examples:** 

يظهر كيفية إنشاء إعدادات نمط مخصصة للجدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | كمية المسافة (بالنقاط) لإضافتها إلى يمين محتويات خلايا الجدول. |

### setRowAttr(int key, Object value) {#setRowAttr-int-java.lang.Object}
```
public void setRowAttr(int key, Object value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |
| قيمة | java.lang.Object |  |

### setRowStripe(int value) {#setRowStripe-int}
```
public void setRowStripe(int value)
```


يضبط عدد الصفوف التي يجب تضمينها في التظليل عندما يحدد النمط تظليل الصفوف الفردية/الزوجية.

 **Examples:** 

يظهر كيفية إنشاء أنماط جدول شرطية تتناوب بين الصفوف.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // We can configure a conditional style of a table to apply a different color to the row/column,
 // based on whether the row/column is even or odd, creating an alternating color pattern.
 // We can also apply a number n to the row/column banding,
 // meaning that the color alternates after every n rows/columns instead of one.
 // Create a table where single columns and rows will band the columns will banded in threes.
 Table table = builder.startTable();

 for (int i = 0; i < 15; i++) {
     for (int j = 0; j < 4; j++) {
         builder.insertCell();
         builder.writeln(MessageFormat.format("{0} column.", (j % 2 == 0 ? "Even" : "Odd")));
         builder.write(MessageFormat.format("Row banding {0}.", (i % 3 == 0 ? "start" : "continuation")));
     }
     builder.endRow();
 }

 builder.endTable();

 // Apply a line style to all the borders of the table.
 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOUBLE);

 // Set the two colors, which will alternate over every 3 rows.
 tableStyle.setRowStripe(3);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.ODD_ROW_BANDING).getShading().setBackgroundPatternColor(Color.BLUE);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.EVEN_ROW_BANDING).getShading().setBackgroundPatternColor(Color.CYAN);

 // Set a color to apply to every even column, which will override any custom row coloring.
 tableStyle.setColumnStripe(1);
 tableStyle.getConditionalStyles().getByConditionalStyleType(ConditionalStyleType.EVEN_COLUMN_BANDING).getShading().setBackgroundPatternColor(Color.RED);

 table.setStyle(tableStyle);

 // The "StyleOptions" property enables row banding by default.
 Assert.assertEquals(TableStyleOptions.FIRST_ROW | TableStyleOptions.FIRST_COLUMN | TableStyleOptions.ROW_BANDS,
         table.getStyleOptions());

 // Use the "StyleOptions" property also to enable column banding.
 table.setStyleOptions(table.getStyleOptions() | TableStyleOptions.COLUMN_BANDS);

 doc.save(getArtifactsDir() + "Table.AlternatingRowStyles.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | عدد الصفوف التي يجب تضمينها في التظليل عندما يحدد النمط تظليل الصفوف الفردية/الزوجية. |

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object}
```
public void setRunAttr(int key, Object value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | int |  |
| قيمة | java.lang.Object |  |

### setSemiHidden(boolean value) {#setSemiHidden-boolean}
```
public void setSemiHidden(boolean value)
```


يحصل/يضبط ما إذا كان النمط مخفياً في معرض الأنماط ومن لوحة مهام الأنماط.

 **Examples:** 

يوضح كيفية إعطاء أولوية وإخفاء النمط.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setTopPadding(double value) {#setTopPadding-double}
```
public void setTopPadding(double value)
```


يضبط مقدار المسافة (بالنقاط) لإضافتها فوق محتويات خلايا الجدول.

 **Examples:** 

يظهر كيفية إنشاء إعدادات نمط مخصصة للجدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | كمية المسافة (بالنقاط) لإضافتها فوق محتويات خلايا الجدول. |

### setUnhideWhenUsed(boolean value) {#setUnhideWhenUsed-boolean}
```
public void setUnhideWhenUsed(boolean value)
```


يحصل/يضبط ما إذا كان النمط المستخدم في المستند الحالي يُظهر من معرض الأنماط ومن لوحة مهام الأنماط. True عندما يجب إظهار النمط المستخدم في معرض الأنماط.

 **Examples:** 

يوضح كيفية إعطاء أولوية وإخفاء النمط.

```

 Document doc = new Document();
 Style styleTitle = doc.getStyles().getByStyleIdentifier(StyleIdentifier.SUBTITLE);

 if (styleTitle.getPriority() == 9)
     styleTitle.setPriority(10);

 if (!styleTitle.getUnhideWhenUsed())
     styleTitle.setUnhideWhenUsed(true);

 if (styleTitle.getSemiHidden())
     styleTitle.setSemiHidden(true);

 doc.save(getArtifactsDir() + "Styles.StylePriority.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setVerticalAlignment(int value) {#setVerticalAlignment-int}
```
public void setVerticalAlignment(int value)
```


يحدد المحاذاة العمودية للخلايا.

 **Remarks:** 

القيمة الافتراضية هي [CellVerticalAlignment.TOP](../../com.aspose.words/cellverticalalignment/#TOP).

 **Examples:** 

يظهر كيفية إنشاء إعدادات نمط مخصصة للجدول.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Table table = builder.startTable();
 builder.insertCell();
 builder.write("Name");
 builder.insertCell();
 builder.write("\u0645\u0631\u062d\u0628\u064b\u0627");
 builder.endRow();
 builder.insertCell();
 builder.insertCell();
 builder.endTable();

 TableStyle tableStyle = (TableStyle) doc.getStyles().add(StyleType.TABLE, "MyTableStyle1");
 tableStyle.setAllowBreakAcrossPages(true);
 tableStyle.setCellSpacing(5.0);
 tableStyle.setBottomPadding(20.0);
 tableStyle.setLeftPadding(5.0);
 tableStyle.setRightPadding(10.0);
 tableStyle.setTopPadding(20.0);
 tableStyle.getShading().setBackgroundPatternColor(Color.WHITE);
 tableStyle.getBorders().setColor(Color.BLACK);
 tableStyle.getBorders().setLineStyle(LineStyle.DOT_DASH);
 tableStyle.setVerticalAlignment(CellVerticalAlignment.CENTER);

 table.setStyle(tableStyle);

 table.setBidi(true);

 // Setting the style properties of a table may affect the properties of the table itself.
 Assert.assertTrue(table.getBidi());
 Assert.assertEquals(5.0d, table.getCellSpacing());
 Assert.assertEquals("MyTableStyle1", table.getStyleName());

 doc.save(getArtifactsDir() + "Table.TableStyleCreation.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | القيمة int المقابلة. يجب أن تكون القيمة واحدة من ثوابت [CellVerticalAlignment](../../com.aspose.words/cellverticalalignment/). |

