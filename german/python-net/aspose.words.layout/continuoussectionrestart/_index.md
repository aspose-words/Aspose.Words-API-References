---
title: ContinuousSectionRestart enumeration
linktitle: ContinuousSectionRestart enumeration
articleTitle: ContinuousSectionRestart enumeration
second_title: Aspose.Words for Python
description: "aspose.words.layout.ContinuousSectionRestart enumeration. Represents different behaviors when computing page numbers in a continuous section that restarts page numbering."
type: docs
weight: 20
url: /de/python-net/aspose.words.layout/continuoussectionrestart/
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
# Standardmäßig entspricht das Verhalten von Aspose.Words dem Microsoft Word 2019.
# Wenn Sie das alte Verhalten von Aspose.Words benötigen, das dem von Microsoft Word 2016 entspricht, verwenden Sie 'ContinuousSectionRestart.FromNewPageOnly'.
# Die Seitennummerierung wird nur neu gestartet, wenn vor dem Abschnitt auf der Seite, auf der der Abschnitt beginnt, kein anderer Inhalt vorhanden ist,
# aus diesem Grund wird die Nummerierung ab der zweiten Seite auf 2 zurückgesetzt.
doc.layout_options.continuous_section_page_numbering_restart = aw.layout.ContinuousSectionRestart.FROM_NEW_PAGE_ONLY
doc.update_page_layout()
doc.save(file_name=ARTIFACTS_DIR + 'Layout.RestartPageNumberingInContinuousSection.pdf')
```

### See Also

* module [aspose.words.layout](../)

