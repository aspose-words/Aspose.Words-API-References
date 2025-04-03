---
title: LanguagePreferences.addEditingLanguage method
linktitle: addEditingLanguage method
articleTitle: addEditingLanguage method
second_title: Aspose.Words for NodeJs
description: "LanguagePreferences.addEditingLanguage method. Adds additional editing language."
type: docs
weight: 30
url: /nodejs-net/aspose.words.loading/languagepreferences/addEditingLanguage/
---

## addEditingLanguage(language) {#editinglanguage}

Adds additional editing language.


```js
addEditingLanguage(language: Aspose.Words.Loading.EditingLanguage)
```

| Parameter | Type | Description |
| --- | --- | --- |
| language | [EditingLanguage](../../editinglanguage/) |  |

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

* module [Aspose.Words.Loading](../../)
* class [LanguagePreferences](../)

