﻿---
title: BuiltInDocumentProperties class
second_title: Aspose.Words for Python via .NET API Reference
description: "A collection of built-in document properties"
type: docs
weight: 10
url: /python-net/aspose.words.properties/builtindocumentproperties/
---

## BuiltInDocumentProperties class

A collection of built-in document properties.
To learn more, visit the [Work with Document Properties](https://docs.aspose.com/words/python-net/work-with-document-properties/) documentation article.




Provides access to [DocumentProperty](../documentproperty/) objects by their names (using an indexer) and
via a set of typed properties that return values of appropriate types.




The names of the properties are case-insensitive.

The properties in the collection are sorted alphabetically by name.




**Inheritance:** [BuiltInDocumentProperties](./) → [DocumentPropertyCollection](../documentpropertycollection/)

### Indexers

| Name | Description |
| --- | --- |
| [``__getitem__(index)``](./__getitem__/#int) |  |

### Properties

| Name | Description |
| --- | --- |
| [author](./author/) | Gets or sets the name of the document's author. |
| [bytes](./bytes/) | Represents an estimate of the number of bytes in the document. |
| [category](./category/) | Gets or sets the category of the document. |
| [characters](./characters/) | Represents an estimate of the number of characters in the document. |
| [characters_with_spaces](./characters_with_spaces/) | Represents an estimate of the number of characters (including spaces) in the document. |
| [comments](./comments/) | Gets or sets the document comments. |
| [company](./company/) | Gets or sets the company property. |
| [content_status](./content_status/) | Gets or sets the Aspose.Words.Properties.PropertyName.ContentStatus of the document. |
| [content_type](./content_type/) | Gets or sets the Aspose.Words.Properties.PropertyName.ContentType of the document. |
| [count](../documentpropertycollection/count/) | Gets number of items in the collection.<br>(Inherited from [DocumentPropertyCollection](../documentpropertycollection/)) |
| [created_time](./created_time/) | Gets or sets date of the document creation in UTC. |
| [heading_pairs](./heading_pairs/) | Specifies document headings and their names. |
| [hyperlink_base](./hyperlink_base/) | Specifies the base string used for evaluating relative hyperlinks in this document. |
| [keywords](./keywords/) | Gets or sets the document keywords. |
| [last_printed](./last_printed/) | Gets or sets the date when the document was last printed in UTC. |
| [last_saved_by](./last_saved_by/) | Gets or sets the name of the last author. |
| [last_saved_time](./last_saved_time/) | Gets or sets the time of the last save in UTC. |
| [lines](./lines/) | Represents an estimate of the number of lines in the document. |
| [links_up_to_date](./links_up_to_date/) | Indicates whether hyperlinks in a document are up-to-date. |
| [manager](./manager/) | Gets or sets the manager property. |
| [name_of_application](./name_of_application/) | Gets or sets the name of the application. |
| [pages](./pages/) | Represents an estimate of the number of pages in the document. |
| [paragraphs](./paragraphs/) | Represents an estimate of the number of paragraphs in the document. |
| [revision_number](./revision_number/) | Gets or sets the document revision number. |
| [security](./security/) | Specifies the security level of a document as a numeric value. |
| [subject](./subject/) | Gets or sets the subject of the document. |
| [template](./template/) | Gets or sets the informational name of the document template. |
| [thumbnail](./thumbnail/) | Gets or sets the thumbnail of the document. |
| [title](./title/) | Gets or sets the title of the document. |
| [titles_of_parts](./titles_of_parts/) | Each string in the array specifies the name of a part in the document. |
| [total_editing_time](./total_editing_time/) | Gets or sets the total editing time in minutes. |
| [version](./version/) | Represents the version number of the application that created the document. |
| [words](./words/) | Represents an estimate of the number of words in the document. |

### Methods

| Name | Description |
| --- | --- |
|[ clear()](../documentpropertycollection/clear/#default) | Removes all properties from the collection.<br>(Inherited from [DocumentPropertyCollection](../documentpropertycollection/)) |
|[ contains(name)](../documentpropertycollection/contains/#str) | Returns ``True`` if a property with the specified name exists in the collection.<br>(Inherited from [DocumentPropertyCollection](../documentpropertycollection/)) |
|[ get_by_name(name)](../documentpropertycollection/get_by_name/#str) | Returns a [DocumentProperty](../documentproperty/) object by the name of the property.<br>(Inherited from [DocumentPropertyCollection](../documentpropertycollection/)) |
|[ index_of(name)](../documentpropertycollection/index_of/#str) | Gets the index of a property by name.<br>(Inherited from [DocumentPropertyCollection](../documentpropertycollection/)) |
|[ remove(name)](../documentpropertycollection/remove/#str) | Removes a property with the specified name from the collection.<br>(Inherited from [DocumentPropertyCollection](../documentpropertycollection/)) |
|[ remove_at(index)](../documentpropertycollection/remove_at/#int) | Removes a property at the specified index.<br>(Inherited from [DocumentPropertyCollection](../documentpropertycollection/)) |

### Examples

Shows how to work with built-in document properties.

```python
doc = aw.Document(MY_DIR + "Properties.docx")

# The "Document" object contains some of its metadata in its members.
print(f"Document filename:\n\t \"{doc.original_file_name}\"")

# The document also stores metadata in its built-in properties.
# Each built-in property is a member of the document's "BuiltInDocumentProperties" object.
print("Built-in Properties:")
for doc_property in doc.built_in_document_properties:
    print(doc_property.name)
    print(f"\tType:\t{doc_property.type}")

    # Some properties may store multiple values.
    if isinstance(doc_property.value, list):
        for value in doc_property.value:
            print(f"\tValue:\t\"{value}\"")
    else:
        print(f"\tValue:\t\"{doc_property.value}\"")
```

### See Also

* module [aspose.words.properties](../)
* class [DocumentPropertyCollection](../documentpropertycollection/)
* class [Document](../../aspose.words/document/)
* property [Document.built_in_document_properties](../../aspose.words/document/built_in_document_properties/)
* property [Document.custom_document_properties](../../aspose.words/document/custom_document_properties/)

