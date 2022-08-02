---
title: flat_opc_xml_mapping_only property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets value determining which document formats are allowed to be mapped by [StructuredDocumentTag.xml_mapping](../../../aspose.words.markup/structureddocumenttag/xml_mapping/)"
type: docs
weight: 70
url: /python-net/aspose.words.saving/saveoptions/flat_opc_xml_mapping_only/
---

## SaveOptions.flat_opc_xml_mapping_only property

Gets or sets value determining which document formats are allowed to be mapped by [StructuredDocumentTag.xml_mapping](../../../aspose.words.markup/structureddocumenttag/xml_mapping/).
By default only [LoadFormat.FLAT_OPC](../../../aspose.words/loadformat/#FLAT_OPC) document format is allowed to be mapped.


This option is paired with [LoadOptions.flat_opc_xml_mapping_only](../../../aspose.words.loading/loadoptions/flat_opc_xml_mapping_only/).
Typically you need set both of them to false to allow arbitrary document format mapped.



### Examples

Shows how to binding structured document tags to any format.

```python
# If True - SDT will contain raw HTML text.
# If False - mapped HTML will parsed and resulting document will be inserted into SDT content.
load_options = aw.loading.LoadOptions()
load_options.flat_opc_xml_mapping_only = is_flat_opc_xml_mapping_only
doc = aw.Document(MY_DIR + "Structured document tag with HTML content.docx", load_options)

save_options = aw.saving.SaveOptions.create_save_options(aw.SaveFormat.PDF)
save_options.flat_opc_xml_mapping_only = is_flat_opc_xml_mapping_only

doc.save(ARTIFACTS_DIR + "LoadOptions.flat_opc_xml_mapping_only.pdf", save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [SaveOptions](../)

