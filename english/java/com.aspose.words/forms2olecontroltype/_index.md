---
title: Forms2OleControlType
linktitle: Forms2OleControlType
second_title: Aspose.Words for Java
description: Enumerates types of Forms 2.0 controls in Java.
type: docs
weight: 350
url: /java/com.aspose.words/forms2olecontroltype/
---

**Inheritance:**
java.lang.Object
```
public class Forms2OleControlType
```

Enumerates types of Forms 2.0 controls.

 **Examples:** 

Shows how to change state of the CheckBox control.

```

 Document doc = new Document(getMyDir() + "ActiveX controls.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 CheckBoxControl checkBoxControl = (CheckBoxControl)shape.getOleFormat().getOleControl();
 checkBoxControl.setChecked(true);

 Assert.assertEquals(true, checkBoxControl.getChecked());
 Assert.assertEquals(Forms2OleControlType.CHECK_BOX, checkBoxControl.getType());
 
```
## Fields

| Field | Description |
| --- | --- |
| [CHECK_BOX](#CHECK-BOX) | A control that allows the user to select or deselect an option. |
| [COMBO_BOX](#COMBO-BOX) | A control that allows the user to select an item from a list. |
| [COMMAND_BUTTON](#COMMAND-BUTTON) | A button that triggers an action when clicked. |
| [FORM](#FORM) | A container for other controls. |
| [FRAME](#FRAME) | A control that groups other controls. |
| [IMAGE](#IMAGE) | A control that displays an image. |
| [LABEL](#LABEL) | A control that displays text. |
| [LIST_BOX](#LIST-BOX) | A control that displays a list of items. |
| [MULTI_PAGE](#MULTI-PAGE) | A control that displays multiple pages of content. |
| [OPTION_BUTTON](#OPTION-BUTTON) | A radio button control. |
| [SCROLL_BAR](#SCROLL-BAR) | A control that allows the user to scroll through content. |
| [SPIN_BUTTON](#SPIN-BUTTON) | A control that allows the user to increase or decrease a value. |
| [TAB_STRIP](#TAB-STRIP) | A control that allows the user to switch between multiple pages of content. |
| [TEXTBOX](#TEXTBOX) | A control that allows the user to enter text. |
| [TOGGLE_BUTTON](#TOGGLE-BUTTON) | A control that allows the user to toggle between two states. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String forms2OleControlTypeName)](#fromName-java.lang.String) |  |
| [getName(int forms2OleControlType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int forms2OleControlType)](#toString-int) |  |
### CHECK_BOX {#CHECK-BOX}
```
public static int CHECK_BOX
```


A control that allows the user to select or deselect an option.

### COMBO_BOX {#COMBO-BOX}
```
public static int COMBO_BOX
```


A control that allows the user to select an item from a list.

### COMMAND_BUTTON {#COMMAND-BUTTON}
```
public static int COMMAND_BUTTON
```


A button that triggers an action when clicked.

### FORM {#FORM}
```
public static int FORM
```


A container for other controls.

### FRAME {#FRAME}
```
public static int FRAME
```


A control that groups other controls.

### IMAGE {#IMAGE}
```
public static int IMAGE
```


A control that displays an image.

### LABEL {#LABEL}
```
public static int LABEL
```


A control that displays text.

### LIST_BOX {#LIST-BOX}
```
public static int LIST_BOX
```


A control that displays a list of items.

### MULTI_PAGE {#MULTI-PAGE}
```
public static int MULTI_PAGE
```


A control that displays multiple pages of content.

### OPTION_BUTTON {#OPTION-BUTTON}
```
public static int OPTION_BUTTON
```


A radio button control.

### SCROLL_BAR {#SCROLL-BAR}
```
public static int SCROLL_BAR
```


A control that allows the user to scroll through content.

### SPIN_BUTTON {#SPIN-BUTTON}
```
public static int SPIN_BUTTON
```


A control that allows the user to increase or decrease a value.

### TAB_STRIP {#TAB-STRIP}
```
public static int TAB_STRIP
```


A control that allows the user to switch between multiple pages of content.

### TEXTBOX {#TEXTBOX}
```
public static int TEXTBOX
```


A control that allows the user to enter text.

### TOGGLE_BUTTON {#TOGGLE-BUTTON}
```
public static int TOGGLE_BUTTON
```


A control that allows the user to toggle between two states.

### length {#length}
```
public static int length
```


### fromName(String forms2OleControlTypeName) {#fromName-java.lang.String}
```
public static int fromName(String forms2OleControlTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| forms2OleControlTypeName | java.lang.String |  |

**Returns:**
int
### getName(int forms2OleControlType) {#getName-int}
```
public static String getName(int forms2OleControlType)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| forms2OleControlType | int |  |

**Returns:**
java.lang.String
