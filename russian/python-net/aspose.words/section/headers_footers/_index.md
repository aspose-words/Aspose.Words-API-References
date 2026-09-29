---
title: Section.headers_footers property
linktitle: headers_footers property
articleTitle: headers_footers property
second_title: Aspose.Words for Python
description: "Section.headers_footers property. Provides access to the headers and footers nodes of the section."
type: docs
weight: 30
url: /ru/python-net/aspose.words/section/headers_footers/
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
doc = aw.Document(file_name=MY_DIR + 'Header and footer types.docx')
# Пройдитесь по каждому разделу и удалите все типы нижних колонтитулов.
for section in filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_section(), b), list(doc))):
    # Существует три типа нижних и верхних колонтитулов.
    # 1 -  "First" верхний/нижний колонтитул, который отображается только на первой странице раздела.
    footer = section.headers_footers.get_by_header_footer_type(aw.HeaderFooterType.FOOTER_FIRST)
    cond_expression = footer
    if cond_expression != None:
        cond_expression.remove()
    # 2 -  "Primary" верхний/нижний колонтитул, который отображается на нечётных страницах.
    footer = section.headers_footers.get_by_header_footer_type(aw.HeaderFooterType.FOOTER_PRIMARY)
    cond_expression2 = footer
    if cond_expression2 != None:
        cond_expression2.remove()
    # 3 -  "Even" верхний/нижний колонтитул, который отображается на чётных страницах.
    footer = section.headers_footers.get_by_header_footer_type(aw.HeaderFooterType.FOOTER_EVEN)
    cond_expression3 = footer
    if cond_expression3 != None:
        cond_expression3.remove()
    self.assertEqual(0, len(list(filter(lambda hf: not hf.as_header_footer().is_header, section.headers_footers))))
doc.save(file_name=ARTIFACTS_DIR + 'HeaderFooter.RemoveFooters.docx')
```

Shows how to replace text in a document's footer.

```python
doc = aw.Document(file_name=MY_DIR + 'Footer.docx')
headers_footers = doc.first_section.headers_footers
footer = headers_footers.get_by_header_footer_type(aw.HeaderFooterType.FOOTER_PRIMARY)
options = aw.replacing.FindReplaceOptions()
options.match_case = False
options.find_whole_words_only = False
current_year = datetime.datetime.now().year
footer.range.replace(pattern='(C) 2006 Aspose Pty Ltd.', replacement=f'Copyright (C) {current_year} by Aspose Pty Ltd.', options=options)
doc.save(file_name=ARTIFACTS_DIR + 'HeaderFooter.ReplaceText.docx')
```

### See Also

* module [aspose.words](../../)
* class [Section](../)

