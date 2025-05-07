---
title: DocumentBuilder.insertTableOfContents method
linktitle: insertTableOfContents method
articleTitle: insertTableOfContents method
second_title: Aspose.Words for Node.js
description: "DocumentBuilder.insertTableOfContents method. Inserts a TOC (table of contents) field into the document."
type: docs
weight: 500
url: /nodejs-net/aspose.words/documentbuilder/insertTableOfContents/
---

## insertTableOfContents(switches) {#string}

Inserts a TOC (table of contents) field into the document.


```js
insertTableOfContents(switches: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| switches | string | The TOC field switches. |

### Remarks

This method inserts a TOC (table of contents) field into the document at
the current position.

A table of contents in a Word document can be built in a number of ways
and formatted using a variety of options. The way the table is built and
displayed by Microsoft Word is controlled by the field switches.

The easiest way to specify the switches is to insert and configure a table of
contents into a Word document using the Insert-\>Reference-\>Index and Tables menu,
then switch display of field codes on to see the switches. You can press Alt+F9 in
Microsoft Word to toggle display of field codes on or off.

For example, after creating a table of contents, the following field is inserted
into the document: ****.
You can copy **** and use it as the switches parameter.

Note that [DocumentBuilder.insertTableOfContents()](./#string) will only insert a TOC field, but
will not actually build the table of contents. The table of contents is built by
Microsoft Word when the field is updated.

If you insert a table of contents using this method and then open the file
in Microsoft Word, you will not see the table of contents because the TOC field
has not yet been updated.

In Microsoft Word, fields are not automatically updated when a document is opened,
but you can update fields in a document at any time by pressing F9.




### Examples

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
* class [DocumentBuilder](../)

