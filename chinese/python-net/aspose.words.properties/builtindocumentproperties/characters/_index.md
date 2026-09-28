---
title: BuiltInDocumentProperties.characters property
linktitle: characters property
articleTitle: characters property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.characters property. Represents an estimate of the number of characters in the document."
type: docs
weight: 50
url: /zh/python-net/aspose.words.properties/builtindocumentproperties/characters/
---

## BuiltInDocumentProperties.characters property

Represents an estimate of the number of characters in the document.


```python
@property
def characters(self) -> int:
    ...

@characters.setter
def characters(self, value: int):
    ...

```

### Remarks

Aspose.Words updates this property when you call [Document.update_word_count()](../../../aspose.words/document/update_word_count/#default).




### Examples

Shows how to update all list labels in a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
builder.write('Ut enim ad minim veniam, ' + 'quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.')
# Aspose.Words 并不会实时跟踪此类文档指标。
self.assertEqual(0, doc.built_in_document_properties.characters)
self.assertEqual(0, doc.built_in_document_properties.words)
self.assertEqual(1, doc.built_in_document_properties.paragraphs)
self.assertEqual(1, doc.built_in_document_properties.lines)
# 要获取这三个属性的准确值，我们需要手动更新它们。
doc.update_word_count()
self.assertEqual(196, doc.built_in_document_properties.characters)
self.assertEqual(36, doc.built_in_document_properties.words)
self.assertEqual(2, doc.built_in_document_properties.paragraphs)
# 对于行数，我们需要调用更新方法的特定重载。
self.assertEqual(1, doc.built_in_document_properties.lines)
doc.update_word_count(True)
self.assertEqual(4, doc.built_in_document_properties.lines)
```

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

