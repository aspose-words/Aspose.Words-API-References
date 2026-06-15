---
title: BuiltInDocumentProperties.links_up_to_date property
linktitle: links_up_to_date property
articleTitle: links_up_to_date property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.links_up_to_date property. Indicates whether hyperlinks in a document are up-to-date."
type: docs
weight: 200
url: /python-net/aspose.words.properties/builtindocumentproperties/links_up_to_date/
---

## BuiltInDocumentProperties.links_up_to_date property

Indicates whether hyperlinks in a document are up-to-date.


```python
@property
def links_up_to_date(self) -> bool:
    ...

@links_up_to_date.setter
def links_up_to_date(self, value: bool):
    ...

```

### Remarks

Aspose.Words does not update this property.




### Examples

Shows how to work with document properties in the "Content" category (LineCounter).

```python
class LineCounter:

    def __init__(self, doc):
        self.m_scanning_line_for_real_text = None
        self.m_line_count = None
        self.m_layout_enumerator = aw.layout.LayoutEnumerator(doc)
        self._count_lines()

    def get_line_count(self):
        return self.m_line_count

    def _count_lines(self):
        while true:
            if self.m_layout_enumerator.type == aw.layout.LayoutEntityType.LINE:
                self.m_scanning_line_for_real_text = True
            if self.m_layout_enumerator.move_first_child():
                if self.m_scanning_line_for_real_text and self.m_layout_enumerator.kind.startswith('TEXT'):
                    self.m_line_count += 1
                    self.m_scanning_line_for_real_text = False
                self._count_lines()
                self.m_layout_enumerator.move_parent()
            if self.m_layout_enumerator.move_next():
                break
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

