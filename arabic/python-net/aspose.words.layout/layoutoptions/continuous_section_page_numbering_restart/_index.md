---
title: LayoutOptions.continuous_section_page_numbering_restart property
linktitle: continuous_section_page_numbering_restart property
articleTitle: continuous_section_page_numbering_restart property
second_title: Aspose.Words for Python
description: "LayoutOptions.continuous_section_page_numbering_restart property. Gets or sets the mode of behavior for computing page numbers when a continuous section restarts the page numbering."
type: docs
weight: 40
url: /ar/python-net/aspose.words.layout/layoutoptions/continuous_section_page_numbering_restart/
---

## LayoutOptions.continuous_section_page_numbering_restart property

Gets or sets the mode of behavior for computing page numbers when a continuous section
restarts the page numbering.


```python
@property
def continuous_section_page_numbering_restart(self) -> aspose.words.layout.ContinuousSectionRestart:
    ...

@continuous_section_page_numbering_restart.setter
def continuous_section_page_numbering_restart(self, value: aspose.words.layout.ContinuousSectionRestart):
    ...

```

### Remarks

The default value is [ContinuousSectionRestart.ALWAYS](../../continuoussectionrestart/#ALWAYS).
It matches the behavior of MS Word 2019 which was the latest version at the moment the option was introduced.
Older page numbering logic demonstrated by MS Word 2016 is available via this option.
Please [ContinuousSectionRestart](../../continuoussectionrestart/) for the behavior description.



### Examples

Shows how to control page numbering in a continuous section.

```python
doc = aw.Document(file_name=MY_DIR + 'Continuous section page numbering.docx')
# بشكل افتراضي، سلوك Aspose.Words يطابق Microsoft Word 2019.
# إذا كنت بحاجة إلى سلوك Aspose.Words القديم، مثل Microsoft Word 2016 المتكرر، استخدم 'ContinuousSectionRestart.FromNewPageOnly'.
# يتم إعادة بدء ترقيم الصفحات فقط إذا لم يكن هناك محتوى آخر قبل القسم على الصفحة التي يبدأ فيها القسم،
# وبسبب ذلك سيُعاد ضبط الترقيم إلى 2 بدءًا من الصفحة الثانية.
doc.layout_options.continuous_section_page_numbering_restart = aw.layout.ContinuousSectionRestart.FROM_NEW_PAGE_ONLY
doc.update_page_layout()
doc.save(file_name=ARTIFACTS_DIR + 'Layout.RestartPageNumberingInContinuousSection.pdf')
```

### See Also

* module [aspose.words.layout](../../)
* class [LayoutOptions](../)

