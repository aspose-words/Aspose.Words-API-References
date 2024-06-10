---
title: PageSetup.heading_level_for_chapter property
linktitle: heading_level_for_chapter property
articleTitle: heading_level_for_chapter property
second_title: Aspose.Words for Python
description: "PageSetup.heading_level_for_chapter property. Gets or sets the heading level style that is applied to the chapter titles in the document."
type: docs
weight: 180
url: /python-net/aspose.words/pagesetup/heading_level_for_chapter/
---

## PageSetup.heading_level_for_chapter property

Gets or sets the heading level style that is applied to the chapter titles in the document.


```python
@property
def heading_level_for_chapter(self) -> int:
    ...

@heading_level_for_chapter.setter
def heading_level_for_chapter(self, value: int):
    ...

```

### Remarks

Can be a number from 0 through 9. 0 means no chapter number if applied to page number.

Before you can create page numbers that include chapter numbers, the document headings must have a numbered outline format applied.




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

* module [aspose.words](../../)
* class [PageSetup](../)

