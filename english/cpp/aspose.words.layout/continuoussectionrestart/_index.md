---
title: Aspose::Words::Layout::ContinuousSectionRestart enum
linktitle: ContinuousSectionRestart
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Layout::ContinuousSectionRestart enum. Represents different behaviors when computing page numbers in a continuous section that restarts page numbering in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words.layout/continuoussectionrestart/
---
## ContinuousSectionRestart enum


Represents different behaviors when computing page numbers in a continuous section that restarts page numbering.

```cpp
enum class ContinuousSectionRestart
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Always | 0 | Page numbering always restarts regardless of content flow. |
| FromNewPageOnly | 1 | Page numbering restarts only if there is no other content before the section on the page where the section starts. |


## Examples



Shows how to control page numbering in a continuous section. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Continuous section page numbering.docx");

// By default Aspose.Words behavior matches the Microsoft Word 2019.
// If you need old Aspose.Words behavior, repetitive Microsoft Word 2016, use 'ContinuousSectionRestart.FromNewPageOnly'.
// Page numbering restarts only if there is no other content before the section on the page where the section starts,
// because of that the numbering will reset to 2 from the second page.
doc->get_LayoutOptions()->set_ContinuousSectionPageNumberingRestart(Aspose::Words::Layout::ContinuousSectionRestart::FromNewPageOnly);
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Layout.RestartPageNumberingInContinuousSection.pdf");
```

## See Also

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
