---
title: "Forms2OleControl"
linktitle: "Forms2OleControl"
second_title: "Aspose.Words لـ Java"
description: "يمثل عنصر التحكم OLE الخاص بـ Microsoft Forms 2.0 في Java."
type: docs
weight: 349
url: /ar/java/com.aspose.words/forms2olecontrol/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.OleControl](../../com.aspose.words/olecontrol/)
```
public abstract class Forms2OleControl extends OleControl
```

يمثل عنصر تحكم OLE في Microsoft Forms 2.0.

لمزيد من المعلومات، زر مقالة الوثائق [ Working with Ole Objects ][Working with Ole Objects].

 **Examples:** 

يوضح كيفية التحقق من خصائص عنصر ActiveX.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 OleControl oleControl = shape.getOleFormat().getOleControl();

 Assert.assertEquals(oleControl.getName(), "CheckBox1");

 if (oleControl.isForms2OleControl()) {
     Forms2OleControl checkBox = (Forms2OleControl) oleControl;
     Assert.assertEquals(checkBox.getCaption(), "First");
     Assert.assertEquals(checkBox.getValue(), "0");
     Assert.assertEquals(checkBox.getEnabled(), true);
     Assert.assertEquals(checkBox.getType(), Forms2OleControlType.CHECK_BOX);
     Assert.assertEquals(checkBox.getChildNodes(), null);
 }
 
```


[Working with Ole Objects]: https://docs.aspose.com/words/java/working-with-ole-objects/
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [Forms2OleControl()](#Forms2OleControl) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getBackColor()](#getBackColor) | يحصل على لون الخلفية للعنصر. |
| [getCaption()](#getCaption) | يحصل على خاصية Caption للعنصر. |
| [getChildNodes()](#getChildNodes) | يحصل على مجموعة من عناصر التحكم الفرعية الفورية. |
| [getClsidInternal()](#getClsidInternal) |  |
| [getEnabled()](#getEnabled) | يرجع  true  إذا كان العنصر في حالة تمكين. |
| [getExtensionForUser(String progId)](#getExtensionForUser-java.lang.String) |  |
| [getFileNameForUser()](#getFileNameForUser) |  |
| [getForeColor()](#getForeColor) | يحصل على لون المقدمة للعنصر. |
| [getGroupName()](#getGroupName) | يحصل على سلسلة تحدد مجموعة من عناصر التحكم المتعارضة. |
| [getHeight()](#getHeight) | يحصل على ارتفاع العنصر بالنقاط. |
| [getId()](#getId) |  |
| [getName()](#getName) | يحصل على اسم عنصر التحكم ActiveX. |
| [getType()](#getType) | يحصل على نوع عنصر التحكم Forms 2.0. |
| [getValue()](#getValue) | يحصل على خاصية Value الأساسية التي غالبًا ما تمثل حالة العنصر. |
| [getWidth()](#getWidth) | يحصل على عرض العنصر بالنقاط. |
| [isEmpty()](#isEmpty) |  |
| [isForms2OleControl()](#isForms2OleControl) | يعيد  true  إذا كان التحكم من نوع [Forms2OleControl](../../com.aspose.words/forms2olecontrol/). |
| [isForms2OleControlInternal()](#isForms2OleControlInternal) |  |
| [setBackColor(Color value)](#setBackColor-java.awt.Color) | يضبط لون الخلفية للعنصر. |
| [setCaption(String value)](#setCaption-java.lang.String) | يضبط خاصية Caption للعنصر. |
| [setForeColor(Color value)](#setForeColor-java.awt.Color) | يضبط لون المقدمة للعنصر. |
| [setGroupName(String value)](#setGroupName-java.lang.String) | يضبط سلسلة تحدد مجموعة من العناصر المتعارضة. |
| [setHeight(double value)](#setHeight-double) | يضبط ارتفاع العنصر بالنقاط. |
| [setId(int value)](#setId-int) |  |
| [setName(String value)](#setName-java.lang.String) | يضبط اسم عنصر ActiveX. |
| [setWidth(double value)](#setWidth-double) | يضبط عرض العنصر بالنقاط. |
### Forms2OleControl() {#Forms2OleControl}
```
public Forms2OleControl()
```


### getBackColor() {#getBackColor}
```
public Color getBackColor()
```


يحصل على لون الخلفية للعنصر. القيمة الافتراضية تعتمد على نوع العنصر.

 **Examples:** 

يوضح كيفية ضبط الخصائص لعنصر ActiveX.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Forms2OleControl oleControl = (Forms2OleControl)shape.getOleFormat().getOleControl();
 oleControl.setForeColor(new Color((0x17), (0xE1), (0x35)));
 oleControl.setBackColor(new Color((0x33), (0x97), (0xF4)));
 oleControl.setHeight(100.54);
 oleControl.setWidth(201.06);
 
```

**Returns:**
java.awt.Color - لون خلفية العنصر.
### getCaption() {#getCaption}
```
public String getCaption()
```


يحصل على خاصية Caption للعنصر. القيمة الافتراضية هي سلسلة فارغة.

 **Examples:** 

يوضح كيفية التحقق من خصائص عنصر ActiveX.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 OleControl oleControl = shape.getOleFormat().getOleControl();

 Assert.assertEquals(oleControl.getName(), "CheckBox1");

 if (oleControl.isForms2OleControl()) {
     Forms2OleControl checkBox = (Forms2OleControl) oleControl;
     Assert.assertEquals(checkBox.getCaption(), "First");
     Assert.assertEquals(checkBox.getValue(), "0");
     Assert.assertEquals(checkBox.getEnabled(), true);
     Assert.assertEquals(checkBox.getType(), Forms2OleControlType.CHECK_BOX);
     Assert.assertEquals(checkBox.getChildNodes(), null);
 }
 
```

يوضح كيفية ضبط العنوان لعنصر ActiveX.

```

 DocumentBuilder builder = new DocumentBuilder();

 CommandButtonControl button1 = new CommandButtonControl(); { button1.setCaption("Button caption"); }
 Shape shape = builder.insertForms2OleControl(button1);
 Assert.assertEquals("Button caption", button1.getCaption());
 
```

**Returns:**
java.lang.String - خاصية Caption للعنصر.
### getChildNodes() {#getChildNodes}
```
public Forms2OleControlCollection getChildNodes()
```


يحصل على مجموعة من عناصر التحكم الفرعية الفورية.

 **Remarks:** 

يعيد  null  إذا لم يكن لهذا العنصر إمكانية احتواء عناصر فرعية.

 **Examples:** 

يوضح كيفية التحقق من خصائص عنصر ActiveX.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 OleControl oleControl = shape.getOleFormat().getOleControl();

 Assert.assertEquals(oleControl.getName(), "CheckBox1");

 if (oleControl.isForms2OleControl()) {
     Forms2OleControl checkBox = (Forms2OleControl) oleControl;
     Assert.assertEquals(checkBox.getCaption(), "First");
     Assert.assertEquals(checkBox.getValue(), "0");
     Assert.assertEquals(checkBox.getEnabled(), true);
     Assert.assertEquals(checkBox.getType(), Forms2OleControlType.CHECK_BOX);
     Assert.assertEquals(checkBox.getChildNodes(), null);
 }
 
```

**Returns:**
[Forms2OleControlCollection](../../com.aspose.words/forms2olecontrolcollection/) - Collection of immediate child controls.
### getClsidInternal() {#getClsidInternal}
```
public String getClsidInternal()
```




**Returns:**
java.lang.String
### getEnabled() {#getEnabled}
```
public boolean getEnabled()
```


يرجع  true  إذا كان العنصر في حالة تمكين.

 **Examples:** 

يوضح كيفية التحقق من خصائص عنصر ActiveX.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 OleControl oleControl = shape.getOleFormat().getOleControl();

 Assert.assertEquals(oleControl.getName(), "CheckBox1");

 if (oleControl.isForms2OleControl()) {
     Forms2OleControl checkBox = (Forms2OleControl) oleControl;
     Assert.assertEquals(checkBox.getCaption(), "First");
     Assert.assertEquals(checkBox.getValue(), "0");
     Assert.assertEquals(checkBox.getEnabled(), true);
     Assert.assertEquals(checkBox.getType(), Forms2OleControlType.CHECK_BOX);
     Assert.assertEquals(checkBox.getChildNodes(), null);
 }
 
```

**Returns:**
boolean -  true  إذا كان العنصر في حالة مفعلة.
### getExtensionForUser(String progId) {#getExtensionForUser-java.lang.String}
```
public String getExtensionForUser(String progId)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| progId | java.lang.String |  |

**Returns:**
java.lang.String
### getFileNameForUser() {#getFileNameForUser}
```
public String getFileNameForUser()
```




**Returns:**
java.lang.String
### getForeColor() {#getForeColor}
```
public Color getForeColor()
```


يحصل على لون المقدمة للعنصر. القيمة الافتراضية تعتمد على نوع العنصر.

 **Examples:** 

يوضح كيفية ضبط الخصائص لعنصر ActiveX.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Forms2OleControl oleControl = (Forms2OleControl)shape.getOleFormat().getOleControl();
 oleControl.setForeColor(new Color((0x17), (0xE1), (0x35)));
 oleControl.setBackColor(new Color((0x33), (0x97), (0xF4)));
 oleControl.setHeight(100.54);
 oleControl.setWidth(201.06);
 
```

**Returns:**
java.awt.Color - لون مقدمة العنصر.
### getGroupName() {#getGroupName}
```
public String getGroupName()
```


يحصل على سلسلة تحدد مجموعة من العناصر المتعارضة. القيمة الافتراضية هي سلسلة فارغة.

 **Examples:** 

يوضح كيفية التحقق من خصائص عنصر ActiveX.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 OleControl oleControl = shape.getOleFormat().getOleControl();

 Assert.assertEquals(oleControl.getName(), "CheckBox1");

 if (oleControl.isForms2OleControl()) {
     Forms2OleControl checkBox = (Forms2OleControl) oleControl;
     Assert.assertEquals(checkBox.getCaption(), "First");
     Assert.assertEquals(checkBox.getValue(), "0");
     Assert.assertEquals(checkBox.getEnabled(), true);
     Assert.assertEquals(checkBox.getType(), Forms2OleControlType.CHECK_BOX);
     Assert.assertEquals(checkBox.getChildNodes(), null);
 }
 
```

**Returns:**
java.lang.String - سلسلة تحدد مجموعة من العناصر المتعارضة.
### getHeight() {#getHeight}
```
public double getHeight()
```


يحصل على ارتفاع العنصر بالنقاط.

 **Examples:** 

يوضح كيفية ضبط الخصائص لعنصر ActiveX.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Forms2OleControl oleControl = (Forms2OleControl)shape.getOleFormat().getOleControl();
 oleControl.setForeColor(new Color((0x17), (0xE1), (0x35)));
 oleControl.setBackColor(new Color((0x33), (0x97), (0xF4)));
 oleControl.setHeight(100.54);
 oleControl.setWidth(201.06);
 
```

**Returns:**
double - ارتفاع العنصر بالنقاط.
### getId() {#getId}
```
public int getId()
```




**Returns:**
int
### getName() {#getName}
```
public String getName()
```


يحصل على اسم عنصر التحكم ActiveX.

 **Examples:** 

يوضح كيفية التحقق من خصائص عنصر ActiveX.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 OleControl oleControl = shape.getOleFormat().getOleControl();

 Assert.assertEquals(oleControl.getName(), "CheckBox1");

 if (oleControl.isForms2OleControl()) {
     Forms2OleControl checkBox = (Forms2OleControl) oleControl;
     Assert.assertEquals(checkBox.getCaption(), "First");
     Assert.assertEquals(checkBox.getValue(), "0");
     Assert.assertEquals(checkBox.getEnabled(), true);
     Assert.assertEquals(checkBox.getType(), Forms2OleControlType.CHECK_BOX);
     Assert.assertEquals(checkBox.getChildNodes(), null);
 }
 
```

**Returns:**
java.lang.String - اسم عنصر ActiveX.
### getType() {#getType}
```
public abstract int getType()
```


يحصل على نوع عنصر التحكم Forms 2.0.

 **Examples:** 

يوضح كيفية التحقق من خصائص عنصر ActiveX.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 OleControl oleControl = shape.getOleFormat().getOleControl();

 Assert.assertEquals(oleControl.getName(), "CheckBox1");

 if (oleControl.isForms2OleControl()) {
     Forms2OleControl checkBox = (Forms2OleControl) oleControl;
     Assert.assertEquals(checkBox.getCaption(), "First");
     Assert.assertEquals(checkBox.getValue(), "0");
     Assert.assertEquals(checkBox.getEnabled(), true);
     Assert.assertEquals(checkBox.getType(), Forms2OleControlType.CHECK_BOX);
     Assert.assertEquals(checkBox.getChildNodes(), null);
 }
 
```

**Returns:**
int - نوع عنصر Forms 2.0. القيمة المرجعة هي واحدة من ثوابت [Forms2OleControlType](../../com.aspose.words/forms2olecontroltype/) constants.
### getValue() {#getValue}
```
public String getValue()
```


يحصل على الخاصية Value الأساسية التي غالبًا ما تمثل حالة التحكم. على سبيل المثال، زر الخيار المحدد يحتوي على القيمة '1' بينما غير المحدد يحتوي على '0'. القيمة الافتراضية هي سلسلة فارغة.

 **Examples:** 

يوضح كيفية التحقق من خصائص عنصر ActiveX.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 OleControl oleControl = shape.getOleFormat().getOleControl();

 Assert.assertEquals(oleControl.getName(), "CheckBox1");

 if (oleControl.isForms2OleControl()) {
     Forms2OleControl checkBox = (Forms2OleControl) oleControl;
     Assert.assertEquals(checkBox.getCaption(), "First");
     Assert.assertEquals(checkBox.getValue(), "0");
     Assert.assertEquals(checkBox.getEnabled(), true);
     Assert.assertEquals(checkBox.getType(), Forms2OleControlType.CHECK_BOX);
     Assert.assertEquals(checkBox.getChildNodes(), null);
 }
 
```

**Returns:**
java.lang.String - الخاصية Value الأساسية التي غالبًا ما تمثل حالة التحكم.
### getWidth() {#getWidth}
```
public double getWidth()
```


يحصل على عرض العنصر بالنقاط.

 **Examples:** 

يوضح كيفية ضبط الخصائص لعنصر ActiveX.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Forms2OleControl oleControl = (Forms2OleControl)shape.getOleFormat().getOleControl();
 oleControl.setForeColor(new Color((0x17), (0xE1), (0x35)));
 oleControl.setBackColor(new Color((0x33), (0x97), (0xF4)));
 oleControl.setHeight(100.54);
 oleControl.setWidth(201.06);
 
```

**Returns:**
double - عرض التحكم بالنقاط.
### isEmpty() {#isEmpty}
```
public boolean isEmpty()
```




**Returns:**
boolean
### isForms2OleControl() {#isForms2OleControl}
```
public boolean isForms2OleControl()
```


يعيد  true  إذا كان التحكم من نوع [Forms2OleControl](../../com.aspose.words/forms2olecontrol/).

 **Examples:** 

يوضح كيفية التحقق من خصائص عنصر ActiveX.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 OleControl oleControl = shape.getOleFormat().getOleControl();

 Assert.assertEquals(oleControl.getName(), "CheckBox1");

 if (oleControl.isForms2OleControl()) {
     Forms2OleControl checkBox = (Forms2OleControl) oleControl;
     Assert.assertEquals(checkBox.getCaption(), "First");
     Assert.assertEquals(checkBox.getValue(), "0");
     Assert.assertEquals(checkBox.getEnabled(), true);
     Assert.assertEquals(checkBox.getType(), Forms2OleControlType.CHECK_BOX);
     Assert.assertEquals(checkBox.getChildNodes(), null);
 }
 
```

**Returns:**
boolean -  true  إذا كان التحكم هو [Forms2OleControl](../../com.aspose.words/forms2olecontrol/).
### isForms2OleControlInternal() {#isForms2OleControlInternal}
```
public boolean isForms2OleControlInternal()
```




**Returns:**
boolean
### setBackColor(Color value) {#setBackColor-java.awt.Color}
```
public void setBackColor(Color value)
```


يضبط لون الخلفية للتحكم. القيمة الافتراضية تعتمد على نوع التحكم.

 **Examples:** 

يوضح كيفية ضبط الخصائص لعنصر ActiveX.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Forms2OleControl oleControl = (Forms2OleControl)shape.getOleFormat().getOleControl();
 oleControl.setForeColor(new Color((0x17), (0xE1), (0x35)));
 oleControl.setBackColor(new Color((0x33), (0x97), (0xF4)));
 oleControl.setHeight(100.54);
 oleControl.setWidth(201.06);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color | لون خلفية التحكم. |

### setCaption(String value) {#setCaption-java.lang.String}
```
public void setCaption(String value)
```


يضبط خاصية Caption للتحكم. القيمة الافتراضية هي سلسلة فارغة.

 **Examples:** 

يوضح كيفية التحقق من خصائص عنصر ActiveX.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 OleControl oleControl = shape.getOleFormat().getOleControl();

 Assert.assertEquals(oleControl.getName(), "CheckBox1");

 if (oleControl.isForms2OleControl()) {
     Forms2OleControl checkBox = (Forms2OleControl) oleControl;
     Assert.assertEquals(checkBox.getCaption(), "First");
     Assert.assertEquals(checkBox.getValue(), "0");
     Assert.assertEquals(checkBox.getEnabled(), true);
     Assert.assertEquals(checkBox.getType(), Forms2OleControlType.CHECK_BOX);
     Assert.assertEquals(checkBox.getChildNodes(), null);
 }
 
```

يوضح كيفية ضبط العنوان لعنصر ActiveX.

```

 DocumentBuilder builder = new DocumentBuilder();

 CommandButtonControl button1 = new CommandButtonControl(); { button1.setCaption("Button caption"); }
 Shape shape = builder.insertForms2OleControl(button1);
 Assert.assertEquals("Button caption", button1.getCaption());
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | خاصية Caption للتحكم. |

### setForeColor(Color value) {#setForeColor-java.awt.Color}
```
public void setForeColor(Color value)
```


يضبط لون المقدمة للتحكم. القيمة الافتراضية تعتمد على نوع التحكم.

 **Examples:** 

يوضح كيفية ضبط الخصائص لعنصر ActiveX.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Forms2OleControl oleControl = (Forms2OleControl)shape.getOleFormat().getOleControl();
 oleControl.setForeColor(new Color((0x17), (0xE1), (0x35)));
 oleControl.setBackColor(new Color((0x33), (0x97), (0xF4)));
 oleControl.setHeight(100.54);
 oleControl.setWidth(201.06);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.awt.Color | لون المقدمة للتحكم. |

### setGroupName(String value) {#setGroupName-java.lang.String}
```
public void setGroupName(String value)
```


يضبط سلسلة تحدد مجموعة من عناصر التحكم المتعارضة. القيمة الافتراضية هي سلسلة فارغة.

 **Examples:** 

يوضح كيفية التحقق من خصائص عنصر ActiveX.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 OleControl oleControl = shape.getOleFormat().getOleControl();

 Assert.assertEquals(oleControl.getName(), "CheckBox1");

 if (oleControl.isForms2OleControl()) {
     Forms2OleControl checkBox = (Forms2OleControl) oleControl;
     Assert.assertEquals(checkBox.getCaption(), "First");
     Assert.assertEquals(checkBox.getValue(), "0");
     Assert.assertEquals(checkBox.getEnabled(), true);
     Assert.assertEquals(checkBox.getType(), Forms2OleControlType.CHECK_BOX);
     Assert.assertEquals(checkBox.getChildNodes(), null);
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | سلسلة تحدد مجموعة من عناصر التحكم المتعارضة. |

### setHeight(double value) {#setHeight-double}
```
public void setHeight(double value)
```


يضبط ارتفاع العنصر بالنقاط.

 **Examples:** 

يوضح كيفية ضبط الخصائص لعنصر ActiveX.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Forms2OleControl oleControl = (Forms2OleControl)shape.getOleFormat().getOleControl();
 oleControl.setForeColor(new Color((0x17), (0xE1), (0x35)));
 oleControl.setBackColor(new Color((0x33), (0x97), (0xF4)));
 oleControl.setHeight(100.54);
 oleControl.setWidth(201.06);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | ارتفاع التحكم بالنقاط. |

### setId(int value) {#setId-int}
```
public void setId(int value)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int |  |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


يضبط اسم عنصر ActiveX.

 **Examples:** 

يوضح كيفية التحقق من خصائص عنصر ActiveX.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape) doc.getChild(NodeType.SHAPE, 0, true);
 OleControl oleControl = shape.getOleFormat().getOleControl();

 Assert.assertEquals(oleControl.getName(), "CheckBox1");

 if (oleControl.isForms2OleControl()) {
     Forms2OleControl checkBox = (Forms2OleControl) oleControl;
     Assert.assertEquals(checkBox.getCaption(), "First");
     Assert.assertEquals(checkBox.getValue(), "0");
     Assert.assertEquals(checkBox.getEnabled(), true);
     Assert.assertEquals(checkBox.getType(), Forms2OleControlType.CHECK_BOX);
     Assert.assertEquals(checkBox.getChildNodes(), null);
 }
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.String | اسم عنصر التحكم ActiveX. |

### setWidth(double value) {#setWidth-double}
```
public void setWidth(double value)
```


يضبط عرض العنصر بالنقاط.

 **Examples:** 

يوضح كيفية ضبط الخصائص لعنصر ActiveX.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Forms2OleControl oleControl = (Forms2OleControl)shape.getOleFormat().getOleControl();
 oleControl.setForeColor(new Color((0x17), (0xE1), (0x35)));
 oleControl.setBackColor(new Color((0x33), (0x97), (0xF4)));
 oleControl.setHeight(100.54);
 oleControl.setWidth(201.06);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | double | عرض التحكم بالنقاط. |

