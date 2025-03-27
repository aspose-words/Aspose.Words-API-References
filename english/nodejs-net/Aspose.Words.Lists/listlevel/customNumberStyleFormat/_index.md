---
title: ListLevel.customNumberStyleFormat property
linktitle: customNumberStyleFormat property
articleTitle: customNumberStyleFormat property
second_title: Aspose.Words for NodeJs
description: "ListLevel.customNumberStyleFormat property. Gets or sets the custom number style format for this list level"
type: docs
weight: 20
url: /nodejs-net/Aspose.Words.Lists/listlevel/customNumberStyleFormat/
---

## ListLevel.customNumberStyleFormat property

Gets or sets the custom number style format for this list level. For example: "a, ç, ĝ, ...".


```js
get customNumberStyleFormat(): string
```

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

Shows how to set customer number style format.

```js
let doc = new aw.Document(base.myDir + "List with leading zero.docx");

doc.updateListLabels();

let paras = doc.firstSection.body.paragraphs;
expect(paras.at(0).listLabel.labelString).toEqual("001.");
expect(paras.at(1).listLabel.labelString).toEqual("0001.");
expect(paras.at(2).listLabel.labelString).toEqual("0002.");

paras.at(1).listFormat.listLevel.customNumberStyleFormat = "001, 002, 003, ...";

doc.updateListLabels();

expect(paras.at(0).listLabel.labelString).toEqual("001.");
expect(paras.at(1).listLabel.labelString).toEqual("001.");
expect(paras.at(2).listLabel.labelString).toEqual("002.");
```

### See Also

* module [Aspose.Words.Lists](../../)
* class [ListLevel](../)

