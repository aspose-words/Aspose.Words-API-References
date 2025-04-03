---
title: BuiltInDocumentProperties.keywords property
linktitle: keywords property
articleTitle: keywords property
second_title: Aspose.Words for NodeJs
description: "BuiltInDocumentProperties.keywords property. Gets or sets the document keywords."
type: docs
weight: 130
url: /nodejs-net/aspose.words.properties/builtindocumentproperties/keywords/
---

## BuiltInDocumentProperties.keywords property

Gets or sets the document keywords.


```js
get keywords(): string
```

### Examples

Shows how to work with built-in document properties in the "Description" category.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);
let properties = doc.builtInDocumentProperties;

// Below are four built-in document properties that have fields that can display their values in the document body.
// 1 -  "Author" property, which we can display using an AUTHOR field:
properties.author = "John Doe";
builder.write("Author:\t");
builder.insertField(aw.Fields.FieldType.FieldAuthor, true);

// 2 -  "Title" property, which we can display using a TITLE field:
properties.title = "John's Document";
builder.write("\nDoc title:\t");
builder.insertField(aw.Fields.FieldType.FieldTitle, true);

// 3 -  "Subject" property, which we can display using a SUBJECT field:
properties.subject = "My subject";
builder.write("\nSubject:\t");
builder.insertField(aw.Fields.FieldType.FieldSubject, true);

// 4 -  "Comments" property, which we can display using a COMMENTS field:
properties.comments = `This is ${properties.author}'s document about ${properties.subject}`;
builder.write("\nComments:\t\"");
builder.insertField(aw.Fields.FieldType.FieldComments, true);
builder.write("\"");

// The "Category" built-in property does not have a field that can display its value.
properties.category = "My category";

// We can set multiple keywords for a document by separating the string value of the "Keywords" property with semicolons.
properties.keywords = "Tag 1; Tag 2; Tag 3";

// We can right-click this document in Windows Explorer and find these properties in "Properties" -> "Details".
// The "Author" built-in property is in the "Origin" group, and the others are in the "Description" group.
doc.save(base.artifactsDir + "DocumentProperties.description.docx");
```

### See Also

* module [Aspose.Words.Properties](../../)
* class [BuiltInDocumentProperties](../)

