---
title: delete_fields method
second_title: Aspose.Words for Python via .NET API Reference
description: "Removes mail merge related fields from the document."
type: docs
weight: 170
url: /python-net/aspose.words.mailmerging/mailmerge/delete_fields/
---

## delete_fields() {#default}

Removes mail merge related fields from the document.


```python
def delete_fields(self):
    ...
```

This method removes MERGEFIELD and NEXT fields from the document.

This method could be useful if your mail merge operation does not always need
to populate all fields in the document. Use this method to remove all remaining
mail merge fields.




### Examples

Shows how to delete all MERGEFIELDs from a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.write("Dear ")
builder.insert_field(" MERGEFIELD FirstName ")
builder.write(" ")
builder.insert_field(" MERGEFIELD LastName ")
builder.writeln(",")
builder.writeln("Greetings!")

self.assertEqual(
    "Dear \u0013 MERGEFIELD FirstName \u0014«FirstName»\u0015 \u0013 MERGEFIELD LastName \u0014«LastName»\u0015,\rGreetings!",
    doc.get_text().strip())

doc.mail_merge.delete_fields()

self.assertEqual("Dear  ,\rGreetings!", doc.get_text().strip())
```

### See Also

* module [aspose.words.mailmerging](../../)
* class [MailMerge](../)

