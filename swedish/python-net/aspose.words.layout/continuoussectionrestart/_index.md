---
title: ContinuousSectionRestart enumeration
linktitle: ContinuousSectionRestart enumeration
articleTitle: ContinuousSectionRestart enumeration
second_title: Aspose.Words for Python
description: "aspose.words.layout.ContinuousSectionRestart enumeration. Represents different behaviors when computing page numbers in a continuous section that restarts page numbering."
type: docs
weight: 20
url: /sv/python-net/aspose.words.layout/continuoussectionrestart/
---

## ContinuousSectionRestart enumeration

Represents different behaviors when computing page numbers in a continuous section that restarts page numbering.


### Members

| Name | Description |
| --- | --- |
| ALWAYS | Page numbering always restarts regardless of content flow. |
| FROM_NEW_PAGE_ONLY | Page numbering restarts only if there is no other content before the section on the page where the section starts. |

### Examples

Shows how to control page numbering in a continuous section.

```python
doc = aw.Document(file_name=MY_DIR + 'Continuous section page numbering.docx')
# Som standard matchar Aspose.Words beteendet Microsoft Word 2019.
# Om du behöver det gamla Aspose.Words-beteendet, liknande Microsoft Word 2016, använd 'ContinuousSectionRestart.FromNewPageOnly'.
# Sidnumrering startar om endast om det inte finns något annat innehåll före avsnittet på sidan där avsnittet börjar,
# på grund av det kommer numreringen att återställas till 2 från den andra sidan.
doc.layout_options.continuous_section_page_numbering_restart = aw.layout.ContinuousSectionRestart.FROM_NEW_PAGE_ONLY
doc.update_page_layout()
doc.save(file_name=ARTIFACTS_DIR + 'Layout.RestartPageNumberingInContinuousSection.pdf')
```

### See Also

* module [aspose.words.layout](../)

