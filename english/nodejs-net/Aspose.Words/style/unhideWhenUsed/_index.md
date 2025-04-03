---
title: Style.unhideWhenUsed property
linktitle: unhideWhenUsed property
articleTitle: unhideWhenUsed property
second_title: Aspose.Words for NodeJs
description: "Style.unhideWhenUsed property. Gets/sets whether the style used in the current document unhides from the Styles gallery and from the Styles task pane"
type: docs
weight: 210
url: /nodejs-net/aspose.words/style/unhideWhenUsed/
---

## Style.unhideWhenUsed property

Gets/sets whether the style used in the current document unhides from the Styles gallery and from the Styles task pane.
True when the used style should be shown in the Styles gallery.


```js
get unhideWhenUsed(): boolean
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

