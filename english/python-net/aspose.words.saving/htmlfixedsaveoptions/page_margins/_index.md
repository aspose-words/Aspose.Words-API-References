---
title: HtmlFixedSaveOptions.page_margins property
linktitle: page_margins property
articleTitle: page_margins property
second_title: Aspose.Words for Python
description: "HtmlFixedSaveOptions.page_margins property. Specifies the margins around pages in an HTML document"
type: docs
weight: 130
url: /python-net/aspose.words.saving/htmlfixedsaveoptions/page_margins/
---

## HtmlFixedSaveOptions.page_margins property

Specifies the margins around pages in an HTML document.
The margins value is measured in points and should be equal to or greater than 0.
Default value is 10 points.


```python
@property
def page_margins(self) -> float:
    ...

@page_margins.setter
def page_margins(self, value: float):
    ...

```

### Remarks

Depends on the value of [HtmlFixedSaveOptions.page_horizontal_alignment](../page_horizontal_alignment/) property:


* Defines top, bottom and left page margins if the value is [HtmlFixedPageHorizontalAlignment.LEFT](../../htmlfixedpagehorizontalalignment/#LEFT).
  
  
* Defines top, bottom and right page margins if the value is [HtmlFixedPageHorizontalAlignment.RIGHT](../../htmlfixedpagehorizontalalignment/#RIGHT).
  
  
* Defines top and bottom page margins if the value is [HtmlFixedPageHorizontalAlignment.CENTER](../../htmlfixedpagehorizontalalignment/#CENTER).
  
  



### Examples

Shows how to adjust page margins when saving a document to HTML.

```python
doc = aw.Document(MY_DIR + 'Document.docx')
save_options = aw.saving.HtmlFixedSaveOptions()
save_options.page_margins = 15
doc.save(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.page_margins.html', save_options)
with open(ARTIFACTS_DIR + 'HtmlFixedSaveOptions.page_margins/styles.css', 'rt', encoding='utf-8') as file:
    out_doc_contents = file.read()
self.assertRegex(out_doc_contents, '[.]awpage { position:relative; border:solid 1pt black; margin:15pt auto 15pt auto; overflow:hidden; }')
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlFixedSaveOptions](../)

