---
title: PageSetup.line_number_restart_mode property
linktitle: line_number_restart_mode property
articleTitle: line_number_restart_mode property
second_title: Aspose.Words for Python
description: "PageSetup.line_number_restart_mode property. Gets or sets the way line numbering runs  that is, whether it starts over at the beginning of a new page or section or runs continuously."
type: docs
weight: 230
url: /ru/python-net/aspose.words/pagesetup/line_number_restart_mode/
---

## PageSetup.line_number_restart_mode property

Gets or sets the way line numbering runs  that is, whether it starts over at the beginning of a new
page or section or runs continuously.


```python
@property
def line_number_restart_mode(self) -> aspose.words.LineNumberRestartMode:
    ...

@line_number_restart_mode.setter
def line_number_restart_mode(self, value: aspose.words.LineNumberRestartMode):
    ...

```

### Examples

Shows how to enable line numbering for a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Мы можем использовать объект PageSetup раздела, чтобы отображать номера слева от строк текста раздела.
# Это то же поведение, что и у объекта List,
# но он охватывает весь раздел и не изменяет текст никоим образом.
# Наш раздел будет перезапускать нумерацию на каждой новой странице с 1 и отображать номер,
# если он кратен 3, на 50pt слева от строки.
page_setup = builder.page_setup
page_setup.line_starting_number = 1
page_setup.line_number_count_by = 3
page_setup.line_number_restart_mode = aw.LineNumberRestartMode.RESTART_PAGE
page_setup.line_number_distance_from_text = 50
i = 1
while i <= 25:
    builder.writeln(f'Line {i}.')
    i += 1
# Счётчик строк будет пропускать любой абзац с флагом "SuppressLineNumbers", установленным в "true".
# Этот абзац находится на 15‑й строке, которая кратна 3, и поэтому обычно отображал бы номер строки.
# Счётчик строк раздела также будет игнорировать эту строку, считать следующую строку 15‑й,
# и продолжать подсчёт с этой точки дальше.
doc.first_section.body.paragraphs[14].paragraph_format.suppress_line_numbers = True
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.LineNumbers.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

