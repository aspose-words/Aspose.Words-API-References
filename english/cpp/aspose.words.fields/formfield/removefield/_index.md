---
title: RemoveField
second_title: Aspose.Words for C++ API Reference
description: Removes the complete form field, not just the form field special character.
type: docs
weight: 300
url: /cpp/aspose.words.fields/formfield/removefield/
---
## FormField.RemoveField method


Removes the complete form field, not just the form field special character.

```cpp
void Aspose::Words::Fields::FormField::RemoveField()
```


## Examples




Shows how to delete a form field. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Form fields.docx");

SharedPtr<FormField> formField = doc->get_Range()->get_FormFields()->idx_get(3);
formField->RemoveField();
```

