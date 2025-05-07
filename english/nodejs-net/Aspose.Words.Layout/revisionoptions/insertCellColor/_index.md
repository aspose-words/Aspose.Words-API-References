---
title: RevisionOptions.insertCellColor property
linktitle: insertCellColor property
articleTitle: insertCellColor property
second_title: Aspose.Words for Node.js
description: "RevisionOptions.insertCellColor property. Allows to specify the color to be used for inserted cells [RevisionType.Insertion](../../../aspose.words/revisiontype/#Insertion)"
type: docs
weight: 50
url: /nodejs-net/aspose.words.layout/revisionoptions/insertCellColor/
---

## RevisionOptions.insertCellColor property

Allows to specify the color to be used for inserted cells [RevisionType.Insertion](../../../aspose.words/revisiontype/#Insertion).
Default value is [RevisionColor.Blue](../../revisioncolor/#Blue).



```js
get insertCellColor(): Aspose.Words.Layout.RevisionColor
```

### Examples

Shows how to work with insert/delete cell revision color.

```js
let doc = new aw.Document(base.myDir + "Cell revisions.docx");

doc.layoutOptions.revisionOptions.insertCellColor = aw.Layout.RevisionColor.LightBlue;
doc.layoutOptions.revisionOptions.deleteCellColor = aw.Layout.RevisionColor.DarkRed;

doc.save(base.artifactsDir + "Revision.RevisionCellColor.pdf");
```

### See Also

* module [Aspose.Words.Layout](../../)
* class [RevisionOptions](../)

