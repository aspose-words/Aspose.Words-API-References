---
title: continuous_section_page_numbering_restart property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the mode of behavior for computing page numbers when a continuous section restarts the page numbering."
type: docs
weight: 40
url: /python-net/aspose.words.layout/layoutoptions/continuous_section_page_numbering_restart/
---

## LayoutOptions.continuous_section_page_numbering_restart property

Gets or sets the mode of behavior for computing page numbers when a continuous section
restarts the page numbering.

The default value is [ContinuousSectionRestart.ALWAYS](../../continuoussectionrestart/#ALWAYS).
It matches the behavior of MS Word 2019 which was the latest version at the moment the option was introduced.
Older page numbering logic demonstrated by MS Word 2016 is available via this option.
Please [ContinuousSectionRestart](../../continuoussectionrestart/) for the behavior description.



### Examples

Shows how to control page numbering in a continuous section.

```python
doc = aw.Document(MY_DIR + "Continuous section page numbering.docx")

# By default Aspose.Words behavior matches the Microsoft Word 2019.
# If you need old Aspose.Words behavior, repetitive Microsoft Word 2016, use 'ContinuousSectionRestart.FROM_NEW_PAGE_ONLY'.
# Page numbering restarts only if there is no other content before the section on the page where the section starts,
# because of that the numbering will reset to 2 from the second page.
doc.layout_options.continuous_section_page_numbering_restart = aw.layout.ContinuousSectionRestart.FROM_NEW_PAGE_ONLY
doc.update_page_layout()

doc.save(ARTIFACTS_DIR + "Layout.restart_page_numbering_in_continuous_section.pdf")
```

### See Also

* module [aspose.words.layout](../../)
* class [LayoutOptions](../)

