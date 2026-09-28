---
title: LineNumberRestartMode enumeration
linktitle: LineNumberRestartMode enumeration
articleTitle: LineNumberRestartMode enumeration
second_title: Aspose.Words for Python
description: "aspose.words.LineNumberRestartMode enumeration. Determines when automatic line numbering restarts."
type: docs
weight: 720
url: /de/python-net/aspose.words/linenumberrestartmode/
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

* module [aspose.words](../)
* class [PageSetup](../pagesetup/)
* property [PageSetup.line_number_restart_mode](../pagesetup/line_number_restart_mode/)

