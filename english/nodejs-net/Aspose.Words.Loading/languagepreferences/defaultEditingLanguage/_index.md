---
title: LanguagePreferences.defaultEditingLanguage property
linktitle: defaultEditingLanguage property
articleTitle: defaultEditingLanguage property
second_title: Aspose.Words for Node.js
description: "LanguagePreferences.defaultEditingLanguage property. Gets or sets default editing language."
type: docs
weight: 20
url: /nodejs-net/aspose.words.loading/languagepreferences/defaultEditingLanguage/
---

## LanguagePreferences.defaultEditingLanguage property

Gets or sets default editing language.

The default value is EnglishUS.




```js
get defaultEditingLanguage(): Aspose.Words.Loading.EditingLanguage
```

### Examples

Shows how set a default language when loading a document.

```js
let loadOptions = new aw.Loading.LoadOptions();
loadOptions.languagePreferences.defaultEditingLanguage = aw.Loading.EditingLanguage.Russian;

let doc = new aw.Document(base.myDir + "No default editing language.docx", loadOptions);

var localeId = doc.styles.defaultFont.localeId;
console.log(localeId == aw.Loading.EditingLanguage.Russian
  ? "The document either has no any language set in defaults or it was set to Russian originally."
  : "The document default language was set to another than Russian language originally, so it is not overridden.");
```

### See Also

* module [Aspose.Words.Loading](../../)
* class [LanguagePreferences](../)

