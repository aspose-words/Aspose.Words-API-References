---
title: TxtLoadOptions.detect_numbering_with_whitespaces property
linktitle: detect_numbering_with_whitespaces property
articleTitle: detect_numbering_with_whitespaces property
second_title: Aspose.Words for Python
description: "TxtLoadOptions.detect_numbering_with_whitespaces property. Allows to specify how numbered list items are recognized when document is imported from plain text format"
type: docs
weight: 40
url: /sv/python-net/aspose.words.loading/txtloadoptions/detect_numbering_with_whitespaces/
---

## TxtLoadOptions.detect_numbering_with_whitespaces property

Allows to specify how numbered list items are recognized when document is imported from plain text format.
The default value is ``True``.


```python
@property
def detect_numbering_with_whitespaces(self) -> bool:
    ...

@detect_numbering_with_whitespaces.setter
def detect_numbering_with_whitespaces(self, value: bool):
    ...

```

### Remarks

If this option is set to ``False``, lists recognition algorithm detects list paragraphs, when list numbers ends with
either dot, right bracket or bullet symbols (such as "•", "\*", "-" or "o").

If this option is set to ``True``, whitespaces are also used as list number delimiters:
list recognition algorithm for Arabic style numbering (1., 1.1.2.) uses both whitespaces and dot (".") symbols.




### Examples

Shows how to detect lists when loading plaintext documents.

```python
# Skapa ett klartextdokument i en sträng med fyra separata delar som vi kan tolka som listor,
# med olika avgränsare. Vid inläsning av klartextdokumentet i ett "Document"-objekt,
# Aspose.Words kommer alltid att upptäcka de första tre listorna och kommer att lägga till ett "List"-objekt
# för varje till dokumentets "Lists"-egenskap.
text_doc = 'Full stop delimiters:\n' + '1. First list item 1\n' + '2. First list item 2\n' + '3. First list item 3\n\n' + 'Right bracket delimiters:\n' + '1) Second list item 1\n' + '2) Second list item 2\n' + '3) Second list item 3\n\n' + 'Bullet delimiters:\n' + '• Third list item 1\n' + '• Third list item 2\n' + '• Third list item 3\n\n' + 'Whitespace delimiters:\n' + '1 Fourth list item 1\n' + '2 Fourth list item 2\n' + '3 Fourth list item 3'
# Skapa ett "TxtLoadOptions"‑objekt, som vi kan skicka till ett dokuments konstruktor
# för att ändra hur vi laddar ett klartext‑dokument.
load_options = aw.loading.TxtLoadOptions()
# Ställ in egenskapen "DetectNumberingWithWhitespaces" till "true" för att upptäcka numrerade objekt
# med avgränsare av mellanslag, såsom den fjärde listan i vårt dokument, som listor.
# Detta kan också felaktigt upptäcka stycken som börjar med siffror som listor.
# Ställ in egenskapen "DetectNumberingWithWhitespaces" till "false"
# för att inte skapa listor från numrerade objekt med avgränsare av mellanslag.
load_options.detect_numbering_with_whitespaces = detect_numbering_with_whitespaces
doc = aw.Document(stream=io.BytesIO(system_helper.text.Encoding.get_bytes(text_doc, system_helper.text.Encoding.utf_8())), load_options=load_options)
if detect_numbering_with_whitespaces:
    self.assertEqual(4, doc.lists.count)
    self.assertTrue(any(['Fourth list' in p.get_text() and p.as_paragraph().is_list_item for p in doc.first_section.body.paragraphs]))
else:
    self.assertEqual(3, doc.lists.count)
    self.assertFalse(any(['Fourth list' in p.get_text() and p.as_paragraph().is_list_item for p in doc.first_section.body.paragraphs]))
```

### See Also

* module [aspose.words.loading](../../)
* class [TxtLoadOptions](../)

