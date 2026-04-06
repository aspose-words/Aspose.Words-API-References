---
title: Document.updateFields method
linktitle: updateFields method
articleTitle: updateFields method
second_title: Aspose.Words for Node.js
description: "Document.updateFields method. Updates the values of fields in the whole document."
type: docs
weight: 740
url: /nodejs-net/aspose.words/document/updateFields/
---

## updateFields() {#default}

Updates the values of fields in the whole document.


```js
updateFields()
```

### Remarks

When you open, modify and then save a document, Aspose.Words does not update fields automatically, it keeps them intact.
Therefore, you would usually want to call this method before saving if you have modified the document
programmatically and want to make sure the proper (calculated) field values appear in the saved document.

There is no need to update fields after executing a mail merge because mail merge is a kind of field update
and automatically updates all fields in the document.

This method does not update all field types. For the detailed list of supported field types, see the Programmers Guide.

This method does not update fields that are related to the page layout algorithms (e.g. PAGE, PAGES, PAGEREF).
The page layout-related fields are updated when you render a document or call [Document.updatePageLayout()](../updatePageLayout/#default).

Use the [Document.normalizeFieldTypes()](../normalizeFieldTypes/#default) method before fields updating if there were document changes that affected field types.

To update fields in a specific part of the document use [Range.updateFields()](../../range/updateFields/#default).




### Examples

Shows how to set user details, and display them using fields.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Create a UserInformation object and set it as the data source for fields that display user information.
let userInformation = new aw.Fields.UserInformation();
userInformation.name = "John Doe";
userInformation.initials = "J. D.";
userInformation.address = "123 Main Street";
doc.fieldOptions.currentUser = userInformation;

// Insert USERNAME, USERINITIALS, and USERADDRESS fields, which display values of
// the respective properties of the UserInformation object that we have created above.
expect(builder.insertField(" USERNAME ").result).toEqual(userInformation.name);
expect(builder.insertField(" USERINITIALS ").result).toEqual(userInformation.initials);
expect(builder.insertField(" USERADDRESS ").result).toEqual(userInformation.address);

// The field options object also has a static default user that fields from all documents can refer to.
aw.Fields.UserInformation.defaultUser.name = "Default User";
aw.Fields.UserInformation.defaultUser.initials = "D. U.";
aw.Fields.UserInformation.defaultUser.address = "One Microsoft Way";
doc.fieldOptions.currentUser = aw.Fields.UserInformation.defaultUser;

expect(builder.insertField(" USERNAME ").result).toEqual("Default User");
expect(builder.insertField(" USERINITIALS ").result).toEqual("D. U.");
expect(builder.insertField(" USERADDRESS ").result).toEqual("One Microsoft Way");

doc.updateFields();
doc.save(base.artifactsDir + "FieldOptions.currentUser.docx");
```

Shows how to insert a Table of contents (TOC) into a document using heading styles as entries.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

// Insert a table of contents for the first page of the document.
// Configure the table to pick up paragraphs with headings of levels 1 to 3.
// Also, set its entries to be hyperlinks that will take us
// to the location of the heading when left-clicked in Microsoft Word.
builder.insertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.insertBreak(aw.BreakType.PageBreak);

// Populate the table of contents by adding paragraphs with heading styles.
// Each such heading with a level between 1 and 3 will create an entry in the table.
builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading1;
builder.writeln("Heading 1");

builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading2;
builder.writeln("Heading 1.1");
builder.writeln("Heading 1.2");

builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading1;
builder.writeln("Heading 2");
builder.writeln("Heading 3");

builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading2;
builder.writeln("Heading 3.1");

builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading3;
builder.writeln("Heading 3.1.1");
builder.writeln("Heading 3.1.2");
builder.writeln("Heading 3.1.3");

builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading4;
builder.writeln("Heading 3.1.3.1");
builder.writeln("Heading 3.1.3.2");

builder.paragraphFormat.styleIdentifier = aw.StyleIdentifier.Heading2;
builder.writeln("Heading 3.2");
builder.writeln("Heading 3.3");

// A table of contents is a field of a type that needs to be updated to show an up-to-date result.
doc.updateFields();
doc.save(base.artifactsDir + "DocumentBuilder.InsertToc.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Document](../)

