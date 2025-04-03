---
title: ListLevel.getEffectiveValue method
linktitle: getEffectiveValue method
articleTitle: getEffectiveValue method
second_title: Aspose.Words for NodeJs
description: "ListLevel.getEffectiveValue method. Reports the string representation of the [ListLevel](../) object for the specified index of the list item"
type: docs
weight: 180
url: /nodejs-net/Aspose.Words.Lists/listlevel/getEffectiveValue/
---

## getEffectiveValue(index, numberStyle, customNumberStyleFormat) {#number_numberstyle_string}

Reports the string representation of the [ListLevel](../) object for the specified index
of the list item. Parameters specify the [NumberStyle](../../../aspose.words/numberstyle/) and an optional format string
used when [NumberStyle.Custom](../../../aspose.words/numberstyle/#Custom) is specified.



```js
getEffectiveValue(index: numbernumberStyle: Aspose.Words.NumberStylecustomNumberStyleFormat: string)
```

| Parameter | Type | Description |
| --- | --- | --- |
| index | number | The index of the list item (must be in the range from 1 to 32767). |
| numberStyle | [NumberStyle](../../../aspose.words/numberstyle/) | The [NumberStyle](../../../aspose.words/numberstyle/) of the [ListLevel](../) object. |
| customNumberStyleFormat | string | The optional format string used when [NumberStyle.Custom](../../../aspose.words/numberstyle/#Custom) is specified (e.g. "a, ç, ĝ, ..."). In other cases, this parameter must be ``null`` or empty. |

### Returns

The string representation of the [ListLevel](../) object, described by the *numberStyle* parameter and
the*customNumberStyleFormat* parameter, in the list item at the position determined by the*index* parameter.


### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentException)) | *customNumberStyleFormat* is``null`` or empty when the *numberStyle* is custom.-or-*customNumberStyleFormat* is not``null`` or empty when the *numberStyle* is non-custom.-or-*customNumberStyleFormat* is invalid. |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | index is out of range. |

### Examples

Shows how to get the format for a list with the custom number style.

```js
let doc = new aw.Document(base.myDir + "List with leading zero.docx");

let listLevel = doc.firstSection.body.paragraphs.at(0).listFormat.listLevel;

let customNumberStyleFormat = '';

if (listLevel.numberStyle == aw.NumberStyle.Custom)
  customNumberStyleFormat = listLevel.customNumberStyleFormat;

expect(customNumberStyleFormat).toEqual("001, 002, 003, ...");

// We can get value for the specified index of the list item.
expect(aw.Lists.ListLevel.getEffectiveValue(4, aw.NumberStyle.LowercaseRoman, null)).toEqual("iv");
expect(aw.Lists.ListLevel.getEffectiveValue(5, aw.NumberStyle.Custom, customNumberStyleFormat)).toEqual("005");
```

### See Also

* module [Aspose.Words.Lists](../../)
* class [ListLevel](../)

