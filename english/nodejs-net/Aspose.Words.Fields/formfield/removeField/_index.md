---
title: FormField.removeField method
linktitle: removeField method
articleTitle: removeField method
second_title: Aspose.Words for NodeJs
description: "FormField.removeField method. Removes the complete form field, not just the form field special character."
type: docs
weight: 240
url: /nodejs-net/Aspose.Words.Fields/formfield/removeField/
---

## removeField() {#default}

Removes the complete form field, not just the form field special character.


```js
removeField()
```

### Remarks

If there is a bookmark associated with the form field, the bookmark is not removed.


### Examples

Shows how to delete a form field.

```js
let doc = new aw.Document(base.myDir + "Form fields.docx");

let formField = doc.range.formFields.at(3);
formField.removeField();
```

### See Also

* module [Aspose.Words.Fields](../../)
* class [FormField](../)

