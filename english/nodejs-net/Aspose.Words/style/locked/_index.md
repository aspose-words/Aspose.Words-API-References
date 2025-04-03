---
title: Style.locked property
linktitle: locked property
articleTitle: locked property
second_title: Aspose.Words for NodeJs
description: "Style.locked property. Specifies whether this style is locked."
type: docs
weight: 120
url: /nodejs-net/aspose.words/style/locked/
---

## Style.locked property

Specifies whether this style is locked.


```js
get locked(): boolean
```

### Examples

Shows how to lock style.

```js
let doc = new aw.Document();

let styleHeading1 = doc.styles.at(aw.StyleIdentifier.Heading1);
if (!styleHeading1.locked)            
  styleHeading1.locked = true;

doc.save(base.artifactsDir + "Styles.LockStyle.docx");
```

### See Also

* module [Aspose.Words](../../)
* class [Style](../)

