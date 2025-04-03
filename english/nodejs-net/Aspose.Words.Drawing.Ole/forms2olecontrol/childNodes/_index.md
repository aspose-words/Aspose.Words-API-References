---
title: Forms2OleControl.childNodes property
linktitle: childNodes property
articleTitle: childNodes property
second_title: Aspose.Words for NodeJs
description: "Forms2OleControl.childNodes property. Gets collection of immediate child controls."
type: docs
weight: 30
url: /nodejs-net/aspose.words.drawing.ole/forms2olecontrol/childNodes/
---

## Forms2OleControl.childNodes property

Gets collection of immediate child controls.


```js
get childNodes(): Aspose.Words.Drawing.Ole.Forms2OleControlCollection
```

### Remarks

Returns ``null`` if this control can not have children.


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

