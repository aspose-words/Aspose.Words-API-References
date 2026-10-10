---
title: ParagraphFormat.suppress_line_numbers property
linktitle: suppress_line_numbers property
articleTitle: suppress_line_numbers property
second_title: Aspose.Words for Python
description: "ParagraphFormat.suppress_line_numbers property. Specifies whether the current paragraph's lines should be exempted from line numbering which is applied in the parent section."
type: docs
weight: 390
url: /de/python-net/aspose.words/paragraphformat/suppress_line_numbers/
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
# Wir können das PageSetup‑Objekt des Abschnitts verwenden, um Zahlen links von den Textzeilen des Abschnitts anzuzeigen.
# Dies ist das gleiche Verhalten wie bei einem List‑Objekt,
# aber es deckt den gesamten Abschnitt ab und verändert den Text in keiner Weise.
# Unser Abschnitt wird die Nummerierung auf jeder neuen Seite bei 1 neu starten und die Nummer anzeigen,
# wenn sie ein Vielfaches von 3 ist, 50 pt links von der Zeile.
page_setup = builder.page_setup
page_setup.line_starting_number = 1
page_setup.line_number_count_by = 3
page_setup.line_number_restart_mode = aw.LineNumberRestartMode.RESTART_PAGE
page_setup.line_number_distance_from_text = 50
i = 1
while i <= 25:
    builder.writeln(f'Line {i}.')
    i += 1
# Der Zeilenzähler überspringt jeden Absatz, bei dem das Flag "SuppressLineNumbers" auf "true" gesetzt ist.
# Dieser Absatz befindet sich in der 15. Zeile, die ein Vielfaches von 3 ist, und würde daher normalerweise eine Zeilennummer anzeigen.
# Der Zeilenzähler des Abschnitts wird diese Zeile ebenfalls ignorieren, die nächste Zeile als die 15. behandeln,
# und den Zähler von diesem Punkt an weiterführen.
doc.first_section.body.paragraphs[14].paragraph_format.suppress_line_numbers = True
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.LineNumbers.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

