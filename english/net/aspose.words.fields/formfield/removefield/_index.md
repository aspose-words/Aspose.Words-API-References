---
title: FormField.RemoveField
linktitle: RemoveField
articleTitle: RemoveField
second_title: Aspose.Words for .NET
description: Effortlessly remove entire form fields with the FormField RemoveField method, enhancing your document's clarity and organization.
type: docs
weight: 240
url: /net/aspose.words.fields/formfield/removefield/
---
## FormField.RemoveField method

Removes the complete form field, not just the form field special character.

```csharp
public void RemoveField()
```

## Remarks

If there is a bookmark associated with the form field, the bookmark is not removed.

## Examples

Shows how to delete a form field.

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

FormField formField = doc.Range.FormFields[3];
formField.RemoveField();
```

### See Also

* class [FormField](../)
* namespace [Aspose.Words.Fields](../../../aspose.words.fields/)
* assembly [Aspose.Words](../../../)
