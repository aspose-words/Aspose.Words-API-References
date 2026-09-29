---
title: ParagraphAlignment enumeration
linktitle: ParagraphAlignment enumeration
articleTitle: ParagraphAlignment enumeration
second_title: Aspose.Words for Python
description: "aspose.words.ParagraphAlignment enumeration. Specifies text alignment in a paragraph."
type: docs
weight: 970
url: /sv/python-net/aspose.words/paragraphalignment/
---

## ParagraphAlignment enumeration

Specifies text alignment in a paragraph.


### Members

| Name | Description |
| --- | --- |
| LEFT | Text is aligned to the left. |
| CENTER | Text is centered horizontally. |
| RIGHT | Text is aligned to the right. |
| JUSTIFY | Text is aligned to both left and right. |
| DISTRIBUTED | Text is evenly distributed. |
| ARABIC_MEDIUM_KASHIDA | Arabic only. Kashida length for text is extended to a medium length determined by the consumer. |
| ARABIC_HIGH_KASHIDA | Arabic only. Kashida length for text is extended to its widest possible length. |
| ARABIC_LOW_KASHIDA | Arabic only. Kashida length for text is extended to a slightly longer length. |
| THAI_DISTRIBUTED | Thai only. Text is justified with an optimization for Thai. |
| MATH_ELEMENT_CENTER_AS_GROUP | The only Math element in a line, aligned as 'Centered As Group'. |

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

* module [aspose.words](../)

