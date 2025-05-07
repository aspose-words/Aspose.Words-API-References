---
title: Forms2OleControl.caption property
linktitle: caption property
articleTitle: caption property
second_title: Aspose.Words for Node.js
description: "Forms2OleControl.caption property. Gets or sets a Caption property of the control"
type: docs
weight: 20
url: /nodejs-net/aspose.words.drawing.ole/forms2olecontrol/caption/
---

## Forms2OleControl.caption property

Gets or sets a Caption property of the control.
Default value is an empty string.


```js
get caption(): string
```

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

* module [Aspose.Words.Drawing.Ole](../../)
* class [Forms2OleControl](../)

