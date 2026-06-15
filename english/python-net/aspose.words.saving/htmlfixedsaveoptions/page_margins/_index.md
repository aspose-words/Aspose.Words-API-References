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
  
  



### See Also

* module [aspose.words.saving](../../)
* class [HtmlFixedSaveOptions](../)

