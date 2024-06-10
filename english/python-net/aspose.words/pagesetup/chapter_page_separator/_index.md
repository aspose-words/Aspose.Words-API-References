---
title: PageSetup.chapter_page_separator property
linktitle: chapter_page_separator property
articleTitle: chapter_page_separator property
second_title: Aspose.Words for Python
description: "PageSetup.chapter_page_separator property. Gets or sets the separator character that appears between the chapter number and the page number."
type: docs
weight: 90
url: /python-net/aspose.words/pagesetup/chapter_page_separator/
---

## PageSetup.chapter_page_separator property

Gets or sets the separator character that appears between the chapter number and the page number.


```python
@property
def chapter_page_separator(self) -> aspose.words.ChapterPageSeparator:
    ...

@chapter_page_separator.setter
def chapter_page_separator(self, value: aspose.words.ChapterPageSeparator):
    ...

```

### Remarks

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

