---
title: DocumentBuilder.insertCheckBox method
linktitle: insertCheckBox method
articleTitle: insertCheckBox method
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.DocumentBuilder.insertCheckBox method"
type: docs
weight: 290
url: /nodejs-net/Aspose.Words/documentbuilder/insertCheckBox/
---

## insertCheckBox(name, checkedValue, size) {#string_boolean_number}

Inserts a checkbox form field at the current position.


```js
insertCheckBox(name: stringcheckedValue: booleansize: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | string | The name of the form field. Can be an empty string. The value longer than 20 characters will be truncated. |
| checkedValue | boolean | Checked status of the checkbox form field. |
| size | number | Specifies the size of the checkbox in points. Specify 0 for MS Word to calculate the size of the checkbox automatically. |

### Remarks

If you specify a name for the form field, then a bookmark is automatically created with the same name.




### Returns

The form field node that was just inserted.


## insertCheckBox(name, defaultValue, checkedValue, size) {#string_boolean_boolean_number}

Inserts a checkbox form field at the current position.


```js
insertCheckBox(name: stringdefaultValue: booleancheckedValue: booleansize: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| name | string | The name of the form field. Can be an empty string. The value longer than 20 characters will be truncated. |
| defaultValue | boolean | Default value of the checkbox form field. |
| checkedValue | boolean | Current checked status of the checkbox form field. |
| size | number | Specifies the size of the checkbox in points. Specify 0 for MS Word to calculate the size of the checkbox automatically. |

### Remarks

If you specify a name for the form field, then a bookmark is automatically created with the same name.




### Returns

The form field node that was just inserted.


## Examples

Shows how to insert checkboxes into the document.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert checkboxes of varying sizes and default checked statuses.
builder.write("Unchecked check box of a default size: ");
builder.insertCheckBox('', false, false, 0);
builder.insertParagraph();

builder.write("Large checked check box: ");
builder.insertCheckBox("CheckBox_Default", true, true, 50);
builder.insertParagraph();

// Form fields have a name length limit of 20 characters.
builder.write("Very large checked check box: ");
builder.insertCheckBox("CheckBox_OnlyCheckedValue", true, 100);

expect(doc.range.formFields.at(2).name).toEqual("CheckBox_OnlyChecked");

// We can interact with these check boxes in Microsoft Word by double clicking them.
doc.save(base.artifactsDir + "DocumentBuilder.insertCheckBox.docx");
```

## See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

