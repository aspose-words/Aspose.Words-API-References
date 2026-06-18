---
title: BuiltInDocumentProperties.characters_with_spaces property
linktitle: characters_with_spaces property
articleTitle: characters_with_spaces property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.characters_with_spaces property. Represents an estimate of the number of characters (including spaces) in the document."
type: docs
weight: 60
url: /python-net/aspose.words.properties/builtindocumentproperties/characters_with_spaces/
---

## BuiltInDocumentProperties.characters_with_spaces property

Represents an estimate of the number of characters (including spaces) in the document.


```python
@property
def characters_with_spaces(self) -> int:
    ...

@characters_with_spaces.setter
def characters_with_spaces(self, value: int):
    ...

```

### Remarks

Aspose.Words updates this property when you call [Document.update_word_count()](../../../aspose.words/document/update_word_count/#default).




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

