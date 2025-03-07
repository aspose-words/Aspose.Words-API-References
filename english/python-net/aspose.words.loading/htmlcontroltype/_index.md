---
title: HtmlControlType enumeration
linktitle: HtmlControlType enumeration
articleTitle: HtmlControlType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.loading.HtmlControlType enumeration. Type of document nodes that represent <input> and <select> elements imported from HTML."
type: docs
weight: 60
url: /python-net/aspose.words.loading/htmlcontroltype/
---

## HtmlControlType enumeration

Type of document nodes that represent \<input\> and \<select\> elements imported from HTML.


### Members

| Name | Description |
| --- | --- |
| FORM_FIELD | A form field. |
| STRUCTURED_DOCUMENT_TAG | A structured document tag |

### Examples

Shows how to set preferred type of document nodes that will represent imported \<input\> and \<select\> elements.

```python
html = "\n                <html>\n                    <select name='ComboBox' size='1'>\n                        <option value='val1'>item1</option>\n                        <option value='val2'></option>\n                    </select>\n                </html>\n            "
html_load_options = aw.loading.HtmlLoadOptions()
html_load_options.preferred_control_type = aw.loading.HtmlControlType.STRUCTURED_DOCUMENT_TAG
doc = aw.Document(stream=io.BytesIO(system_helper.text.Encoding.get_bytes(html, system_helper.text.Encoding.utf_8())), load_options=html_load_options)
nodes = doc.get_child_nodes(aw.NodeType.STRUCTURED_DOCUMENT_TAG, True)
tag = nodes[0].as_structured_document_tag()
```

### See Also

* module [aspose.words.loading](../)

