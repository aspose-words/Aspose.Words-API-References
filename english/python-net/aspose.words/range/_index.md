---
title: Range class
linktitle: Range class
articleTitle: Range class
second_title: Aspose.Words for Python
description: "aspose.words.Range class. Represents a contiguous area in a document"
type: docs
weight: 1020
url: /python-net/aspose.words/range/
---

## Range class

Represents a contiguous area in a document.
To learn more, visit the [Working with Ranges](https://docs.aspose.com/words/python-net/working-with-ranges/) documentation article.




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
| [form_fields](./form_fields/) | Returns a [Range.form_fields](./form_fields/) collection that represents all form fields in the range. |
| [revisions](./revisions/) | Gets a collection of revisions (tracked changes) that exist in this range. |
| [structured_document_tags](./structured_document_tags/) | Returns a [Range.structured_document_tags](./structured_document_tags/) collection that represents all structured document tags in the range. |
| [text](./text/) | Gets the text of the range. |

### Methods

| Name | Description |
| --- | --- |
|[ delete()](./delete/#default) | Deletes all characters of the range. |
|[ normalize_field_types()](./normalize_field_types/#default) | Changes field type values [FieldChar.field_type](../../aspose.words.fields/fieldchar/field_type/) of [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/) in this range so that they correspond to the field types contained in the field codes. |
|[ replace(pattern, replacement)](./replace/#str_str) | Replaces all occurrences of a specified character string pattern with a replacement string. |
|[ replace(pattern, replacement, options)](./replace/#str_str_findreplaceoptions) | Replaces all occurrences of a specified character string pattern with a replacement string. |
|[ replace_regex(pattern, replacement)](./replace_regex/#str_str) | Replaces all occurrences of a character pattern specified by a regular expression with another string. |
|[ replace_regex(pattern, replacement, options)](./replace_regex/#str_str_findreplaceoptions) | Replaces all occurrences of a character pattern specified by a regular expression with another string. |
|[ to_document()](./to_document/#default) | Constructs a new fully formed document that contains the range. |
|[ unlink_fields()](./unlink_fields/#default) | Unlinks fields in this range. |
|[ update_fields()](./update_fields/#default) | Updates the values of document fields in this range. |

### Examples

Shows how to get the text contents of all the nodes that a range covers.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Hello world!')
self.assertEqual('Hello world!', doc.range.text.strip())
```

### See Also

* module [aspose.words](../)

