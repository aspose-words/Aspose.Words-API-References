---
title: FixedPageSaveOptions.numeral_format property
linktitle: numeral_format property
articleTitle: numeral_format property
second_title: Aspose.Words for Python
description: "FixedPageSaveOptions.numeral_format property. Gets or sets [NumeralFormat](../../numeralformat/) used for rendering of numerals"
type: docs
weight: 40
url: /python-net/aspose.words.saving/fixedpagesaveoptions/numeral_format/
---

## FixedPageSaveOptions.numeral_format property

Gets or sets [NumeralFormat](../../numeralformat/) used for rendering of numerals.
European numerals are used by default.



```python
@property
def numeral_format(self) -> aspose.words.saving.NumeralFormat:
    ...

@numeral_format.setter
def numeral_format(self, value: aspose.words.saving.NumeralFormat):
    ...

```

### Remarks

If the value of this property is changed and page layout is already built then
[Document.update_page_layout()](../../../aspose.words/document/update_page_layout/#default) is invoked automatically to update any changes.



### See Also

* module [aspose.words.saving](../../)
* class [FixedPageSaveOptions](../)

