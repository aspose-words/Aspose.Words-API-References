---
title: OleControl class
linktitle: OleControl class
articleTitle: OleControl class
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Drawing.Ole.OleControl class. Represents OLE ActiveX control"
type: docs
weight: 70
url: /nodejs-net/aspose.words.drawing.ole/olecontrol/
---

## OleControl class

Represents OLE ActiveX control.
To learn more, visit the [Working with Ole Objects](https://docs.aspose.com/words/nodejs-net/working-with-ole-objects/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [isForms2OleControl](./isForms2OleControl/) | Returns ``true`` if the control is a [Forms2OleControl](../forms2olecontrol/). |
| [name](./name/) | Gets or sets name of the ActiveX control. |

### Methods

| Name | Description |
| --- | --- |
|[ asCheckBoxControl()](./asCheckBoxControl/#default) |  |
|[ asForms2OleControl()](./asForms2OleControl/#default) |  |
|[ asOptionButtonControl()](./asOptionButtonControl/#default) |  |
|[ asTextBoxControl()](./asTextBoxControl/#default) |  |

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

