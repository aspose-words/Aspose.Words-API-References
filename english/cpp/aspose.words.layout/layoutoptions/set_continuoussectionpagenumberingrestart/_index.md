---
title: Aspose::Words::Layout::LayoutOptions::set_ContinuousSectionPageNumberingRestart method
linktitle: set_ContinuousSectionPageNumberingRestart
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Layout::LayoutOptions::set_ContinuousSectionPageNumberingRestart method. Sets the mode of behavior for computing page numbers when a continuous section restarts the page numbering in C++.'
type: docs
weight: 15000
url: /cpp/aspose.words.layout/layoutoptions/set_continuoussectionpagenumberingrestart/
---
## LayoutOptions::set_ContinuousSectionPageNumberingRestart method


Sets the mode of behavior for computing page numbers when a continuous section restarts the page numbering.

```cpp
void Aspose::Words::Layout::LayoutOptions::set_ContinuousSectionPageNumberingRestart(Aspose::Words::Layout::ContinuousSectionRestart value)
```

## Remarks

 The default value is [Always](../../continuoussectionrestart/). It matches the behavior of MS Word 2019 which was the latest version at the moment the option was introduced. Older page numbering logic demonstrated by MS Word 2016 is available via this option. Please [ContinuousSectionRestart](../../continuoussectionrestart/) for the behavior description. 
## Examples


Shows how to control page numbering in a continuous section.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Continuous section page numbering.docx"));

// By default Aspose.Words behavior matches the Microsoft Word 2019.
// If you need old Aspose.Words behavior, repetitive Microsoft Word 2016, use 'ContinuousSectionRestart.FromNewPageOnly'.
// Page numbering restarts only if there is no other content before the section on the page where the section starts,
// because of that the numbering will reset to 2 from the second page.
doc->get_LayoutOptions()->set_ContinuousSectionPageNumberingRestart(ContinuousSectionRestart::FromNewPageOnly);
doc->UpdatePageLayout();

doc->Save(get_ArtifactsDir() + u"Layout.RestartPageNumberingInContinuousSection.pdf");
```
## See Also

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
