---
title: HeaderFooterCollection.link_to_previous method
linktitle: link_to_previous method
articleTitle: link_to_previous method
second_title: Aspose.Words for Python
description: "aspose.words.HeaderFooterCollection.link_to_previous method"
type: docs
weight: 90
url: /it/python-net/aspose.words/headerfootercollection/link_to_previous/
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
# Passa alla prima sezione e crea un'intestazione e un piè di pagina. Per impostazione predefinita,
# l'intestazione e il piè di pagina appariranno solo nelle pagine della sezione che li contiene.
builder.move_to_section(0)
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.write('This is the header, which will be displayed in sections 1 and 2.')
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
builder.write('This is the footer, which will be displayed in sections 1, 2 and 3.')
# Possiamo collegare le intestazioni/piè di pagina di una sezione a quelle della sezione precedente
# per consentire alla sezione di collegamento di visualizzare le intestazioni/piè di pagina della sezione collegata.
doc.sections[1].headers_footers.link_to_previous(is_link_to_previous=True)
# Ogni sezione avrà comunque i propri oggetti di intestazione/piè di pagina. Quando colleghiamo le sezioni,
# la sezione di collegamento visualizzerà le intestazioni/piè di pagina della sezione collegata mantenendo le proprie.
assert doc.sections[0].headers_footers[0] is not doc.sections[1].headers_footers[0]
assert doc.sections[0].headers_footers[0].parent_section is not doc.sections[1].headers_footers[0].parent_section
# Collega le intestazioni/piè di pagina della terza sezione a quelle della seconda sezione.
# La seconda sezione è già collegata alle intestazioni/piè di pagina della prima sezione,
# quindi collegare alla seconda sezione creerà una catena di collegamenti.
# La prima, la seconda e ora la terza sezione visualizzeranno tutte le intestazioni della prima sezione.
doc.sections[2].headers_footers.link_to_previous(is_link_to_previous=True)
# Possiamo scollegare le intestazioni/piè di pagina di una sezione precedente passando "false" quando si chiama il metodo LinkToPrevious.
doc.sections[2].headers_footers.link_to_previous(is_link_to_previous=False)
# Possiamo anche selezionare solo un tipo specifico di intestazione/piè di pagina da collegare usando questo metodo.
# La terza sezione ora avrà lo stesso piè di pagina delle seconde e prime sezioni, ma non l'intestazione.
doc.sections[2].headers_footers.link_to_previous(header_footer_type=aw.HeaderFooterType.FOOTER_PRIMARY, is_link_to_previous=True)
# Le intestazioni/piè di pagina della prima sezione non possono collegarsi a nulla perché non esiste una sezione precedente.
self.assertEqual(2, doc.sections[0].headers_footers.count)
self.assertEqual(2, len(list(filter(lambda hf: not hf.as_header_footer().is_linked_to_previous, doc.sections[0].headers_footers))))
# Tutte le intestazioni/piè di pagina della seconda sezione sono collegate alle intestazioni/piè di pagina della prima sezione.
self.assertEqual(6, doc.sections[1].headers_footers.count)
self.assertEqual(6, len(list(filter(lambda hf: hf.as_header_footer().is_linked_to_previous, doc.sections[1].headers_footers))))
# Nella terza sezione, solo il piè di pagina è collegato al piè di pagina della prima sezione tramite la seconda sezione.
self.assertEqual(6, doc.sections[2].headers_footers.count)
self.assertEqual(5, len(list(filter(lambda hf: not hf.as_header_footer().is_linked_to_previous, doc.sections[2].headers_footers))))
self.assertTrue(doc.sections[2].headers_footers[3].is_linked_to_previous)
doc.save(file_name=ARTIFACTS_DIR + 'HeaderFooter.Link.docx')
```

## See Also

* module [aspose.words](../../)
* class [HeaderFooterCollection](../)

