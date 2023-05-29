---
title: LanguagePreferences.default_editing_language property
linktitle: default_editing_language property
articleTitle: default_editing_language property
second_title: Aspose.Words for Python
description: "LanguagePreferences.default_editing_language property. Gets or sets default editing language."
type: docs
weight: 20
url: /python-net/aspose.words.loading/languagepreferences/default_editing_language/
---

## LanguagePreferences.default_editing_language property

Gets or sets default editing language.

The default value is Aspose.Words.Loading.EditingLanguage.EnglishUS.




### Examples

Shows how set a default language when loading a document.

```python
load_options = aw.loading.LoadOptions()
load_options.language_preferences.default_editing_language = aw.loading.EditingLanguage.RUSSIAN

doc = aw.Document(MY_DIR + "No default editing language.docx", load_options)

locale_id = doc.styles.default_font.locale_id
if locale_id == aw.loading.EditingLanguage.RUSSIAN:
    print("The document either has no any language set in defaults or it was set to Russian originally.")
else:
    print("The document default language was set to another than Russian language originally, so it is not overridden.")
```

### See Also

* module [aspose.words.loading](../../)
* class [LanguagePreferences](../)

