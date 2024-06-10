---
title: LanguagePreferences.add_editing_language method
linktitle: add_editing_language method
articleTitle: add_editing_language method
second_title: Aspose.Words for Python
description: "LanguagePreferences.add_editing_language method. Adds additional editing language."
type: docs
weight: 30
url: /python-net/aspose.words.loading/languagepreferences/add_editing_language/
---

## add_editing_language(language) {#editinglanguage}

Adds additional editing language.


```python
def add_editing_language(self, language: aspose.words.loading.EditingLanguage):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| language | [EditingLanguage](../../editinglanguage/) |  |

### Examples

Shows how to apply language preferences when loading a document.

```python
load_options = aw.loading.LoadOptions()
load_options.language_preferences.add_editing_language(aw.loading.EditingLanguage.JAPANESE)
doc = aw.Document(MY_DIR + 'No default editing language.docx', load_options)
locale_id_far_east = doc.styles.default_font.locale_id_far_east
if locale_id_far_east == aw.loading.EditingLanguage.JAPANESE:
    print('The document either has no any FarEast language set in defaults or it was set to Japanese originally.')
else:
    print('The document default FarEast language was set to another than Japanese language originally, so it is not overridden.')
```

### See Also

* module [aspose.words.loading](../../)
* class [LanguagePreferences](../)

