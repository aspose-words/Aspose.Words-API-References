---
title: HtmlLoadOptions.preferred_control_type property
linktitle: preferred_control_type property
articleTitle: preferred_control_type property
second_title: Aspose.Words for Python
description: "HtmlLoadOptions.preferred_control_type property. Gets or sets preferred type of document nodes that will represent imported <input> and <select> elements"
type: docs
weight: 50
url: /python-net/aspose.words.loading/htmlloadoptions/preferred_control_type/
---

## HtmlLoadOptions.preferred_control_type property

Gets or sets preferred type of document nodes that will represent imported \<input\> and \<select\> elements.
Default value is [HtmlControlType.FORM_FIELD](../../htmlcontroltype/#FORM_FIELD).



```python
@property
def preferred_control_type(self) -> aspose.words.loading.HtmlControlType:
    ...

@preferred_control_type.setter
def preferred_control_type(self, value: aspose.words.loading.HtmlControlType):
    ...

```

### Remarks

Please note that setting this property does not guarantee that all imported controls will be of the specified type.
If an HTML control is not representable with document nodes of the preferred type, Aspose.Words will use
a compatible [HtmlControlType](../../htmlcontroltype/) for that control.



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

* module [aspose.words.loading](../../)
* class [HtmlLoadOptions](../)

