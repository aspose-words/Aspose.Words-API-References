---
title: ParagraphFormat.suppress_line_numbers property
linktitle: suppress_line_numbers property
articleTitle: suppress_line_numbers property
second_title: Aspose.Words for Python
description: "ParagraphFormat.suppress_line_numbers property. Specifies whether the current paragraph's lines should be exempted from line numbering which is applied in the parent section."
type: docs
weight: 390
url: /zh/python-net/aspose.words/paragraphformat/suppress_line_numbers/
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
# 我们可以使用节的 PageSetup 对象在节的文本行左侧显示编号。
# 这与 List 对象的行为相同，
# 但它覆盖整个节且不以任何方式修改文本。
# 我们的节将在每个新页面上从 1 重新开始编号并显示该编号，
# 如果它是 3 的倍数，则在行左侧 50pt 处显示。
page_setup = builder.page_setup
page_setup.line_starting_number = 1
page_setup.line_number_count_by = 3
page_setup.line_number_restart_mode = aw.LineNumberRestartMode.RESTART_PAGE
page_setup.line_number_distance_from_text = 50
i = 1
while i <= 25:
    builder.writeln(f'Line {i}.')
    i += 1
# 行计数器将跳过任何将 "SuppressLineNumbers" 标志设置为 "true" 的段落。
# 此段落位于第 15 行，是 3 的倍数，因此通常会显示行号。
# 该节的行计数器也会忽略此行，将下一行视为第15行，
# 并从该点继续计数。
doc.first_section.body.paragraphs[14].paragraph_format.suppress_line_numbers = True
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.LineNumbers.docx')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

