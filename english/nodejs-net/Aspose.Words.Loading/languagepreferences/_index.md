---
title: LanguagePreferences class
linktitle: LanguagePreferences class
articleTitle: LanguagePreferences class
second_title: Aspose.Words for Node.js
description: "Aspose.Words.Loading.LanguagePreferences class. Allows to set up language preferences"
type: docs
weight: 90
url: /nodejs-net/aspose.words.loading/languagepreferences/
---

## LanguagePreferences class

Allows to set up language preferences.
To learn more, visit the [Specify Load Options](https://docs.aspose.com/words/nodejs-net/specify-load-options/) documentation article.




### Remarks

Implements 'Set the Office Language Preferences' dialog in Word.


### Constructors
| Name | Description |
| --- | --- |
| [LanguagePreferences()](./constructor/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [defaultEditingLanguage](./defaultEditingLanguage/) | Gets or sets default editing language. |

### Methods

| Name | Description |
| --- | --- |
|[ addEditingLanguage(language)](./addEditingLanguage/#editinglanguage) | Adds additional editing language. |
|[ addEditingLanguages(languages)](./addEditingLanguages/#editinglanguage[]) | Adds additional editing languages. |

### Examples

Shows how to apply language preferences when loading a document.

```js
let loadOptions = new aw.Loading.LoadOptions();
loadOptions.languagePreferences.addEditingLanguage(aw.Loading.EditingLanguage.Japanese);

let doc = new aw.Document(base.myDir + "No default editing language.docx", loadOptions);

var localeIdFarEast = doc.styles.defaultFont.localeIdFarEast;
console.log(localeIdFarEast == aw.Loading.EditingLanguage.Japanese
  ? "The document either has no any FarEast language set in defaults or it was set to Japanese originally."
  : "The document default FarEast language was set to another than Japanese language originally, so it is not overridden.");
```

### See Also

* module [Aspose.Words.Loading](../)

