---
title: HtmlLoadOptions.ignoreNoscriptElements property
linktitle: ignoreNoscriptElements property
articleTitle: ignoreNoscriptElements property
second_title: Aspose.Words for NodeJs
description: "HtmlLoadOptions.ignoreNoscriptElements property. Gets or sets a value indicating whether to ignore <noscript> HTML elements"
type: docs
weight: 40
url: /nodejs-net/aspose.words.loading/htmlloadoptions/ignoreNoscriptElements/
---

## HtmlLoadOptions.ignoreNoscriptElements property

Gets or sets a value indicating whether to ignore \<noscript\> HTML elements.
Default value is ``false``.



```js
get ignoreNoscriptElements(): boolean
```

### Remarks

Like MS Word, Aspose.Words does not support scripts and by default loads content of \<noscript\> elements
into the resulting document. In most browsers, however, scripts are supported and content from \<noscript\>
is not visible. Setting this property to ``true`` forces Aspose.Words to ignore all \<noscript\> elements
and helps to produce documents that look closer to what is seen in browsers.



### See Also

* module [Aspose.Words.Loading](../../)
* class [HtmlLoadOptions](../)

