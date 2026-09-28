---
title: FindReplaceOptions.ignore_fields property
linktitle: ignore_fields property
articleTitle: ignore_fields property
second_title: Aspose.Words for Python
description: "FindReplaceOptions.ignore_fields property. Gets or sets a boolean value indicating either to ignore text inside fields"
type: docs
weight: 80
url: /zh/python-net/aspose.words.replacing/findreplaceoptions/ignore_fields/
---

## FindReplaceOptions.ignore_fields property

Gets or sets a boolean value indicating either to ignore text inside fields.
The default value is ``False``.



```python
@property
def ignore_fields(self) -> bool:
    ...

@ignore_fields.setter
def ignore_fields(self, value: bool):
    ...

```

### Remarks

This option affects whole field (all nodes between
[NodeType.FIELD_START](../../../aspose.words/nodetype/#FIELD_START) and [NodeType.FIELD_END](../../../aspose.words/nodetype/#FIELD_END)).

To ignore only field codes, please use corresponding option [FindReplaceOptions.ignore_field_codes](../ignore_field_codes/).




### Examples

Shows how to ignore text inside fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
builder.insert_field(field_code='QUOTE', field_value='Hello again!')
# 我们可以使用 "FindReplaceOptions" 对象来修改查找替换过程。
options = aw.replacing.FindReplaceOptions()
# 将 "IgnoreFields" 标志设置为 "true" 以获取查找和替换
# 操作以忽略字段中的文本。
# 将 "IgnoreFields" 标志设置为 "false" 以获取查找和替换
# 操作以同时搜索字段中的文本。
options.ignore_fields = ignore_text_inside_fields
doc.range.replace(pattern='Hello', replacement='Greetings', options=options)
self.assertEqual('Greetings world!\r\x13QUOTE\x14Hello again!\x15' if ignore_text_inside_fields else 'Greetings world!\r\x13QUOTE\x14Greetings again!\x15', doc.get_text().strip())
```

### See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)

