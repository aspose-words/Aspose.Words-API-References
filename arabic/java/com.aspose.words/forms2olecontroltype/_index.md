---
title: "Forms2OleControlType"
linktitle: "Forms2OleControlType"
second_title: "Aspose.Words لـ Java"
description: "يسرد أنواع عناصر تحكم Forms 2.0 في Java."
type: docs
weight: 351
url: /ar/java/com.aspose.words/forms2olecontroltype/
---

**Inheritance:**
java.lang.Object
```
public class Forms2OleControlType
```

يسرد أنواع عناصر تحكم Forms 2.0.

 **Examples:** 

يظهر كيفية تغيير حالة عنصر التحكم CheckBox.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 CheckBoxControl checkBoxControl = (CheckBoxControl)shape.getOleFormat().getOleControl();
 checkBoxControl.setChecked(true);

 Assert.assertEquals(true, checkBoxControl.getChecked());
 Assert.assertEquals(Forms2OleControlType.CHECK_BOX, checkBoxControl.getType());
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [CHECK_BOX](#CHECK-BOX) | عنصر تحكم يتيح للمستخدم اختيار أو إلغاء اختيار خيار. |
| [COMBO_BOX](#COMBO-BOX) | عنصر تحكم يتيح للمستخدم اختيار عنصر من قائمة. |
| [COMMAND_BUTTON](#COMMAND-BUTTON) | زر يُطلق إجراءً عند النقر. |
| [FORM](#FORM) | حاوية لعناصر التحكم الأخرى. |
| [FRAME](#FRAME) | عنصر تحكم يجمع عناصر التحكم الأخرى. |
| [IMAGE](#IMAGE) | عنصر تحكم يعرض صورة. |
| [LABEL](#LABEL) | عنصر تحكم يعرض نصًا. |
| [LIST_BOX](#LIST-BOX) | عنصر تحكم يعرض قائمة من العناصر. |
| [MULTI_PAGE](#MULTI-PAGE) | عنصر تحكم يعرض عدة صفحات من المحتوى. |
| [OPTION_BUTTON](#OPTION-BUTTON) | عنصر تحكم زر راديو. |
| [SCROLL_BAR](#SCROLL-BAR) | عنصر تحكم يتيح للمستخدم التمرير عبر المحتوى. |
| [SPIN_BUTTON](#SPIN-BUTTON) | عنصر تحكم يتيح للمستخدم زيادة أو تقليل قيمة. |
| [TAB_STRIP](#TAB-STRIP) | عنصر تحكم يتيح للمستخدم التنقل بين عدة صفحات من المحتوى. |
| [TEXTBOX](#TEXTBOX) | عنصر تحكم يتيح للمستخدم إدخال نص. |
| [TOGGLE_BUTTON](#TOGGLE-BUTTON) | عنصر تحكم يتيح للمستخدم التبديل بين حالتين. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String forms2OleControlTypeName)](#fromName-java.lang.String) |  |
| [getName(int forms2OleControlType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int forms2OleControlType)](#toString-int) |  |
### CHECK_BOX {#CHECK-BOX}
```
public static int CHECK_BOX
```


عنصر تحكم يتيح للمستخدم اختيار أو إلغاء اختيار خيار.

### COMBO_BOX {#COMBO-BOX}
```
public static int COMBO_BOX
```


عنصر تحكم يتيح للمستخدم اختيار عنصر من قائمة.

### COMMAND_BUTTON {#COMMAND-BUTTON}
```
public static int COMMAND_BUTTON
```


زر يُطلق إجراءً عند النقر.

### FORM {#FORM}
```
public static int FORM
```


حاوية لعناصر التحكم الأخرى.

### FRAME {#FRAME}
```
public static int FRAME
```


عنصر تحكم يجمع عناصر التحكم الأخرى.

### IMAGE {#IMAGE}
```
public static int IMAGE
```


عنصر تحكم يعرض صورة.

### LABEL {#LABEL}
```
public static int LABEL
```


عنصر تحكم يعرض نصًا.

### LIST_BOX {#LIST-BOX}
```
public static int LIST_BOX
```


عنصر تحكم يعرض قائمة من العناصر.

### MULTI_PAGE {#MULTI-PAGE}
```
public static int MULTI_PAGE
```


عنصر تحكم يعرض عدة صفحات من المحتوى.

### OPTION_BUTTON {#OPTION-BUTTON}
```
public static int OPTION_BUTTON
```


عنصر تحكم زر راديو.

### SCROLL_BAR {#SCROLL-BAR}
```
public static int SCROLL_BAR
```


عنصر تحكم يتيح للمستخدم التمرير عبر المحتوى.

### SPIN_BUTTON {#SPIN-BUTTON}
```
public static int SPIN_BUTTON
```


عنصر تحكم يتيح للمستخدم زيادة أو تقليل قيمة.

### TAB_STRIP {#TAB-STRIP}
```
public static int TAB_STRIP
```


عنصر تحكم يتيح للمستخدم التنقل بين عدة صفحات من المحتوى.

### TEXTBOX {#TEXTBOX}
```
public static int TEXTBOX
```


عنصر تحكم يتيح للمستخدم إدخال نص.

### TOGGLE_BUTTON {#TOGGLE-BUTTON}
```
public static int TOGGLE_BUTTON
```


عنصر تحكم يتيح للمستخدم التبديل بين حالتين.

### length {#length}
```
public static int length
```


### fromName(String forms2OleControlTypeName) {#fromName-java.lang.String}
```
public static int fromName(String forms2OleControlTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| forms2OleControlTypeName | java.lang.String |  |

**Returns:**
int
### getName(int forms2OleControlType) {#getName-int}
```
public static String getName(int forms2OleControlType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| forms2OleControlType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int forms2OleControlType) {#toString-int}
```
public static String toString(int forms2OleControlType)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| forms2OleControlType | int |  |

**Returns:**
java.lang.String
