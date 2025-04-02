---
title: LoadOptions.languagePreferences property
linktitle: languagePreferences property
articleTitle: languagePreferences property
second_title: Aspose.Words for NodeJs
description: "LoadOptions.languagePreferences property. Gets language preferences that will be used when document is loading."
type: docs
weight: 80
url: /nodejs-net/Aspose.Words.Loading/loadoptions/languagePreferences/
---

## LoadOptions.languagePreferences property

Gets language preferences that will be used when document is loading.


```js
get languagePreferences(): Aspose.Words.Loading.LanguagePreferences
```

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
* class [LoadOptions](../)

