---
title: SectionStart enumeration
linktitle: SectionStart enumeration
articleTitle: SectionStart enumeration
second_title: Aspose.Words for Python
description: "aspose.words.SectionStart enumeration. The type of break at the beginning of the section."
type: docs
weight: 1170
url: /sv/python-net/aspose.words/sectionstart/
---

## SectionStart enumeration

The type of break at the beginning of the section.


### Members

| Name | Description |
| --- | --- |
| CONTINUOUS | The new section starts on the same page as the previous section. |
| NEW_COLUMN | The section starts from a new column. |
| NEW_PAGE | The section starts from a new page. |
| EVEN_PAGE | The section starts on a new even page. |
| ODD_PAGE | The section starts on a new odd page. |

### Examples

Shows how to specify how a new section separates itself from the previous.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('This text is in section 1.')
# Typen av sektionsbrytning bestämmer hur ett nytt avsnitt separerar sig från föregående avsnitt.
# Nedan följer fem typer av sektionsbrytningar.
# 1 -  Startar nästa avsnitt på en ny sida:
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.writeln('This text is in section 2.')
self.assertEqual(aw.SectionStart.NEW_PAGE, doc.sections[1].page_setup.section_start)
# 2 -  Startar nästa avsnitt på den aktuella sidan:
builder.insert_break(aw.BreakType.SECTION_BREAK_CONTINUOUS)
builder.writeln('This text is in section 3.')
self.assertEqual(aw.SectionStart.CONTINUOUS, doc.sections[2].page_setup.section_start)
# 3 -  Startar nästa avsnitt på en ny jämn sida:
builder.insert_break(aw.BreakType.SECTION_BREAK_EVEN_PAGE)
builder.writeln('This text is in section 4.')
self.assertEqual(aw.SectionStart.EVEN_PAGE, doc.sections[3].page_setup.section_start)
# 4 -  Startar nästa avsnitt på en ny udda sida:
builder.insert_break(aw.BreakType.SECTION_BREAK_ODD_PAGE)
builder.writeln('This text is in section 5.')
self.assertEqual(aw.SectionStart.ODD_PAGE, doc.sections[4].page_setup.section_start)
# 5 -  Startar nästa avsnitt i en ny kolumn:
columns = builder.page_setup.text_columns
columns.set_count(2)
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_COLUMN)
builder.writeln('This text is in section 6.')
self.assertEqual(aw.SectionStart.NEW_COLUMN, doc.sections[5].page_setup.section_start)
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.SetSectionStart.docx')
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

* module [aspose.words](../)

