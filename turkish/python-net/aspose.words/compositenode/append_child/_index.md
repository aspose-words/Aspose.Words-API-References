---
title: CompositeNode.append_child method
linktitle: append_child method
articleTitle: append_child method
second_title: Aspose.Words for Python
description: "CompositeNode.append_child method. Adds the specified node to the end of the list of child nodes for this node."
type: docs
weight: 80
url: /tr/python-net/aspose.words/compositenode/append_child/
---

## append_child(new_child) {#node}

Adds the specified node to the end of the list of child nodes for this node.


```python
def append_child(self, new_child: aspose.words.Node):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| new_child | [Node](../../node/) | The node to add. |

### Remarks

If the *newChild* is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use 
[DocumentBase.import_node()](../../documentbase/import_node/#node_bool_importformatmode) to import the node to the current document. 
The imported node can then be inserted into the current document.




### Returns

The node added.


### Examples

Shows how to construct an Aspose.Words document by hand.

```python
doc = aw.Document()
# Boş bir belge bir bölüm, bir gövde ve bir paragraf içerir.
# "RemoveAllChildren" metodunu çağırarak bu düğümlerin tümünü kaldırın,
# ve hiçbir çocuğu olmayan bir belge düğümü elde edin.
doc.remove_all_children()
# Bu belge artık içerik ekleyebileceğimiz birleşik çocuk düğümlerine sahip değil.
# Eğer düzenlemek istersek, düğüm koleksiyonunu yeniden doldurmamız gerekecek.
# İlk olarak yeni bir bölüm oluşturun ve ardından bunu kök belge düğümüne çocuk olarak ekleyin.
section = aw.Section(doc)
doc.append_child(section)
# Bölüm için bazı sayfa ayarı özelliklerini ayarlayın.
section.page_setup.section_start = aw.SectionStart.NEW_PAGE
section.page_setup.paper_size = aw.PaperSize.LETTER
# Bir bölüm bir gövdeye ihtiyaç duyar; bu gövde tüm içeriğini barındırır ve gösterir
# sayfada bölümün başlığı ile altbilgisi arasında.
body = aw.Body(doc)
section.append_child(body)
# Bir paragraf oluşturun, bazı biçimlendirme özelliklerini ayarlayın ve ardından gövdeye çocuk olarak ekleyin.
para = aw.Paragraph(doc)
para.paragraph_format.style_name = 'Heading 1'
para.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
body.append_child(para)
# Son olarak, belgeyi oluşturmak için bazı içerikler ekleyin. Bir run oluşturun,
# görünümünü ve içeriğini ayarlayın, ardından paragrafın çocuğu olarak ekleyin.
run = aw.Run(doc=doc)
run.text = 'Hello World!'
run.font.color = aspose.pydrawing.Color.red
para.append_child(run)
self.assertEqual('Hello World!', doc.get_text().strip())
doc.save(file_name=ARTIFACTS_DIR + 'Section.CreateManually.docx')
```

### See Also

* module [aspose.words](../../)
* class [CompositeNode](../)

