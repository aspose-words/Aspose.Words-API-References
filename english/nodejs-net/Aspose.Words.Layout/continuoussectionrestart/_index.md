---
title: ContinuousSectionRestart enumeration
linktitle: ContinuousSectionRestart enumeration
articleTitle: ContinuousSectionRestart enumeration
second_title: Aspose.Words for NodeJs
description: "Aspose.Words.Layout.ContinuousSectionRestart enumeration. Represents different behaviors when computing page numbers in a continuous section that restarts page numbering."
type: docs
weight: 20
url: /nodejs-net/aspose.words.layout/continuoussectionrestart/
---

## ContinuousSectionRestart enumeration

Represents different behaviors when computing page numbers in a continuous section that restarts page numbering.


### Members

| Name | Description |
| --- | --- |
| Always | Page numbering always restarts regardless of content flow. |
| FromNewPageOnly | Page numbering restarts only if there is no other content before the section on the page where the section starts. |

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

* module [Aspose.Words.Layout](../)

