---
title: Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart method
linktitle: get_ContinuousSectionPageNumberingRestart
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart method. Gets or sets the mode of behavior for computing page numbers when a continuous section restarts the page numbering in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.layout/layoutoptions/get_continuoussectionpagenumberingrestart/
---
## LayoutOptions::get_ContinuousSectionPageNumberingRestart method


Gets or sets the mode of behavior for computing page numbers when a continuous section restarts the page numbering.

```cpp
Aspose::Words::Layout::ContinuousSectionRestart Aspose::Words::Layout::LayoutOptions::get_ContinuousSectionPageNumberingRestart() const
```


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

* Enum [ContinuousSectionRestart](../../continuoussectionrestart/)
* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
