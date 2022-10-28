---
title: get_by_header_footer_type method
second_title: Aspose.Words for Python via .NET API Reference
description: "Retrieves a HeaderFooter of the specified type."
type: docs
weight: 80
url: /python-net/aspose.words/headerfootercollection/get_by_header_footer_type/
---

## get_by_header_footer_type(header_footer_type) {#headerfootertype}

Retrieves a **HeaderFooter** of the specified type.



```python
def get_by_header_footer_type(self, header_footer_type: aspose.words.HeaderFooterType):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| header_footer_type | [HeaderFooterType](../../headerfootertype/) |  |

### Examples

Shows how to replace text in a document's footer.

```python
doc = aw.Document(MY_DIR + "Footer.docx")

headers_footers = doc.first_section.headers_footers
footer = headers_footers.get_by_header_footer_type(aw.HeaderFooterType.FOOTER_PRIMARY)

options = aw.replacing.FindReplaceOptions()
options.match_case = False
options.find_whole_words_only = False

current_year = date.today().year
footer.range.replace("(C) 2006 Aspose Pty Ltd.", f"Copyright (C) {current_year} by Aspose Pty Ltd.", options)

doc.save(ARTIFACTS_DIR + "HeaderFooter.replace_text.docx")
```

### See Also

* module [aspose.words](../../)
* class [HeaderFooterCollection](../)

