---
title: OleControl.isForms2OleControl property
linktitle: isForms2OleControl property
articleTitle: isForms2OleControl property
second_title: Aspose.Words for Node.js
description: "OleControl.isForms2OleControl property. Returns ``true`` if the control is a [Forms2OleControl](../../forms2olecontrol/)."
type: docs
weight: 10
url: /nodejs-net/aspose.words.drawing.ole/olecontrol/isForms2OleControl/
---

## OleControl.isForms2OleControl property

Returns ``true`` if the control is a [Forms2OleControl](../../forms2olecontrol/).



```js
get isForms2OleControl(): boolean
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
* class [OleControl](../)

