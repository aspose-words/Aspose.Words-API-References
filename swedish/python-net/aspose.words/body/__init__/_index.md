---
title: Body constructor
linktitle: Body constructor
articleTitle: Body constructor
second_title: Aspose.Words for Python
description: "Body constructor. Initializes a new instance of the [Body](../) class."
type: docs
weight: 10
url: /sv/python-net/aspose.words/body/__init__/
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
# Ett tomt dokument innehåller en sektion, en kropp och ett stycke.
# Anropa metoden "RemoveAllChildren" för att ta bort alla dessa noder,
# och sluta med ett dokumentnod utan några barn.
doc.remove_all_children()
# Detta dokument har nu inga sammansatta barnnoder som vi kan lägga till innehåll i.
# Om vi vill redigera det måste vi återfylla dess nodsamling.
# Först, skapa en ny sektion och lägg sedan till den som ett barn till rot-dokumentnoden.
section = aw.Section(doc)
doc.append_child(section)
# Ställ in några sidinställningsegenskaper för sektionen.
section.page_setup.section_start = aw.SectionStart.NEW_PAGE
section.page_setup.paper_size = aw.PaperSize.LETTER
# En sektion behöver en kropp, som kommer att innehålla och visa allt dess innehåll
# på sidan mellan sektionens sidhuvud och sidfot.
body = aw.Body(doc)
section.append_child(body)
# Skapa ett stycke, ställ in några formateringsegenskaper och lägg sedan till det som ett barn till kroppen.
para = aw.Paragraph(doc)
para.paragraph_format.style_name = 'Heading 1'
para.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
body.append_child(para)
# Slutligen, lägg till lite innehåll i dokumentet. Skapa en run,
# ställ in dess utseende och innehåll, och lägg sedan till den som ett barn till stycket.
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

