---
title: remove_field method
second_title: Aspose.Words for Python via .NET API Reference
description: "Removes the complete form field, not just the form field special character."
type: docs
weight: 240
url: /python-net/aspose.words.fields/formfield/remove_field/
---

## remove_field() {#default}

Removes the complete form field, not just the form field special character.


```python
def remove_field(self):
    ...
```

If there is a bookmark associated with the form field, the bookmark is not removed.


### Examples

Shows how to delete a form field.

```python
doc = aw.Document(MY_DIR + "Form fields.docx")

form_field = doc.range.form_fields[3]
form_field.remove_field()
```

### See Also

* module [aspose.words.fields](../../)
* class [FormField](../)

