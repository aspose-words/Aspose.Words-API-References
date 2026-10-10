---
title: PageSetup.line_number_count_by property
linktitle: line_number_count_by property
articleTitle: line_number_count_by property
second_title: Aspose.Words for Python
description: "PageSetup.line_number_count_by property. Returns or sets the numeric increment for line numbers."
type: docs
weight: 210
url: /it/python-net/aspose.words/pagesetup/line_number_count_by/
---

## PageSetup.line_number_count_by property

Returns or sets the numeric increment for line numbers.


```python
@property
def line_number_count_by(self) -> int:
    ...

@line_number_count_by.setter
def line_number_count_by(self, value: int):
    ...

```

### Examples

Shows how to enable line numbering for a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Possiamo usare l'oggetto PageSetup della sezione per visualizzare i numeri a sinistra delle righe di testo della sezione.
# Questo è lo stesso comportamento di un oggetto List,
# ma copre l'intera sezione e non modifica il testo in alcun modo.
# La nostra sezione ricomincerà la numerazione su ogni nuova pagina da 1 e visualizzerà il numero,
# se è un multiplo di 3, a 50pt a sinistra della riga.
page_setup = builder.page_setup
page_setup.line_starting_number = 1
page_setup.line_number_count_by = 3
page_setup.line_number_restart_mode = aw.LineNumberRestartMode.RESTART_PAGE
page_setup.line_number_distance_from_text = 50
i = 1
while i <= 25:
    builder.writeln(f'Line {i}.')
    i += 1
# Il contatore di righe salterà qualsiasi paragrafo con il flag "SuppressLineNumbers" impostato su "true".
# Questo paragrafo è sulla 15ª riga, che è un multiplo di 3, e quindi normalmente visualizzerebbe un numero di riga.
# Il contatore di righe della sezione ignorerà anche questa riga, considera la riga successiva come la 15ª,
# e continua il conteggio da quel punto in poi.
doc.first_section.body.paragraphs[14].paragraph_format.suppress_line_numbers = True
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.LineNumbers.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

