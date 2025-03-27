---
title: Forms2OleControl.value property
linktitle: value property
articleTitle: value property
second_title: Aspose.Words for NodeJs
description: "Forms2OleControl.value property. Gets underlying Value property which often represents control state"
type: docs
weight: 90
url: /nodejs-net/Aspose.Words.Drawing.Ole/forms2olecontrol/value/
---

## Forms2OleControl.value property

Gets underlying Value property which often represents control state.
For example checked option button has '1' value while unchecked has '0'.
Default value is an empty string.


```js
get value(): string
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

