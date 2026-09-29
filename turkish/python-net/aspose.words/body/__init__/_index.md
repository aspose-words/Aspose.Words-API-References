---
title: Body constructor
linktitle: Body constructor
articleTitle: Body constructor
second_title: Aspose.Words for Python
description: "Body constructor. Initializes a new instance of the [Body](../) class."
type: docs
weight: 10
url: /tr/python-net/aspose.words/body/__init__/
---

## Body(doc) {#documentbase}

Initializes a new instance of the [Body](../) class.



```python
def __init__(self, doc: aspose.words.DocumentBase):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| doc | [DocumentBase](../../documentbase/) | The owner document. |

### Remarks

When [Body](../) is created, it belongs to the specified document, but is not 
yet part of the document and [Node.parent_node](../../node/parent_node/) is ``None``.

To append [Body](../) to a [Section](../../section/) use [CompositeNode.append_child()](../../compositenode/append_child/#node)
[CompositeNode.insert_after()](../../compositenode/insert_after/#node_node) or [CompositeNode.insert_before()](../../compositenode/insert_before/#node_node)
methods.




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
* class [Body](../)

