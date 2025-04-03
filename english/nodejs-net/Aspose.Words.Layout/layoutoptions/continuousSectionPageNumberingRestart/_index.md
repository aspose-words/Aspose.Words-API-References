---
title: LayoutOptions.continuousSectionPageNumberingRestart property
linktitle: continuousSectionPageNumberingRestart property
articleTitle: continuousSectionPageNumberingRestart property
second_title: Aspose.Words for NodeJs
description: "LayoutOptions.continuousSectionPageNumberingRestart property. Gets or sets the mode of behavior for computing page numbers when a continuous section restarts the page numbering."
type: docs
weight: 40
url: /nodejs-net/aspose.words.layout/layoutoptions/continuousSectionPageNumberingRestart/
---

## LayoutOptions.continuousSectionPageNumberingRestart property

Gets or sets the mode of behavior for computing page numbers when a continuous section
restarts the page numbering.


```js
get continuousSectionPageNumberingRestart(): Aspose.Words.Layout.ContinuousSectionRestart
```

### Remarks

The default value is [ContinuousSectionRestart.Always](../../continuoussectionrestart/#Always).
It matches the behavior of MS Word 2019 which was the latest version at the moment the option was introduced.
Older page numbering logic demonstrated by MS Word 2016 is available via this option.
Please [ContinuousSectionRestart](../../continuoussectionrestart/) for the behavior description.



### Examples

Shows how to control page numbering in a continuous section.

```js
let doc = new aw.Document(base.myDir + "Continuous section page numbering.docx");

// By default Aspose.words behavior matches the Microsoft Word 2019.
// If you need old Aspose.words behavior, repetitive Microsoft Word 2016, use 'ContinuousSectionRestart.FromNewPageOnly'.
// Page numbering restarts only if there is no other content before the section on the page where the section starts,
// because of that the numbering will reset to 2 from the second page.
doc.layoutOptions.continuousSectionPageNumberingRestart = aw.Layout.ContinuousSectionRestart.FromNewPageOnly;
doc.updatePageLayout();

doc.save(base.artifactsDir + "Layout.RestartPageNumberingInContinuousSection.pdf");
```

### See Also

* module [Aspose.Words.Layout](../../)
* class [LayoutOptions](../)

