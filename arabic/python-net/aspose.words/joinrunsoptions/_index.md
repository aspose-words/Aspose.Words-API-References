---
title: JoinRunsOptions class
linktitle: JoinRunsOptions class
articleTitle: JoinRunsOptions class
second_title: Aspose.Words for Python
description: "aspose.words.JoinRunsOptions class. Provides configuration flags for the join runs operation."
type: docs
weight: 700
url: /ar/python-net/aspose.words/joinrunsoptions/
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

### See Also

* module [aspose.words](../)

