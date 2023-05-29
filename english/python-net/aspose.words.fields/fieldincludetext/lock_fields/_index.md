---
title: FieldIncludeText.lock_fields property
linktitle: lock_fields property
articleTitle: lock_fields property
second_title: Aspose.Words for Python
description: "FieldIncludeText.lock_fields property. Gets or sets whether to prevent fields in the included document from being updated."
type: docs
weight: 40
url: /python-net/aspose.words.fields/fieldincludetext/lock_fields/
---

## FieldIncludeText.lock_fields property

Gets or sets whether to prevent fields in the included document from being updated.


### Examples

Shows how to create an INCLUDETEXT field, and set its properties.

```python
def test_field_include_text(self):

    doc = aw.Document()
    builder = aw.DocumentBuilder(doc)

    # Below are two ways to use INCLUDETEXT fields to display the contents of an XML file in the local file system.
    # 1 -  Perform an XSL transformation on an XML document:
    field_include_text = ExField.create_field_include_text(builder, MY_DIR + "CD collection data.xml", False, "text/xml", "XML", "ISO-8859-1")
    field_include_text.xsl_transformation = MY_DIR + "CD collection XSL transformation.xsl"

    builder.writeln()

    # 2 -  Use an XPath to take specific elements from an XML document:
    field_include_text = ExField.create_field_include_text(builder, MY_DIR + "CD collection data.xml", False, "text/xml", "XML", "ISO-8859-1")
    field_include_text.namespace_mappings = "xmlns:n='myNamespace'"
    field_include_text.xpath = "/catalog/cd/title"

    doc.update_fields()
    doc.save(ARTIFACTS_DIR + "Field.field_include_text.docx")

@staticmethod
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

* module [aspose.words.fields](../../)
* class [FieldIncludeText](../)

