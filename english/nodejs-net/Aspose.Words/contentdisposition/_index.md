---
title: ContentDisposition enumeration
linktitle: ContentDisposition enumeration
articleTitle: ContentDisposition enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.ContentDisposition enumeration. Enumerates different ways of presenting the document at the client browser."
type: docs
weight: 270
url: /nodejs-net/aspose.words/contentdisposition/
---

## ContentDisposition enumeration

Enumerates different ways of presenting the document at the client browser.

Note that the actual behavior on the client browser might be affected by security configuration of the browser.




### Members

| Name | Description |
| --- | --- |
| Attachment | Send the document to the browser and present an option to save the document to disk or open in the application associated with the document's extension. |
| Inline | Send the document to the browser and presents an option to save the document to disk or open inside the browser. |

### Examples

Shows how to perform a mail merge, and then save the document to the client browser.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.insertField(" MERGEFIELD FullName ");
builder.insertParagraph();
builder.insertField(" MERGEFIELD Company ");
builder.insertParagraph();
builder.insertField(" MERGEFIELD Address ");
builder.insertParagraph();
builder.insertField(" MERGEFIELD City ");

doc.mailMerge.execute(new string[] { "FullName", "Company", "Address", "City" },
  new object[] { "James Bond", "MI5 Headquarters", "Milbank", "London" });

// Send the document to the client browser.
//Thrown because HttpResponse is null in the test.
expect(() => doc.save(response, "Artifacts/MailMerge.ExecuteArray.docx", aw.ContentDisposition.Inline, null)).toThrow("TODO: ArgumentNullException");

// We will need to close this response manually to ensure that we do not add any superfluous content to the document after saving.
expect(() => response.end()).toThrow("Object reference not set to an instance of an object.");
```

### See Also

* module [Aspose.Words](../)

