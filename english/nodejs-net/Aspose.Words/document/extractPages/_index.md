---
title: Document.extractPages method
linktitle: extractPages method
articleTitle: extractPages method
second_title: Aspose.Words for Node.js
description: "Document.extractPages method. Returns the [Document](../) object representing specified range of pages."
type: docs
weight: 600
url: /nodejs-net/aspose.words/document/extractPages/
---

## extractPages(index, count) {#number_number}

Returns the [Document](../) object representing specified range of pages.



```js
extractPages(index: number, count: number)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | number | The zero-based index of the first page to extract. |
| count | number | Number of pages to be extracted. |

### Remarks

The resulting document should look like the one in MS Word, as if we had performed 'Print specific pages' – the numbering,
headers/footers and cross tables layout will be preserved.
But due to a large number of nuances, appearing while reducing the number of pages, full match of the layout is a quiet complicated task requiring a lot of effort.
Depending on the document complexity there might be slight differences in the resulting document contents layout comparing to the source document.
Any feedback would be greatly appreciated.


### See Also

* module [Aspose.Words](../../)
* class [Document](../)

