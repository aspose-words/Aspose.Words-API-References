---
title: Section.headers_footers property
linktitle: headers_footers property
articleTitle: headers_footers property
second_title: Aspose.Words for Python
description: "Section.headers_footers property. Provides access to the headers and footers nodes of the section."
type: docs
weight: 30
url: /python-net/aspose.words/section/headers_footers/
---

## Section.headers_footers property

Provides access to the headers and footers nodes of the section.


```python
@property
def headers_footers(self) -> aspose.words.HeaderFooterCollection:
    ...

```

### Examples

Shows how to delete all footers from a document.

```python
doc = aw.Document(MY_DIR + 'Header and footer types.docx')
# Iterate through each section and remove footers of every kind.
for section in doc:
    section = section.as_section()
    # There are three kinds of footer and header types.
    # 1 -  The "First" header/footer, which only appears on the first page of a section.
    footer = section.headers_footers[aw.HeaderFooterType.FOOTER_FIRST]
    if footer is not None:
        footer.remove()
    # 2 -  The "Primary" header/footer, which appears on odd pages.
    footer = section.headers_footers[aw.HeaderFooterType.FOOTER_PRIMARY]
    if footer is not None:
        footer.remove()
    # 3 -  The "Even" header/footer, which appears on even pages.
    footer = section.headers_footers[aw.HeaderFooterType.FOOTER_EVEN]
    if footer is not None:
        footer.remove()
    self.assertEqual(0, len([node for node in section.headers_footers if not node.as_header_footer().is_header]))
doc.save(ARTIFACTS_DIR + 'HeaderFooter.remove_footers.docx')
```

Shows how to replace text in a document's footer.

```python
doc = aw.Document(MY_DIR + 'Footer.docx')
headers_footers = doc.first_section.headers_footers
footer = headers_footers.get_by_header_footer_type(aw.HeaderFooterType.FOOTER_PRIMARY)
options = aw.replacing.FindReplaceOptions()
options.match_case = False
options.find_whole_words_only = False
current_year = date.today().year
footer.range.replace('(C) 2006 Aspose Pty Ltd.', f'Copyright (C) {current_year} by Aspose Pty Ltd.', options)
doc.save(ARTIFACTS_DIR + 'HeaderFooter.replace_text.docx')
```

### See Also

* module [aspose.words](../../)
* class [Section](../)

