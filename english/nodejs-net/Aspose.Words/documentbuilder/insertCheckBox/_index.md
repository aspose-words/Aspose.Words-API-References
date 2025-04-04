---
title: DocumentBuilder.insertCheckBox method
linktitle: insertCheckBox method
articleTitle: insertCheckBox method
second_title: Aspose.Words for Node.js
description: "Aspose.Words.DocumentBuilder.insertCheckBox method"
type: docs
weight: 290
url: /nodejs-net/aspose.words/documentbuilder/insertCheckBox/
---

## insertCheckBox(name, checkedValue, size) {#string_boolean_number}

Inserts a checkbox form field at the current position.


```js
insertCheckBox(name: string, checkedValue: boolean, size: number)
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
insertCheckBox(name: string, defaultValue: boolean, checkedValue: boolean, size: number)
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


## See Also

* module [Aspose.Words](../../)
* class [DocumentBuilder](../)

