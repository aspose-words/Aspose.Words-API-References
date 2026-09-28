---
title: Paragraph.join_runs_with_same_formatting method
linktitle: join_runs_with_same_formatting method
articleTitle: join_runs_with_same_formatting method
second_title: Aspose.Words for Python
description: "aspose.words.Paragraph.join_runs_with_same_formatting method"
type: docs
weight: 300
url: /ar/python-net/aspose.words/paragraph/join_runs_with_same_formatting/
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
# أنشئ مقاطع نصية بتنسيق مرئي متطابق لكن مع بعض الاختلافات الداخلية.
builder.font.name = 'Arial'
builder.font.size = 12
builder.write('Hello ')
builder.write('world')
# تحقق من المقاطع قبل الدمج.
self.assertEqual(2, doc.first_section.body.first_paragraph.runs.count)
self.assertEqual('Hello ', doc.first_section.body.first_paragraph.runs[0].text)
self.assertEqual('world', doc.first_section.body.first_paragraph.runs[1].text)
# قم بتكوين الخيارات لتجاهل السمات الزائدة وغير المهمة أثناء الدمج.
options = aw.JoinRunsOptions()
options.ignore_redundant = True  # Ignore redundant run properties that don't affect appearance.
options.ignore_insignificant = True  # Ignore insignificant differences like whitespace-only runs.
# ادمج المقاطع التي لها نفس التنسيق المرئي باستخدام الخيارات الموسعة.
doc.first_section.body.first_paragraph.join_runs_with_same_formatting(options)
# تحقق من أن المقاطع تم ربطها بنجاح.
self.assertEqual(1, doc.first_section.body.first_paragraph.runs.count)
self.assertEqual('Hello world', doc.first_section.body.first_paragraph.runs[0].text)
doc.save(file_name=ARTIFACTS_DIR + 'Paragraph.JoinRunsWithSameFormattingWithOptions.docx')
```

## See Also

* module [aspose.words](../../)
* class [Paragraph](../)

