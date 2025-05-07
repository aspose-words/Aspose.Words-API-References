---
title: Forms2OleControl class
linktitle: Forms2OleControl class
articleTitle: Forms2OleControl class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Drawing.Ole.Forms2OleControl class. Represents Microsoft Forms 2.0 OLE control"
type: docs
weight: 30
url: /nodejs-net/aspose.words.drawing.ole/forms2olecontrol/
---

## Forms2OleControl class

Represents Microsoft Forms 2.0 OLE control.
To learn more, visit the [Working with Ole Objects](https://docs.aspose.com/words/nodejs-net/working-with-ole-objects/) documentation article.




**Inheritance:** [Forms2OleControl](./) → [OleControl](../olecontrol/)

### Properties

| Name | Description |
| --- | --- |
| [backColor](./backColor/) | Gets or sets a background color of the control. The default value depends on a type of the control. |
| [caption](./caption/) | Gets or sets a Caption property of the control. Default value is an empty string. |
| [childNodes](./childNodes/) | Gets collection of immediate child controls. |
| [enabled](./enabled/) | Returns ``true`` if control is in enabled state. |
| [foreColor](./foreColor/) | Gets or sets a foreground color of the control. The default value depends on a type of the control. |
| [groupName](./groupName/) | Gets or sets a string that specifies a group of mutually exclusive controls. The default value is an empty string. |
| [height](./height/) | Gets or sets a height of the control in points. |
| [isForms2OleControl](../olecontrol/isForms2OleControl/) | Returns ``true`` if the control is a [Forms2OleControl](./).<br>(Inherited from [OleControl](../olecontrol/)) |
| [name](../olecontrol/name/) | Gets or sets name of the ActiveX control.<br>(Inherited from [OleControl](../olecontrol/)) |
| [type](./type/) | Gets type of Forms 2.0 control. |
| [value](./value/) | Gets underlying Value property which often represents control state. For example checked option button has '1' value while unchecked has '0'. Default value is an empty string. |
| [width](./width/) | Gets or sets a width of the control in points. |

### Methods

| Name | Description |
| --- | --- |
|[ asCheckBoxControl()](../olecontrol/asCheckBoxControl/#default) | <br>(Inherited from [OleControl](../olecontrol/)) |
|[ asForms2OleControl()](../olecontrol/asForms2OleControl/#default) | <br>(Inherited from [OleControl](../olecontrol/)) |
|[ asOptionButtonControl()](../olecontrol/asOptionButtonControl/#default) | <br>(Inherited from [OleControl](../olecontrol/)) |
|[ asTextBoxControl()](../olecontrol/asTextBoxControl/#default) | <br>(Inherited from [OleControl](../olecontrol/)) |

### Examples

Shows how to verify the properties of an ActiveX control.

```js
let doc = new aw.Document(base.myDir + "ActiveX controls.docx");

let shape = doc.getShape(0, true);
let oleControl = shape.oleFormat.oleControl;

expect(oleControl.name).toEqual("CheckBox1");

if (oleControl.isForms2OleControl)
{
  console.log(oleControl);
  let checkBox = oleControl.asForms2OleControl();
  expect(checkBox.caption).toEqual("First");
  expect(checkBox.value).toEqual("0");
  expect(checkBox.enabled).toEqual(true);
  expect(checkBox.type).toEqual(aw.Drawing.Ole.Forms2OleControlType.CheckBox);
  expect(checkBox.childNodes).toEqual(null);
  expect(checkBox.groupName).toEqual('');

  // Note, that you can't set GroupName for a Frame.
  checkBox.groupName = "Aspose group name";
}
```

### See Also

* module [Aspose.Words.Drawing.Ole](../)
* class [OleControl](../olecontrol/)

