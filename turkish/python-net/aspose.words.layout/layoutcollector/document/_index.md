---
title: LayoutCollector.document property
linktitle: document property
articleTitle: document property
second_title: Aspose.Words for Python
description: "LayoutCollector.document property. Gets or sets the document this collector instance is attached to."
type: docs
weight: 20
url: /tr/python-net/aspose.words.layout/layoutcollector/document/
---

## LayoutCollector.document property

Gets or sets the document this collector instance is attached to.


```python
@property
def document(self) -> aspose.words.Document:
    ...

@document.setter
def document(self, value: aspose.words.Document):
    ...

```

### Remarks

If you need to access page indexes of the document nodes you need to set this property to point to a document instance,
before page layout of the document is built. It is best to set this property to ``None`` afterwards, 
otherwise the collector continues to accumulate information from subsequent rebuilds of the document's page layout.



### Examples

Shows how to see the the ranges of pages that a node spans.

```python
doc = aw.Document()
layout_collector = aw.layout.LayoutCollector(doc)
# Belgemizin içeriğinin kaç sayfaya yayıldığını saymak için "GetNumPagesSpanned" yöntemini çağırın.
# Belge boş olduğu için, sayfa sayısı şu anda sıfırdır.
self.assertEqual(doc, layout_collector.document)
self.assertEqual(0, layout_collector.get_num_pages_spanned(doc))
# Belgeyi 5 sayfa içerikle doldurun.
builder = aw.DocumentBuilder(doc=doc)
builder.write('Section 1')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.SECTION_BREAK_EVEN_PAGE)
builder.write('Section 2')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Düzen toplayıcıdan önce, bize ... vermesi için "UpdatePageLayout" yöntemini çağırmamız gerekir
# sayfa sayısı gibi düzenle ilgili herhangi bir metrik için doğru bir sayı.
self.assertEqual(0, layout_collector.get_num_pages_spanned(doc))
layout_collector.clear()
doc.update_page_layout()
self.assertEqual(5, layout_collector.get_num_pages_spanned(doc))
# Herhangi bir düğümün başlangıç ve bitiş sayfa numaralarını ve toplam sayfa kapsamlarını görebiliriz.
nodes = doc.get_child_nodes(aw.NodeType.ANY, True)
for node in nodes:
    print(f'->  NodeType.{node.node_type}: ')
    print(f'\tStarts on page {layout_collector.get_start_page_index(node)}, ends on page {layout_collector.get_end_page_index(node)},' + f' spanning {layout_collector.get_num_pages_spanned(node)} pages.')
# LayoutEnumerator kullanarak düzen varlıkları üzerinde yineleme yapabiliriz.
layout_enumerator = aw.layout.LayoutEnumerator(doc)
self.assertEqual(aw.layout.LayoutEntityType.PAGE, layout_enumerator.type)
# LayoutEnumerator, düzen varlıkları koleksiyonunu bir ağaç gibi dolaşabilir.
# Bunu herhangi bir düğümün ilgili düzen varlığına da uygulayabiliriz.
layout_enumerator.set_current(layout_collector, doc.get_child(aw.NodeType.PARAGRAPH, 1, True))
self.assertEqual(aw.layout.LayoutEntityType.SPAN, layout_enumerator.type)
self.assertEqual('¶', layout_enumerator.text)
```

### See Also

* module [aspose.words.layout](../../)
* class [LayoutCollector](../)

