---
title: HeaderFooterCollection.link_to_previous method
linktitle: link_to_previous method
articleTitle: link_to_previous method
second_title: Aspose.Words for Python
description: "aspose.words.HeaderFooterCollection.link_to_previous method"
type: docs
weight: 90
url: /sv/python-net/aspose.words/headerfootercollection/link_to_previous/
---

## link_to_previous(is_link_to_previous) {#bool}

Links or unlinks all headers and footers to the corresponding
headers and footers in the previous section.


```python
def link_to_previous(self, is_link_to_previous: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| is_link_to_previous | bool | ``True`` to link the headers and footers to the previous section; ``False`` to unlink them. |

### Remarks

If any of the headers or footers do not exist, creates them automatically.




## link_to_previous(header_footer_type, is_link_to_previous) {#headerfootertype_bool}

Links or unlinks the specified header or footer to the corresponding
header or footer in the previous section.


```python
def link_to_previous(self, header_footer_type: aspose.words.HeaderFooterType, is_link_to_previous: bool):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| header_footer_type | [HeaderFooterType](../../headerfootertype/) | A [HeaderFooterType](../../headerfootertype/) value that specifies the header or footer to link/unlink. |
| is_link_to_previous | bool | ``True`` to link the header or footer to the previous section; ``False`` to unlink. |

### Remarks

If the header or footer of the specified type does not exist, creates it automatically.




## Examples

Shows how to link headers and footers between sections.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Section 1')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('Section 2')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('Section 3')
# Gå till det första avsnittet och skapa ett sidhuvud och en sidfot. Som standard,
# kommer sidhuvudet och sidfoten endast att visas på sidor i det avsnitt som innehåller dem.
builder.move_to_section(0)
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.write('This is the header, which will be displayed in sections 1 and 2.')
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
builder.write('This is the footer, which will be displayed in sections 1, 2 and 3.')
# Vi kan länka ett avsnitts sidhuvuden/sidfötter till föregående avsnitts sidhuvuden/sidfötter
# för att låta det länkade avsnittet visa det länkade avsnittets sidhuvuden/sidfötter.
doc.sections[1].headers_footers.link_to_previous(is_link_to_previous=True)
# Varje avsnitt kommer fortfarande att ha sina egna sidhuvuds-/sidfot-objekt. När vi länkar avsnitt,
# kommer det länkande avsnittet att visa det länkade avsnittets sidhuvud/sidfötter samtidigt som det behåller sina egna.
assert doc.sections[0].headers_footers[0] is not doc.sections[1].headers_footers[0]
assert doc.sections[0].headers_footers[0].parent_section is not doc.sections[1].headers_footers[0].parent_section
# Länka sidhuvuden/sidfötterna i det tredje avsnittet till sidhuvuden/sidfötterna i det andra avsnittet.
# Det andra avsnittet länkar redan till det första avsnittets sidhuvuden/sidfötter,
# så att länka till det andra avsnittet kommer att skapa en länkkedja.
# Det första, andra och nu det tredje avsnittet kommer alla att visa det första avsnittets sidhuvuden.
doc.sections[2].headers_footers.link_to_previous(is_link_to_previous=True)
# Vi kan ta bort länken till ett föregående avsnitts sidhuvuden/sidfötter genom att skicka "false" när vi anropar metoden LinkToPrevious.
doc.sections[2].headers_footers.link_to_previous(is_link_to_previous=False)
# Vi kan också välja endast en specifik typ av sidhuvud/sidfot att länka med hjälp av den här metoden.
# Det tredje avsnittet kommer nu att ha samma sidfot som det andra och första avsnittet, men inte sidhuvudet.
doc.sections[2].headers_footers.link_to_previous(header_footer_type=aw.HeaderFooterType.FOOTER_PRIMARY, is_link_to_previous=True)
# Den första sektionens header/footers kan inte länka sig själva till något eftersom det inte finns någon föregående sektion.
self.assertEqual(2, doc.sections[0].headers_footers.count)
self.assertEqual(2, len(list(filter(lambda hf: not hf.as_header_footer().is_linked_to_previous, doc.sections[0].headers_footers))))
# Alla den andra sektionens header/footers är länkade till den första sektionens header/footers.
self.assertEqual(6, doc.sections[1].headers_footers.count)
self.assertEqual(6, len(list(filter(lambda hf: hf.as_header_footer().is_linked_to_previous, doc.sections[1].headers_footers))))
# I den tredje sektionen är endast footern länkad till den första sektionens footer via den andra sektionen.
self.assertEqual(6, doc.sections[2].headers_footers.count)
self.assertEqual(5, len(list(filter(lambda hf: not hf.as_header_footer().is_linked_to_previous, doc.sections[2].headers_footers))))
self.assertTrue(doc.sections[2].headers_footers[3].is_linked_to_previous)
doc.save(file_name=ARTIFACTS_DIR + 'HeaderFooter.Link.docx')
```

## See Also

* module [aspose.words](../../)
* class [HeaderFooterCollection](../)

