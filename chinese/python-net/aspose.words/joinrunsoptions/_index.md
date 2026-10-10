---
title: JoinRunsOptions class
linktitle: JoinRunsOptions class
articleTitle: JoinRunsOptions class
second_title: Aspose.Words for Python
description: "aspose.words.JoinRunsOptions class. Provides configuration flags for the join runs operation."
type: docs
weight: 700
url: /zh/python-net/aspose.words/joinrunsoptions/
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
# 创建具有相同可见格式但内部有些差异的运行。
builder.font.name = 'Arial'
builder.font.size = 12
builder.write('Hello ')
builder.write('world')
# 在合并之前验证运行。
self.assertEqual(2, doc.first_section.body.first_paragraph.runs.count)
self.assertEqual('Hello ', doc.first_section.body.first_paragraph.runs[0].text)
self.assertEqual('world', doc.first_section.body.first_paragraph.runs[1].text)
# 配置选项以在合并期间忽略冗余和不重要的属性。
options = aw.JoinRunsOptions()
options.ignore_redundant = True  # Ignore redundant run properties that don't affect appearance.
options.ignore_insignificant = True  # Ignore insignificant differences like whitespace-only runs.
# 使用扩展选项合并具有相同可见格式的运行。
doc.first_section.body.first_paragraph.join_runs_with_same_formatting(options)
# 验证运行已成功连接。
self.assertEqual(1, doc.first_section.body.first_paragraph.runs.count)
self.assertEqual('Hello world', doc.first_section.body.first_paragraph.runs[0].text)
doc.save(file_name=ARTIFACTS_DIR + 'Paragraph.JoinRunsWithSameFormattingWithOptions.docx')
```

### See Also

* module [aspose.words](../)

