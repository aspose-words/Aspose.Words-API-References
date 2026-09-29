---
title: Section.page_setup property
linktitle: page_setup property
articleTitle: page_setup property
second_title: Aspose.Words for Python
description: "Section.page_setup property. Returns an object that represents page setup and section properties."
type: docs
weight: 50
url: /sv/python-net/aspose.words/section/page_setup/
---

## Section.page_setup property

Returns an object that represents page setup and section properties.


```python
@property
def page_setup(self) -> aspose.words.PageSetup:
    ...

```

### Examples

Shows how to create a wide blue band border at the top of the first page.

```python
doc = aw.Document()
page_setup = doc.sections[0].page_setup
page_setup.border_always_in_front = False
page_setup.border_distance_from = aw.PageBorderDistanceFrom.PAGE_EDGE
page_setup.border_applies_to = aw.PageBorderAppliesTo.FIRST_PAGE
border = page_setup.borders.get_by_border_type(aw.BorderType.TOP)
border.line_style = aw.LineStyle.SINGLE
border.line_width = 30
border.color = aspose.pydrawing.Color.blue
border.distance_from_text = 0
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.PageBorderProperties.docx')
```

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
* class [Section](../)

