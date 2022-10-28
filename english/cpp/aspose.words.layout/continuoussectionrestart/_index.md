---
title: ContinuousSectionRestart
second_title: Aspose.Words for C++ API Reference
description: Represents different behaviors when computing page numbers in a continuous section that restarts page numbering.
type: docs
weight: 92
url: /cpp/aspose.words.layout/continuoussectionrestart/
---
## ContinuousSectionRestart enum


Represents different behaviors when computing page numbers in a continuous section that restarts page numbering.

### Values

| Name | Value | Description |
| --- | --- | --- |
| Always | 0 | Page numbering always restarts regardless of content flow. |
| FromNewPageOnly | 1 | Page numbering restarts only if there is no other content before the section on the page where the section starts. |


## Examples




Shows how to control page numbering in a continuous section. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Continuous section page numbering.docx");

// By default Aspose.Words behavior matches the Microsoft Word 2019.
// If you need old Aspose.Words behavior, repetitive Microsoft Word 2016, use 'ContinuousSectionRestart.FromNewPageOnly'.
// Page numbering restarts only if there is no other content before the section on the page where the section starts,
// because of that the numbering will reset to 2 from the second page.
doc->get_LayoutOptions()->set_ContinuousSectionPageNumberingRestart(ContinuousSectionRestart::FromNewPageOnly);
doc->UpdatePageLayout();

doc->Save(ArtifactsDir + u"Layout.RestartPageNumberingInContinuousSection.pdf");
```

