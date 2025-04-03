---
title: Style.semiHidden property
linktitle: semiHidden property
articleTitle: semiHidden property
second_title: Aspose.Words for NodeJs
description: "Style.semiHidden property. Gets/sets whether the style hides from the Styles gallery and from the Styles task pane."
type: docs
weight: 170
url: /nodejs-net/aspose.words/style/semiHidden/
---

## Style.semiHidden property

Gets/sets whether the style hides from the Styles gallery and from the Styles task pane.


```js
get semiHidden(): boolean
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

