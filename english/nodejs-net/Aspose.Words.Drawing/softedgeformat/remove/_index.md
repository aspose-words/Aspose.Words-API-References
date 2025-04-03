---
title: SoftEdgeFormat.remove method
linktitle: remove method
articleTitle: remove method
second_title: Aspose.Words for NodeJs
description: "SoftEdgeFormat.remove method. Removes [SoftEdgeFormat](../) from the parent object."
type: docs
weight: 20
url: /nodejs-net/aspose.words.drawing/softedgeformat/remove/
---

## remove() {#default}

Removes [SoftEdgeFormat](../) from the parent object.



```js
remove()
```

### Examples

Shows how to set limit for image resolution.

```js
let doc = new aw.Document(base.myDir + "Rendering.docx");

let saveOptions = new aw.Saving.SvgSaveOptions();
saveOptions.maxImageResolution = 72;

doc.save(base.artifactsDir + "SvgSaveOptions.maxImageResolution.svg", saveOptions);
```

### See Also

* module [Aspose.Words.Drawing](../../)
* class [SoftEdgeFormat](../)

