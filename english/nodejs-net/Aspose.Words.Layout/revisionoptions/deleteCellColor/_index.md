---
title: RevisionOptions.deleteCellColor property
linktitle: deleteCellColor property
articleTitle: deleteCellColor property
second_title: Aspose.Words for Node.js
description: "RevisionOptions.deleteCellColor property. Allows to specify the color to be used for deleted cells [RevisionType.Deletion](../../../aspose.words/revisiontype/#Deletion)"
type: docs
weight: 20
url: /nodejs-net/aspose.words.layout/revisionoptions/deleteCellColor/
---

## RevisionOptions.deleteCellColor property

Allows to specify the color to be used for deleted cells [RevisionType.Deletion](../../../aspose.words/revisiontype/#Deletion).
Default value is [RevisionColor.Pink](../../revisioncolor/#Pink).



```js
get deleteCellColor(): Aspose.Words.Layout.RevisionColor
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

