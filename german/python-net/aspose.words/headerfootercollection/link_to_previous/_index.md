---
title: HeaderFooterCollection.link_to_previous method
linktitle: link_to_previous method
articleTitle: link_to_previous method
second_title: Aspose.Words for Python
description: "aspose.words.HeaderFooterCollection.link_to_previous method"
type: docs
weight: 90
url: /de/python-net/aspose.words/headerfootercollection/link_to_previous/
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
# Wechseln Sie zum ersten Abschnitt und erstellen Sie eine Kopfzeile und eine Fußzeile. Standardmäßig,
# werden die Kopfzeile und die Fußzeile nur auf den Seiten des Abschnitts angezeigt, der sie enthält.
builder.move_to_section(0)
builder.move_to_header_footer(aw.HeaderFooterType.HEADER_PRIMARY)
builder.write('This is the header, which will be displayed in sections 1 and 2.')
builder.move_to_header_footer(aw.HeaderFooterType.FOOTER_PRIMARY)
builder.write('This is the footer, which will be displayed in sections 1, 2 and 3.')
# Wir können die Kopfzeilen/Fußzeilen eines Abschnitts mit den Kopfzeilen/Fußzeilen des vorherigen Abschnitts verknüpfen
# um dem verknüpften Abschnitt zu ermöglichen, die Kopfzeilen/Fußzeilen des verknüpften Abschnitts anzuzeigen.
doc.sections[1].headers_footers.link_to_previous(is_link_to_previous=True)
# Jeder Abschnitt hat weiterhin seine eigenen Kopfzeilen-/Fußzeilen-Objekte. Wenn wir Abschnitte verknüpfen,
# zeigt der verknüpfende Abschnitt die Kopfzeilen/Fußzeilen des verknüpften Abschnitts an, während er seine eigenen beibehält.
assert doc.sections[0].headers_footers[0] is not doc.sections[1].headers_footers[0]
assert doc.sections[0].headers_footers[0].parent_section is not doc.sections[1].headers_footers[0].parent_section
# Verknüpfen Sie die Kopfzeilen/Fußzeilen des dritten Abschnitts mit den Kopfzeilen/Fußzeilen des zweiten Abschnitts.
# Der zweite Abschnitt ist bereits mit den Kopfzeilen/Fußzeilen des ersten Abschnitts verknüpft,
# so führt das Verknüpfen mit dem zweiten Abschnitt zu einer Verknüpfungskette.
# Der erste, zweite und nun der dritte Abschnitt werden alle die Kopfzeilen des ersten Abschnitts anzeigen.
doc.sections[2].headers_footers.link_to_previous(is_link_to_previous=True)
# Wir können die Kopfzeilen/Fußzeilen eines vorherigen Abschnitts durch Übergabe von "false" beim Aufruf der Methode LinkToPrevious entknüpfen.
doc.sections[2].headers_footers.link_to_previous(is_link_to_previous=False)
# Wir können außerdem nur einen bestimmten Typ von Kopfzeile/Fußzeile auswählen, um ihn mit dieser Methode zu verknüpfen.
# Der dritte Abschnitt wird nun dieselbe Fußzeile wie der zweite und erste Abschnitt haben, jedoch nicht dieselbe Kopfzeile.
doc.sections[2].headers_footers.link_to_previous(header_footer_type=aw.HeaderFooterType.FOOTER_PRIMARY, is_link_to_previous=True)
# Die Kopf-/Fußzeilen des ersten Abschnitts können sich zu nichts verlinken, weil es keinen vorherigen Abschnitt gibt.
self.assertEqual(2, doc.sections[0].headers_footers.count)
self.assertEqual(2, len(list(filter(lambda hf: not hf.as_header_footer().is_linked_to_previous, doc.sections[0].headers_footers))))
# Alle Kopf-/Fußzeilen des zweiten Abschnitts sind mit den Kopf-/Fußzeilen des ersten Abschnitts verknüpft.
self.assertEqual(6, doc.sections[1].headers_footers.count)
self.assertEqual(6, len(list(filter(lambda hf: hf.as_header_footer().is_linked_to_previous, doc.sections[1].headers_footers))))
# Im dritten Abschnitt ist nur die Fußzeile über den zweiten Abschnitt mit der Fußzeile des ersten Abschnitts verknüpft.
self.assertEqual(6, doc.sections[2].headers_footers.count)
self.assertEqual(5, len(list(filter(lambda hf: not hf.as_header_footer().is_linked_to_previous, doc.sections[2].headers_footers))))
self.assertTrue(doc.sections[2].headers_footers[3].is_linked_to_previous)
doc.save(file_name=ARTIFACTS_DIR + 'HeaderFooter.Link.docx')
```

## See Also

* module [aspose.words](../../)
* class [HeaderFooterCollection](../)

