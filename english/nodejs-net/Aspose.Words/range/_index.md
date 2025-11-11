---
title: Range class
linktitle: Range class
articleTitle: Range class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Range class. Represents a contiguous area in a document"
type: docs
weight: 1080
url: /nodejs-net/aspose.words/range/
---

## Range class

Represents a contiguous area in a document.
To learn more, visit the [Working with Ranges](https://docs.aspose.com/words/nodejs-net/working-with-ranges/) documentation article.




### Remarks

The document is represented by a tree of nodes and the nodes provide operations
to work with the tree, but some operations are easier to perform if the document
is treated as a contiguous sequence of text.

[Range](./) is a "facade" interface that provide methods that treat the document
or portions of the document as "flat" text regardless of the fact that the document
nodes are stored in a tree-like object model.

[Range](./) does not contain any text or nodes, it is merely a view or "window"
over a fragment of a document.




### Properties

| Name | Description |
| --- | --- |
| [bookmarks](./bookmarks/) | Returns a [Range.bookmarks](./bookmarks/) collection that represents all bookmarks in the range. |
| [fields](./fields/) | Returns a [Range.fields](./fields/) collection that represents all fields in the range. |
| [formFields](./formFields/) | Returns a [Range.formFields](./formFields/) collection that represents all form fields in the range. |
| [revisions](./revisions/) | Gets a collection of revisions (tracked changes) that exist in this range. |
| [structuredDocumentTags](./structuredDocumentTags/) | Returns a [Range.structuredDocumentTags](./structuredDocumentTags/) collection that represents all structured document tags in the range. |
| [text](./text/) | Gets the text of the range. |

### Methods

| Name | Description |
| --- | --- |
|[ delete()](./delete/#default) | Deletes all characters of the range. |
|[ normalizeFieldTypes()](./normalizeFieldTypes/#default) | Changes field type values [FieldChar.fieldType](../../aspose.words.fields/fieldchar/fieldType/) of [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/) in this range so that they correspond to the field types contained in the field codes. |
|[ replace(pattern, replacement)](./replace/#string_string) | Replaces all occurrences of a specified character string pattern with a replacement string. |
|[ replace(pattern, replacement, options)](./replace/#string_string_findreplaceoptions) | Replaces all occurrences of a specified character string pattern with a replacement string. |
|[ replaceRegex(pattern, replacement)](./replaceRegex/#string_string) | Replaces all occurrences of a character pattern specified by a regular expression with another string. |
|[ replaceRegex(pattern, replacement, options)](./replaceRegex/#string_string_findreplaceoptions) | Replaces all occurrences of a character pattern specified by a regular expression with another string. |
|[ toDocument()](./toDocument/#default) | Constructs a new fully formed document that contains the range. |
|[ unlinkFields()](./unlinkFields/#default) | Unlinks fields in this range. |
|[ updateFields()](./updateFields/#default) | Updates the values of document fields in this range. |

### Examples

Shows how to get the text contents of all the nodes that a range covers.

```js
let doc = new aw.Document();
let builder = new aw.DocumentBuilder(doc);

builder.write("Hello world!");

expect(doc.range.text.trim()).toEqual("Hello world!");
```

### See Also

* module [Aspose.Words](../)

