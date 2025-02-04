---
title: Aspose::Words::Range class
linktitle: Range
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Range class. Represents a contiguous area in a document. To learn more, visit the  documentation article in C++.'
type: docs
weight: 51000
url: /cpp/aspose.words/range/
---
## Range class


Represents a contiguous area in a document. To learn more, visit the [Working with Ranges](https://docs.aspose.com/words/cpp/working-with-ranges/) documentation article.

```cpp
class Range : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>
```

## Methods

| Method | Description |
| --- | --- |
| [Delete](./delete/)() | Deletes all characters of the range. |
| [get_Bookmarks](./get_bookmarks/)() | Returns a [Bookmarks](./get_bookmarks/) collection that represents all bookmarks in the range. |
| [get_Fields](./get_fields/)() | Returns a [Fields](./get_fields/) collection that represents all fields in the range. |
| [get_FormFields](./get_formfields/)() | Returns a [FormFields](./get_formfields/) collection that represents all form fields in the range. |
| [get_Revisions](./get_revisions/)() | Gets a collection of revisions (tracked changes) that exist in this range. |
| [get_StructuredDocumentTags](./get_structureddocumenttags/)() | Returns a [StructuredDocumentTags](./get_structureddocumenttags/) collection that represents all structured document tags in the range. |
| [get_Text](./get_text/)() | Gets the text of the range. |
| [GetEnumerator](./getenumerator/)() override |  |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [NormalizeFieldTypes](./normalizefieldtypes/)() | Changes field type values [FieldType](../../aspose.words.fields/fieldchar/get_fieldtype/) of [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/) in this range so that they correspond to the field types contained in the field codes. |
| [Replace](./replace/)(const System::String\&, const System::String\&) | Replaces all occurrences of a specified character string pattern with a replacement string. |
| [Replace](./replace/)(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Replaces all occurrences of a character pattern specified by a regular expression with another string. |
| [Replace](./replace/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Replaces all occurrences of a specified character string pattern with a replacement string. |
| [Replace](./replace/)(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) | Replaces all occurrences of a character pattern specified by a regular expression with another string. |
| [ToDocument](./todocument/)() | Constructs a new fully formed document that contains the range. |
| static [Type](./type/)() |  |
| [UnlinkFields](./unlinkfields/)() | Unlinks fields in this range. |
| [UpdateFields](./updatefields/)() | Updates the values of document fields in this range. |
## Remarks


The document is represented by a tree of nodes and the nodes provide operations to work with the tree, but some operations are easier to perform if the document is treated as a contiguous sequence of text.

[Range](./) is a "facade" interface that provide methods that treat the document or portions of the document as "flat" text regardless of the fact that the document nodes are stored in a tree-like object model.

[Range](./) does not contain any text or nodes, it is merely a view or "window" over a fragment of a document.

## Examples



Shows how to get the text contents of all the nodes that a range covers. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Write(u"Hello world!");

ASSERT_EQ(u"Hello world!", doc->get_Range()->get_Text().Trim());
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
