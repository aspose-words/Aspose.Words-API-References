---
title: language_preferences property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets language preferences that will be used when document is loading."
type: docs
weight: 80
url: /python-net/aspose.words.loading/loadoptions/language_preferences/
---

## LoadOptions.language_preferences property

Gets language preferences that will be used when document is loading.


### Examples

Shows how to apply language preferences when loading a document.

```python
load_options = aw.loading.LoadOptions()
load_options.language_preferences.add_editing_language(aw.loading.EditingLanguage.JAPANESE)

doc = aw.Document(MY_DIR + "No default editing language.docx", load_options)

locale_id_far_east = doc.styles.default_font.locale_id_far_east
if locale_id_far_east == aw.loading.EditingLanguage.JAPANESE:
    print("The document either has no any FarEast language set in defaults or it was set to Japanese originally.")
else:
    print("The document default FarEast language was set to another than Japanese language originally, so it is not overridden.")
```

### See Also

* module [aspose.words.loading](../../)
* class [LoadOptions](../)

