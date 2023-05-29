---
title: ContentDisposition enumeration
linktitle: ContentDisposition enumeration
articleTitle: ContentDisposition enumeration
second_title: Aspose.Words for Python
description: "aspose.words.ContentDisposition enumeration. Enumerates different ways of presenting the document at the client browser."
type: docs
weight: 240
url: /python-net/aspose.words/contentdisposition/
---

## ContentDisposition enumeration

Enumerates different ways of presenting the document at the client browser.

Note that the actual behavior on the client browser might be affected by security configuration of the browser.




### Members

| Name | Description |
| --- | --- |
| ATTACHMENT | Send the document to the browser and present an option to save the document to disk or open in the application associated with the document's extension. |
| INLINE | Send the document to the browser and presents an option to save the document to disk or open inside the browser. |

### Examples

Shows how to perform a mail merge, and then save the document to the client browser.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.insert_field(" MERGEFIELD FullName ")
builder.insert_paragraph()
builder.insert_field(" MERGEFIELD Company ")
builder.insert_paragraph()
builder.insert_field(" MERGEFIELD Address ")
builder.insert_paragraph()
builder.insert_field(" MERGEFIELD City ")

doc.mail_merge.execute(["FullName", "Company", "Address", "City"],
    ["James Bond", "MI5 Headquarters", "Milbank", "London"])

# Send the document to the client browser.
with self.assertRaises(Exception):
    #Thrown because HttpResponse is null in the test.
    doc.save(response, "Artifacts/MailMerge.execute_array.docx", aw.ContentDisposition.INLINE, None)

# We will need to close this response manually to ensure that we do not add any superfluous content to the document after saving.
with self.assertRaises(Exception):
    response.end()
```

### See Also

* module [aspose.words](../)

