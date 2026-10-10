---
title: Paragraph.join_runs_with_same_formatting method
linktitle: join_runs_with_same_formatting method
articleTitle: join_runs_with_same_formatting method
second_title: Aspose.Words for Python
description: "aspose.words.Paragraph.join_runs_with_same_formatting method"
type: docs
weight: 300
url: /ru/python-net/aspose.words/paragraph/join_runs_with_same_formatting/
---

## join_runs_with_same_formatting() {#default}

Joins runs with the same formatting in the paragraph.


```python
def join_runs_with_same_formatting(self):
    ...
```

### Returns

Number of joins performed. When **N** adjacent runs are being joined they count as **N - 1** joins.


## join_runs_with_same_formatting(options) {#joinrunsoptions}

Joins runs with the same formatting in the paragraph.


```python
def join_runs_with_same_formatting(self, options: aspose.words.JoinRunsOptions):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| options | [JoinRunsOptions](../../joinrunsoptions/) | Additional options |

### Returns

Number of joins performed. When **N** adjacent runs are being joined they count as **N - 1** joins.


## Examples

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

## See Also

* module [aspose.words](../../)
* class [Paragraph](../)

