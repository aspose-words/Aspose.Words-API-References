---
title: ContinuousSectionRestart enumeration
linktitle: ContinuousSectionRestart enumeration
articleTitle: ContinuousSectionRestart enumeration
second_title: Aspose.Words for Python
description: "aspose.words.layout.ContinuousSectionRestart enumeration. Represents different behaviors when computing page numbers in a continuous section that restarts page numbering."
type: docs
weight: 20
url: /zh/python-net/aspose.words.layout/continuoussectionrestart/
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
# 默认情况下，Aspose.Words 的行为匹配 Microsoft Word 2019。
# 如果您需要旧的 Aspose.Words 行为，即重复的 Microsoft Word 2016，请使用 'ContinuousSectionRestart.FromNewPageOnly'。
# 仅当章节开始的页面上在该章节之前没有其他内容时，页码才会重新开始，
# 因此页码将在第二页起重置为 2。
doc.layout_options.continuous_section_page_numbering_restart = aw.layout.ContinuousSectionRestart.FROM_NEW_PAGE_ONLY
doc.update_page_layout()
doc.save(file_name=ARTIFACTS_DIR + 'Layout.RestartPageNumberingInContinuousSection.pdf')
```

### See Also

* module [aspose.words.layout](../)

