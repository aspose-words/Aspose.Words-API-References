---
title: ParagraphFormat.suppress_line_numbers property
linktitle: suppress_line_numbers property
articleTitle: suppress_line_numbers property
second_title: Aspose.Words for Python
description: "ParagraphFormat.suppress_line_numbers property. Specifies whether the current paragraph's lines should be exempted from line numbering which is applied in the parent section."
type: docs
weight: 390
url: /es/python-net/aspose.words/paragraphformat/suppress_line_numbers/
---

## ParagraphFormat.suppress_line_numbers property

Specifies whether the current paragraph's lines should be exempted from line numbering
which is applied in the parent section.


```python
@property
def suppress_line_numbers(self) -> bool:
    ...

@suppress_line_numbers.setter
def suppress_line_numbers(self, value: bool):
    ...

```

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

* module [aspose.words](../../)
* class [ParagraphFormat](../)

