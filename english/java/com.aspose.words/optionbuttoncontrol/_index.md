---
title: OptionButtonControl
linktitle: OptionButtonControl
second_title: Aspose.Words for Java
description: The OptionButton control enables a single choice in a limited set of mutually exclusive choices in Java.
type: docs
weight: 492
url: /java/com.aspose.words/optionbuttoncontrol/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.OleControl](../../com.aspose.words/olecontrol/), [com.aspose.words.Forms2OleControl](../../com.aspose.words/forms2olecontrol/), [com.aspose.words.MorphDataControl](../../com.aspose.words/morphdatacontrol/)
```
public class OptionButtonControl extends MorphDataControl
```

The OptionButton control enables a single choice in a limited set of mutually exclusive choices.

 **Examples:** 

Shows how to select radio button.

```

 Document doc = new Document(getMyDir() + "Radio buttons.docx");

 Shape shape1 = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 OptionButtonControl optionButton1 = (OptionButtonControl)shape1.getOleFormat().getOleControl();
 // Deselect selected first item.
 optionButton1.setSelected(false);

 Shape shape2 = (Shape)doc.getChild(NodeType.SHAPE, 1, true);
 OptionButtonControl optionButton2 = (OptionButtonControl)shape2.getOleFormat().getOleControl();
 // Select second option button.
 optionButton2.setSelected(true);

 Assert.assertEquals(Forms2OleControlType.OPTION_BUTTON, optionButton1.getType());
 Assert.assertEquals(Forms2OleControlType.OPTION_BUTTON, optionButton2.getType());

 doc.save(getArtifactsDir() + "Shape.SelectRadioControl.docx");
 
```
## Methods

| Method | Description |
| --- | --- |
| [getBackColor()](#getBackColor) | Gets a background color of the control. |
| [getCaption()](#getCaption) | Gets a Caption property of the control. |
| [getChildNodes()](#getChildNodes) | Gets collection of immediate child controls. |
| [getClsidInternal()](#getClsidInternal) |  |
| [getEnabled()](#getEnabled) | Returns  true  if control is in enabled state. |
| [getExtensionForUser(String progId)](#getExtensionForUser-java.lang.String) |  |
| [getFileNameForUser()](#getFileNameForUser) |  |
| [getForeColor()](#getForeColor) | Gets a foreground color of the control. |
| [getGroupName()](#getGroupName) | Gets a string that specifies a group of mutually exclusive controls. |
| [getHeight()](#getHeight) | Gets a height of the control in points. |
| [getId()](#getId) |  |
| [getName()](#getName) | Gets name of the ActiveX control. |
| [getSelected()](#getSelected) | Gets a boolean value indicating either this [OptionButtonControl](../../com.aspose.words/optionbuttoncontrol/) is selected or not. |
| [getType()](#getType) | Gets type of Forms 2.0 control. |
| [getValue()](#getValue) | Gets underlying Value property which often represents control state. |
| [getWidth()](#getWidth) | Gets a width of the control in points. |
| [isEmpty()](#isEmpty) |  |
| [isForms2OleControl()](#isForms2OleControl) | Returns  true  if the control is a [Forms2OleControl](../../com.aspose.words/forms2olecontrol/). |
| [isForms2OleControlInternal()](#isForms2OleControlInternal) |  |
| [setBackColor(Color value)](#setBackColor-java.awt.Color) | Sets a background color of the control. |
| [setCaption(String value)](#setCaption-java.lang.String) | Sets a Caption property of the control. |
| [setForeColor(Color value)](#setForeColor-java.awt.Color) | Sets a foreground color of the control. |
| [setGroupName(String value)](#setGroupName-java.lang.String) | Sets a string that specifies a group of mutually exclusive controls. |
| [setHeight(double value)](#setHeight-double) | Sets a height of the control in points. |
| [setId(int value)](#setId-int) |  |
| [setName(String value)](#setName-java.lang.String) | Sets name of the ActiveX control. |
| [setSelected(boolean value)](#setSelected-boolean) | Sets a boolean value indicating either this [OptionButtonControl](../../com.aspose.words/optionbuttoncontrol/) is selected or not. |
| [setWidth(double value)](#setWidth-double) | Sets a width of the control in points. |
### getBackColor() {#getBackColor}
```
public Color getBackColor()
```


Gets a background color of the control. The default value depends on a type of the control.

 **Examples:** 

Shows how to set properties for ActiveX control.

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
java.awt.Color - A background color of the control.
### getCaption() {#getCaption}
```
public String getCaption()
```


Gets a Caption property of the control. Default value is an empty string.

 **Examples:** 

Shows how to set caption for ActiveX control.

```

 DocumentBuilder builder = new DocumentBuilder();

 CommandButtonControl button1 = new CommandButtonControl(); { button1.setCaption("Button caption"); }
 Shape shape = builder.insertForms2OleControl(button1);
 Assert.assertEquals("Button caption", button1.getCaption());
 
```

Shows how to verify the properties of an ActiveX control.

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
java.lang.String - A Caption property of the control.
### getChildNodes() {#getChildNodes}
```
public Forms2OleControlCollection getChildNodes()
```


Gets collection of immediate child controls.

 **Remarks:** 

Returns  null  if this control can not have children.

 **Examples:** 

Shows how to verify the properties of an ActiveX control.

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


Returns  true  if control is in enabled state.

 **Examples:** 

Shows how to verify the properties of an ActiveX control.

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
boolean -  true  if control is in enabled state.
### getExtensionForUser(String progId) {#getExtensionForUser-java.lang.String}
```
public String getExtensionForUser(String progId)
```




**Parameters:**
| Parameter | Type | Description |
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


Gets a foreground color of the control. The default value depends on a type of the control.

 **Examples:** 

Shows how to set properties for ActiveX control.

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
java.awt.Color - A foreground color of the control.
### getGroupName() {#getGroupName}
```
public String getGroupName()
```


Gets a string that specifies a group of mutually exclusive controls. The default value is an empty string.

 **Examples:** 

Shows how to verify the properties of an ActiveX control.

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
java.lang.String - A string that specifies a group of mutually exclusive controls.
### getHeight() {#getHeight}
```
public double getHeight()
```


Gets a height of the control in points.

 **Examples:** 

Shows how to set properties for ActiveX control.

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
double - A height of the control in points.
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


Gets name of the ActiveX control.

 **Examples:** 

Shows how to verify the properties of an ActiveX control.

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
java.lang.String - Name of the ActiveX control.
### getSelected() {#getSelected}
```
public boolean getSelected()
```


Gets a boolean value indicating either this [OptionButtonControl](../../com.aspose.words/optionbuttoncontrol/) is selected or not.

 **Remarks:** 

Note, this property allows you to select multiple items in a group of [OptionButtonControl](../../com.aspose.words/optionbuttoncontrol/) with the same [Forms2OleControl.getGroupName()](../../com.aspose.words/forms2olecontrol/\#getGroupName) / [Forms2OleControl.setGroupName(java.lang.String)](../../com.aspose.words/forms2olecontrol/\#setGroupName-java.lang.String). It is up to you to take care of deselecting a previously selected item when you make this [OptionButtonControl](../../com.aspose.words/optionbuttoncontrol/) selected.

 **Examples:** 

Shows how to select radio button.

```

 Document doc = new Document(getMyDir() + "Radio buttons.docx");

 Shape shape1 = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 OptionButtonControl optionButton1 = (OptionButtonControl)shape1.getOleFormat().getOleControl();
 // Deselect selected first item.
 optionButton1.setSelected(false);

 Shape shape2 = (Shape)doc.getChild(NodeType.SHAPE, 1, true);
 OptionButtonControl optionButton2 = (OptionButtonControl)shape2.getOleFormat().getOleControl();
 // Select second option button.
 optionButton2.setSelected(true);

 Assert.assertEquals(Forms2OleControlType.OPTION_BUTTON, optionButton1.getType());
 Assert.assertEquals(Forms2OleControlType.OPTION_BUTTON, optionButton2.getType());

 doc.save(getArtifactsDir() + "Shape.SelectRadioControl.docx");
 
```

**Returns:**
boolean - A boolean value indicating either this [OptionButtonControl](../../com.aspose.words/optionbuttoncontrol/) is selected or not.
### getType() {#getType}
```
public int getType()
```


Gets type of Forms 2.0 control.

 **Examples:** 

Shows how to select radio button.

```

 Document doc = new Document(getMyDir() + "Radio buttons.docx");

 Shape shape1 = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 OptionButtonControl optionButton1 = (OptionButtonControl)shape1.getOleFormat().getOleControl();
 // Deselect selected first item.
 optionButton1.setSelected(false);

 Shape shape2 = (Shape)doc.getChild(NodeType.SHAPE, 1, true);
 OptionButtonControl optionButton2 = (OptionButtonControl)shape2.getOleFormat().getOleControl();
 // Select second option button.
 optionButton2.setSelected(true);

 Assert.assertEquals(Forms2OleControlType.OPTION_BUTTON, optionButton1.getType());
 Assert.assertEquals(Forms2OleControlType.OPTION_BUTTON, optionButton2.getType());

 doc.save(getArtifactsDir() + "Shape.SelectRadioControl.docx");
 
```

**Returns:**
int - Type of Forms 2.0 control. The returned value is one of [Forms2OleControlType](../../com.aspose.words/forms2olecontroltype/) constants.
### getValue() {#getValue}
```
public String getValue()
```


Gets underlying Value property which often represents control state. For example checked option button has '1' value while unchecked has '0'. Default value is an empty string.

 **Examples:** 

Shows how to verify the properties of an ActiveX control.

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
java.lang.String - Underlying Value property which often represents control state.
### getWidth() {#getWidth}
```
public double getWidth()
```


Gets a width of the control in points.

 **Examples:** 

Shows how to set properties for ActiveX control.

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
double - A width of the control in points.
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


Returns  true  if the control is a [Forms2OleControl](../../com.aspose.words/forms2olecontrol/).

 **Examples:** 

Shows how to verify the properties of an ActiveX control.

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
boolean -  true  if the control is a [Forms2OleControl](../../com.aspose.words/forms2olecontrol/).
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


Sets a background color of the control. The default value depends on a type of the control.

 **Examples:** 

Shows how to set properties for ActiveX control.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | A background color of the control. |

### setCaption(String value) {#setCaption-java.lang.String}
```
public void setCaption(String value)
```


Sets a Caption property of the control. Default value is an empty string.

 **Examples:** 

Shows how to set caption for ActiveX control.

```

 DocumentBuilder builder = new DocumentBuilder();

 CommandButtonControl button1 = new CommandButtonControl(); { button1.setCaption("Button caption"); }
 Shape shape = builder.insertForms2OleControl(button1);
 Assert.assertEquals("Button caption", button1.getCaption());
 
```

Shows how to verify the properties of an ActiveX control.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A Caption property of the control. |

### setForeColor(Color value) {#setForeColor-java.awt.Color}
```
public void setForeColor(Color value)
```


Sets a foreground color of the control. The default value depends on a type of the control.

 **Examples:** 

Shows how to set properties for ActiveX control.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.awt.Color | A foreground color of the control. |

### setGroupName(String value) {#setGroupName-java.lang.String}
```
public void setGroupName(String value)
```


Sets a string that specifies a group of mutually exclusive controls. The default value is an empty string.

 **Examples:** 

Shows how to verify the properties of an ActiveX control.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A string that specifies a group of mutually exclusive controls. |

### setHeight(double value) {#setHeight-double}
```
public void setHeight(double value)
```


Sets a height of the control in points.

 **Examples:** 

Shows how to set properties for ActiveX control.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | A height of the control in points. |

### setId(int value) {#setId-int}
```
public void setId(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Sets name of the ActiveX control.

 **Examples:** 

Shows how to verify the properties of an ActiveX control.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | Name of the ActiveX control. |

### setSelected(boolean value) {#setSelected-boolean}
```
public void setSelected(boolean value)
```


Sets a boolean value indicating either this [OptionButtonControl](../../com.aspose.words/optionbuttoncontrol/) is selected or not.

 **Remarks:** 

Note, this property allows you to select multiple items in a group of [OptionButtonControl](../../com.aspose.words/optionbuttoncontrol/) with the same [Forms2OleControl.getGroupName()](../../com.aspose.words/forms2olecontrol/\#getGroupName) / [Forms2OleControl.setGroupName(java.lang.String)](../../com.aspose.words/forms2olecontrol/\#setGroupName-java.lang.String). It is up to you to take care of deselecting a previously selected item when you make this [OptionButtonControl](../../com.aspose.words/optionbuttoncontrol/) selected.

 **Examples:** 

Shows how to select radio button.

```

 Document doc = new Document(getMyDir() + "Radio buttons.docx");

 Shape shape1 = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 OptionButtonControl optionButton1 = (OptionButtonControl)shape1.getOleFormat().getOleControl();
 // Deselect selected first item.
 optionButton1.setSelected(false);

 Shape shape2 = (Shape)doc.getChild(NodeType.SHAPE, 1, true);
 OptionButtonControl optionButton2 = (OptionButtonControl)shape2.getOleFormat().getOleControl();
 // Select second option button.
 optionButton2.setSelected(true);

 Assert.assertEquals(Forms2OleControlType.OPTION_BUTTON, optionButton1.getType());
 Assert.assertEquals(Forms2OleControlType.OPTION_BUTTON, optionButton2.getType());

 doc.save(getArtifactsDir() + "Shape.SelectRadioControl.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A boolean value indicating either this [OptionButtonControl](../../com.aspose.words/optionbuttoncontrol/) is selected or not. |

### setWidth(double value) {#setWidth-double}
```
public void setWidth(double value)
```


Sets a width of the control in points.

 **Examples:** 

Shows how to set properties for ActiveX control.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | A width of the control in points. |

