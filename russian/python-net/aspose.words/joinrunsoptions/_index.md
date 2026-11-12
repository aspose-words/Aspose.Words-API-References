---
title: JoinRunsOptions class
linktitle: JoinRunsOptions class
articleTitle: JoinRunsOptions class
second_title: Aspose.Words for Python
description: "aspose.words.JoinRunsOptions class. Provides configuration flags for the join runs operation."
type: docs
weight: 700
url: /ru/python-net/aspose.words/joinrunsoptions/
---

## JoinRunsOptions class

Provides configuration flags for the join runs operation.


### Constructors
| Name | Description |
| --- | --- |
| [JoinRunsOptions()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [ignore_insignificant](./ignore_insignificant/) | True indicates that the insignificant attributes of all runs will be ignored when joining runs with same formatting. |
| [ignore_redundant](./ignore_redundant/) | True indicates that the redundant attributes of all runs will be ignored when joining runs with same formatting. |
| [ignore_spacing](./ignore_spacing/) | True indicates that the spacing attributes of all runs will be ignored when joining runs with same formatting. |

### Examples

Shows how to join runs with the same formatting while ignoring redundant and insignificant attributes.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Создайте участки (runs) с одинаковым видимым форматированием, но с некоторыми внутренними различиями.
builder.font.name = 'Arial'
builder.font.size = 12
builder.write('Hello ')
builder.write('world')
# Проверьте участки перед объединением.
self.assertEqual(2, doc.first_section.body.first_paragraph.runs.count)
self.assertEqual('Hello ', doc.first_section.body.first_paragraph.runs[0].text)
self.assertEqual('world', doc.first_section.body.first_paragraph.runs[1].text)
# Настройте параметры, чтобы игнорировать избыточные и незначительные атрибуты во время объединения.
options = aw.JoinRunsOptions()
options.ignore_redundant = True  # Ignore redundant run properties that don't affect appearance.
options.ignore_insignificant = True  # Ignore insignificant differences like whitespace-only runs.
# Объедините участки, имеющие одинаковое видимое форматирование, используя расширенные параметры.
doc.first_section.body.first_paragraph.join_runs_with_same_formatting(options)
# Проверьте, что пробеги были успешно объединены.
self.assertEqual(1, doc.first_section.body.first_paragraph.runs.count)
self.assertEqual('Hello world', doc.first_section.body.first_paragraph.runs[0].text)
doc.save(file_name=ARTIFACTS_DIR + 'Paragraph.JoinRunsWithSameFormattingWithOptions.docx')
```

### See Also

* module [aspose.words](../)

