﻿---
title: RevisionOptions.revisedPropertiesEffect property
linktitle: revisedPropertiesEffect property
articleTitle: revisedPropertiesEffect property
second_title: Aspose.Words for Node.js
description: "RevisionOptions.revisedPropertiesEffect property. Allows to specify the effect for content areas with changes of formatting properties [RevisionType.FormatChange](../../../aspose.words/revisiontype/#FormatChange) Default value is [RevisionTextEffect.None](../../revisiontexteffect/#None)"
type: docs
weight: 140
url: /nodejs-net/aspose.words.layout/revisionoptions/revisedPropertiesEffect/
---

## RevisionOptions.revisedPropertiesEffect property

Allows to specify the effect for content areas with changes of formatting properties [RevisionType.FormatChange](../../../aspose.words/revisiontype/#FormatChange)
Default value is [RevisionTextEffect.None](../../revisiontexteffect/#None)



```js
get revisedPropertiesEffect(): Aspose.Words.Layout.RevisionTextEffect
```

### Exceptions

| exception | condition |
| --- | --- |
| RuntimeError (Proxy error(ArgumentOutOfRangeException)) | [RevisionTextEffect.Hidden](../../revisiontexteffect/#Hidden) is not allowed. |

### Examples

Shows how to modify the appearance of revisions.

```js
let doc = new aw.Document(base.myDir + "Revisions.docx");

// Get the RevisionOptions object that controls the appearance of revisions.
let revisionOptions = doc.layoutOptions.revisionOptions;

// Render insertion revisions in green and italic.
revisionOptions.insertedTextColor = aw.Layout.RevisionColor.Green;
revisionOptions.insertedTextEffect = aw.Layout.RevisionTextEffect.Italic;

// Render deletion revisions in red and bold.
revisionOptions.deletedTextColor = aw.Layout.RevisionColor.Red;
revisionOptions.deletedTextEffect = aw.Layout.RevisionTextEffect.Bold;

// The same text will appear twice in a movement revision:
// once at the departure point and once at the arrival destination.
// Render the text at the moved-from revision yellow with a double strike through
// and double-underlined blue at the moved-to revision.
revisionOptions.movedFromTextColor = aw.Layout.RevisionColor.Yellow;
revisionOptions.movedFromTextEffect = aw.Layout.RevisionTextEffect.DoubleStrikeThrough;
revisionOptions.movedToTextColor = aw.Layout.RevisionColor.ClassicBlue;
revisionOptions.movedToTextEffect = aw.Layout.RevisionTextEffect.DoubleUnderline;

// Render format revisions in dark red and bold.
revisionOptions.revisedPropertiesColor = aw.Layout.RevisionColor.DarkRed;
revisionOptions.revisedPropertiesEffect = aw.Layout.RevisionTextEffect.Bold;

// Place a thick dark blue bar on the left side of the page next to lines affected by revisions.
revisionOptions.revisionBarsColor = aw.Layout.RevisionColor.DarkBlue;
revisionOptions.revisionBarsWidth = 15.0f;

// Show revision marks and original text.
revisionOptions.showOriginalRevision = true;
revisionOptions.showRevisionMarks = true;

// Get movement, deletion, formatting revisions, and comments to show up in green balloons
// on the right side of the page.
revisionOptions.showInBalloons = aw.Layout.ShowInBalloons.Format;
revisionOptions.commentColor = aw.Layout.RevisionColor.BrightGreen;

// These features are only applicable to formats such as .pdf or .jpg.
doc.save(base.artifactsDir + "Revision.revisionOptions.pdf");
```

### See Also

* module [Aspose.Words.Layout](../../)
* class [RevisionOptions](../)

