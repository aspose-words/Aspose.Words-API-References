---
title: HtmlLoadOptions.preferredControlType property
linktitle: preferredControlType property
articleTitle: preferredControlType property
second_title: Aspose.Words for NodeJs
description: "HtmlLoadOptions.preferredControlType property. Gets or sets preferred type of document nodes that will represent imported <input> and <select> elements"
type: docs
weight: 50
url: /nodejs-net/aspose.words.loading/htmlloadoptions/preferredControlType/
---

## HtmlLoadOptions.preferredControlType property

Gets or sets preferred type of document nodes that will represent imported \<input\> and \<select\> elements.
Default value is [HtmlControlType.FormField](../../htmlcontroltype/#FormField).



```js
get preferredControlType(): Aspose.Words.Loading.HtmlControlType
```

### Remarks

Please note that setting this property does not guarantee that all imported controls will be of the specified type.
If an HTML control is not representable with document nodes of the preferred type, Aspose.Words will use
a compatible [HtmlControlType](../../htmlcontroltype/) for that control.



### See Also

* module [Aspose.Words.Loading](../../)
* class [HtmlLoadOptions](../)

