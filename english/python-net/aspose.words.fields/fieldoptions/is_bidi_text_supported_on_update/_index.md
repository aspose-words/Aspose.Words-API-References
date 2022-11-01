---
title: is_bidi_text_supported_on_update property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the value indicating whether bidirectional text is fully supported during field update or not."
type: docs
weight: 140
url: /python-net/aspose.words.fields/fieldoptions/is_bidi_text_supported_on_update/
---

## FieldOptions.is_bidi_text_supported_on_update property

Gets or sets the value indicating whether bidirectional text is fully supported during field update or not.

When this property is set to ``True``, additional steps are performed to produce Right-To-Left language
(i.e. Arabic or Hebrew) compatible field result during its update.

When this property is set to ``False`` and Right-To-Left language is used, correctness of field result
after its update is not guaranteed.

The default value is ``False``.




### Examples

Shows how to use FieldOptions to ensure that field updating fully supports bi-directional text.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Ensure that any field operation involving right-to-left text is performs as expected.
doc.field_options.is_bidi_text_supported_on_update = True

# Use a document builder to insert a field that contains the right-to-left text.
combo_box = builder.insert_combo_box("MyComboBox", ["עֶשְׂרִים", "שְׁלוֹשִׁים", "אַרְבָּעִים", "חֲמִשִּׁים", "שִׁשִּׁים"], 0)
combo_box.calculate_on_exit = True

doc.update_fields()
doc.save(ARTIFACTS_DIR + "FieldOptions.bidi.docx")
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldOptions](../)

