---
title: FieldIncludeText class
linktitle: FieldIncludeText class
articleTitle: FieldIncludeText class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldIncludeText class. Implements the INCLUDETEXT field"
type: docs
weight: 590
url: /python-net/aspose.words.fields/fieldincludetext/
---

## FieldIncludeText class

Implements the INCLUDETEXT field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

Inserts all or part of the text and graphics contained in another document.


**Inheritance:** [FieldIncludeText](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldIncludeText()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [bookmark_name](./bookmark_name/) | Gets or sets the name of the bookmark in the document to include. |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [encoding](./encoding/) | Gets or sets the encoding applied to the data within the referenced file. |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [lock_fields](./lock_fields/) | Gets or sets whether to prevent fields in the included document from being updated. |
| [mime_type](./mime_type/) | Gets or sets the MIME type of the referenced file. |
| [namespace_mappings](./namespace_mappings/) | Gets or sets the namespace mappings for XPath queries. |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [source_full_name](./source_full_name/) | Gets or sets the location of the document using an IRI. |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [text_converter](./text_converter/) | Gets or sets the name of the text converter for the format of the included file. |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |
| [xpath](./xpath/) | Gets or sets XPath for the desired portion of the XML file. |
| [xsl_transformation](./xsl_transformation/) | Gets or sets the location of XSL Transformation to format XML data. |

### Methods

| Name | Description |
| --- | --- |
|[ get_field_code()](../field/get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.<br>(Inherited from [Field](../field/)) |
|[ get_field_code(include_child_field_codes)](../field/get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator).<br>(Inherited from [Field](../field/)) |
|[ remove()](../field/remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns ``None``.<br>(Inherited from [Field](../field/)) |
|[ unlink()](../field/unlink/#default) | Performs the field unlink.<br>(Inherited from [Field](../field/)) |
|[ update()](../field/update/#default) | Performs the field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update(ignore_merge_format)](../field/update/#bool) | Performs a field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |

### Examples

Shows how to create an INCLUDETEXT field, and set its properties.

```python
def field_include_text():
    doc = aw.Document()
    builder = aw.DocumentBuilder(doc)
    # Below are two ways to use INCLUDETEXT fields to display the contents of an XML file in the local file system.
    # 1 -  Perform an XSL transformation on an XML document:
    field_include_text = create_field_include_text(builder, MY_DIR + 'CD collection data.xml', False, 'text/xml', 'XML', 'ISO-8859-1')
    field_include_text.xsl_transformation = MY_DIR + 'CD collection XSL transformation.xsl'
    builder.writeln()
    # 2 -  Use an XPath to take specific elements from an XML document:
    field_include_text = create_field_include_text(builder, MY_DIR + 'CD collection data.xml', False, 'text/xml', 'XML', 'ISO-8859-1')
    field_include_text.namespace_mappings = "xmlns:n='myNamespace'"
    field_include_text.xpath = '/catalog/cd/title'
    doc.update_fields()
    doc.save(ARTIFACTS_DIR + 'Field.field_include_text.docx')

def create_field_include_text(builder: aw.DocumentBuilder, source_full_name: str, lock_fields: bool, mime_type: str, text_converter: str, encoding: str) -> aw.fields.FieldIncludeText:
    """Use a document builder to insert an INCLUDETEXT field with custom properties."""
    field_include_text = builder.insert_field(aw.fields.FieldType.FIELD_INCLUDE_TEXT, True).as_field_include_text()
    field_include_text.source_full_name = source_full_name
    field_include_text.lock_fields = lock_fields
    field_include_text.mime_type = mime_type
    field_include_text.text_converter = text_converter
    field_include_text.encoding = encoding
    return field_include_text
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

