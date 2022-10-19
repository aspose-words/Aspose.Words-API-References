---
title: Forms2OleControl
second_title: Aspose.Words for Java API Reference
description: Represents Microsoft Forms 2.0 OLE control.
type: docs
weight: 298
url: /java/com.aspose.words/forms2olecontrol/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.OleControl](../../com.aspose.words/olecontrol)
```
public abstract class Forms2OleControl extends OleControl
```

Represents Microsoft Forms 2.0 OLE control.

To learn more, visit the **Working with Ole Objects** documentation article.
## Constructors

| Constructor | Description |
| --- | --- |
| [Forms2OleControl()](#Forms2OleControl--) |  |
## Methods

| Method | Description |
| --- | --- |
| [getCaption()](#getCaption--) | Gets Caption property of control. |
| [getValue()](#getValue--) | Gets underlying Value property which often represents control state. |
| [getEnabled()](#getEnabled--) | Returns true if control is in enabled state. |
| [getChildNodes()](#getChildNodes--) | Gets collection of immediate child controls. |
| [getType()](#getType--) | Gets type of Forms 2.0 control. |
| [isForms2OleControl()](#isForms2OleControl--) |  |
### Forms2OleControl() {#Forms2OleControl--}
```
public Forms2OleControl()
```


### getCaption() {#getCaption--}
```
public String getCaption()
```


Gets Caption property of control. Default value is an empty string.

**Returns:**
java.lang.String - Caption property of control.
### getValue() {#getValue--}
```
public String getValue()
```


Gets underlying Value property which often represents control state. For example checked option button has '1' value while unchecked has '0'. Default value is an empty string.

**Returns:**
java.lang.String - Underlying Value property which often represents control state.
### getEnabled() {#getEnabled--}
```
public boolean getEnabled()
```


Returns true if control is in enabled state.

**Returns:**
boolean - True if control is in enabled state.
### getChildNodes() {#getChildNodes--}
```
public Forms2OleControlCollection getChildNodes()
```


Gets collection of immediate child controls. Returns **null** if this control can not have children.

**Returns:**
[Forms2OleControlCollection](../../com.aspose.words/forms2olecontrolcollection) - Collection of immediate child controls.
### getType() {#getType--}
```
public int getType()
```


Gets type of Forms 2.0 control.

**Returns:**
int - Type of Forms 2.0 control. The returned value is one of [Forms2OleControlType](../../com.aspose.words/forms2olecontroltype) constants.
### isForms2OleControl() {#isForms2OleControl--}
```
public boolean isForms2OleControl()
```


Returns true if the control is a [Forms2OleControl](../../com.aspose.words/forms2olecontrol).

**Returns:**
boolean
