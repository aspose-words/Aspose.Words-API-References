---
title: LanguagePreferences class
second_title: Aspose.Words for Python via .NET API Reference
description: "Allows to set up language preferences"
type: docs
weight: 100
url: /python-net/aspose.words.loading/languagepreferences/
---

## LanguagePreferences class

Allows to set up language preferences.
To learn more, visit the [Specify Load Options](https://docs.aspose.com/words/net/specify-load-options/) documentation article.




Implements 'Set the Office Language Preferences' dialog in Word.


### Constructors
| Name | Description |
| --- | --- |
| [LanguagePreferences()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [default_editing_language](./default_editing_language/) | Gets or sets default editing language. |

### Methods

| Name | Description |
| --- | --- |
|[ add_editing_language(language)](./add_editing_language/#editinglanguage) | Adds additional editing language. |
|[ add_editing_languages(languages)](./add_editing_languages/#editinglanguagelist) | Adds additional editing languages. |

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

* module [aspose.words.loading](../)

