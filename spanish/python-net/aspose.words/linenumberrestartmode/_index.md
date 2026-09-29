---
title: LineNumberRestartMode enumeration
linktitle: LineNumberRestartMode enumeration
articleTitle: LineNumberRestartMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.LineNumberRestartMode enumeration. Determines when automatic line numbering restarts."
type: docs
weight: 720
url: /es/python-net/aspose.words/linenumberrestartmode/
---

## LineNumberRestartMode enumeration

Determines when automatic line numbering restarts.


### Members

| Name | Description |
| --- | --- |
| RESTART_PAGE | Line numbering restarts at the start of every page. |
| RESTART_SECTION | Line numbering restarts at the section start. |
| CONTINUOUS | Line numbering continuous from the previous section. |

### Examples

Shows how to enable line numbering for a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Podemos usar el objeto PageSetup de la sección para mostrar números a la izquierda de las líneas de texto de la sección.
# Este es el mismo comportamiento que un objeto List,
# pero cubre toda la sección y no modifica el texto de ninguna manera.
# Nuestra sección reiniciará la numeración en cada página nueva desde 1 y mostrará el número,
# si es múltiplo de 3, a 50pt a la izquierda de la línea.
page_setup = builder.page_setup
page_setup.line_starting_number = 1
page_setup.line_number_count_by = 3
page_setup.line_number_restart_mode = aw.LineNumberRestartMode.RESTART_PAGE
page_setup.line_number_distance_from_text = 50
i = 1
while i <= 25:
    builder.writeln(f'Line {i}.')
    i += 1
# El contador de líneas omitirá cualquier párrafo con la bandera "SuppressLineNumbers" establecida en "true".
# Este párrafo está en la línea 15, que es múltiplo de 3, y por lo tanto normalmente mostraría un número de línea.
# The section's line counter will also ignore this line, treat the next line as the 15th,
# and continue the count from that point onward.
doc.first_section.body.paragraphs[14].paragraph_format.suppress_line_numbers = True
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.LineNumbers.docx')
```

### See Also

* module [aspose.words](../)
* class [PageSetup](../pagesetup/)
* property [PageSetup.line_number_restart_mode](../pagesetup/line_number_restart_mode/)

