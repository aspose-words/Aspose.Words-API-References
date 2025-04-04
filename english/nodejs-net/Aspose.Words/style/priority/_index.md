---
title: Style.priority property
linktitle: priority property
articleTitle: priority property
second_title: Aspose.Words for Node.js
description: "Style.priority property. Gets/sets the integer value that represents the priority for sorting the styles in the Styles task pane."
type: docs
weight: 160
url: /nodejs-net/aspose.words/style/priority/
---

## Style.priority property

Gets/sets the integer value that represents the priority for sorting the styles in the Styles task pane.


```js
get priority(): number
```

### Examples

Shows how to prioritize and hide a style.

```js
let doc = new aw.Document();
let styleTitle = doc.styles.at(aw.StyleIdentifier.Subtitle);

if (styleTitle.priority == 9)
  styleTitle.priority = 10;

if (!styleTitle.unhideWhenUsed)
  styleTitle.unhideWhenUsed = true;

if (styleTitle.semiHidden)
  styleTitle.semiHidden = true;

doc.save(base.artifactsDir + "Styles.StylePriority.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Style](../)

