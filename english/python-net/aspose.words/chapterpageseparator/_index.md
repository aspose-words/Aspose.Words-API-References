---
title: ChapterPageSeparator enumeration
linktitle: ChapterPageSeparator enumeration
articleTitle: ChapterPageSeparator enumeration
second_title: Aspose.Words for Python
description: "aspose.words.ChapterPageSeparator enumeration. Defines the separator character that appears between the chapter and page number."
type: docs
weight: 150
url: /python-net/aspose.words/chapterpageseparator/
---

## ChapterPageSeparator enumeration

Defines the separator character that appears between the chapter and page number.


### Members

| Name | Description |
| --- | --- |
| HYPHEN | A colon. |
| PERIOD | A period. |
| COLON | A colon. |
| EM_DASH | An emphasized dash. |
| EN_DASH | A standard dash. |

### Examples

Shows how to work with page chapters.

```python
doc = aw.Document(file_name=MY_DIR + 'Big document.docx')
page_setup = doc.first_section.page_setup
page_setup.page_number_style = aw.NumberStyle.UPPERCASE_ROMAN
page_setup.chapter_page_separator = aw.ChapterPageSeparator.COLON
page_setup.heading_level_for_chapter = 1
```

### See Also

* module [aspose.words](../)
* class [PageSetup](../pagesetup/)
* property [PageSetup.chapter_page_separator](../pagesetup/chapter_page_separator/)

