---
title: Range Class
linktitle: Range
articleTitle: Range
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Range class, your key to managing document sections effortlessly. Enhance your document processing with seamless control and flexibility.
type: docs
weight: 5280
url: /net/aspose.words/range/
---
## Range class

Represents a contiguous area in a document.

To learn more, visit the [Working with Ranges](https://docs.aspose.com/words/net/working-with-ranges/) documentation article.

```csharp
public class Range : IEnumerable<Node>
```

## Properties

| Name | Description |
| --- | --- |
| [Bookmarks](../../aspose.words/range/bookmarks/) { get; } | Returns a [`Bookmarks`](./bookmarks/) collection that represents all bookmarks in the range. |
| [Fields](../../aspose.words/range/fields/) { get; } | Returns a [`Fields`](./fields/) collection that represents all fields in the range. |
| [FormFields](../../aspose.words/range/formfields/) { get; } | Returns a [`FormFields`](./formfields/) collection that represents all form fields in the range. |
| [Revisions](../../aspose.words/range/revisions/) { get; } | Gets a collection of revisions (tracked changes) that exist in this range. |
| [StructuredDocumentTags](../../aspose.words/range/structureddocumenttags/) { get; } | Returns a [`StructuredDocumentTags`](./structureddocumenttags/) collection that represents all structured document tags in the range. |
| [Text](../../aspose.words/range/text/) { get; } | Gets the text of the range. |

## Methods

| Name | Description |
| --- | --- |
| [Delete](../../aspose.words/range/delete/)() | Deletes all characters of the range. |
| [GetEnumerator](../../aspose.words/range/getenumerator/)() |  |
| [NormalizeFieldTypes](../../aspose.words/range/normalizefieldtypes/)() | Changes field type values [`FieldType`](../../aspose.words.fields/fieldchar/fieldtype/) of [`FieldStart`](../../aspose.words.fields/fieldstart/), [`FieldSeparator`](../../aspose.words.fields/fieldseparator/), [`FieldEnd`](../../aspose.words.fields/fieldend/) in this range so that they correspond to the field types contained in the field codes. |
| [Replace](../../aspose.words/range/replace/#replace_2)(*Regex, string*) | Replaces all occurrences of a character pattern specified by a regular expression with another string. |
| [Replace](../../aspose.words/range/replace/#replace)(*string, string*) | Replaces all occurrences of a specified character string pattern with a replacement string. |
| [Replace](../../aspose.words/range/replace/#replace_3)(*Regex, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | Replaces all occurrences of a character pattern specified by a regular expression with another string. |
| [Replace](../../aspose.words/range/replace/#replace_1)(*string, string, [FindReplaceOptions](../../aspose.words.replacing/findreplaceoptions/)*) | Replaces all occurrences of a specified character string pattern with a replacement string. |
| [ToDocument](../../aspose.words/range/todocument/)() | Constructs a new fully formed document that contains the range. |
| [UnlinkFields](../../aspose.words/range/unlinkfields/)() | Unlinks fields in this range. |
| [UpdateFields](../../aspose.words/range/updatefields/)() | Updates the values of document fields in this range. |

## Remarks

The document is represented by a tree of nodes and the nodes provide operations to work with the tree, but some operations are easier to perform if the document is treated as a contiguous sequence of text.

`Range` is a "facade" interface that provide methods that treat the document or portions of the document as "flat" text regardless of the fact that the document nodes are stored in a tree-like object model.

`Range` does not contain any text or nodes, it is merely a view or "window" over a fragment of a document.

## Examples

Shows how to get the text contents of all the nodes that a range covers.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.That(doc.Range.Text.Trim(), Is.EqualTo("Hello world!"));
```

### See Also

* class [Node](../node/)
* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
