---
title: TxtSaveOptionsBase.paragraph_break property
linktitle: paragraph_break property
articleTitle: paragraph_break property
second_title: Aspose.Words for Python
description: "TxtSaveOptionsBase.paragraph_break property. Specifies the string to use as a paragraph break when exporting in text formats."
type: docs
weight: 40
url: /zh/python-net/aspose.words.saving/txtsaveoptionsbase/paragraph_break/
---

## TxtSaveOptionsBase.paragraph_break property

Specifies the string to use as a paragraph break when exporting in text formats.


```python
@property
def paragraph_break(self) -> str:
    ...

@paragraph_break.setter
def paragraph_break(self, value: str):
    ...

```

### Remarks

The default value is [ControlChar.CR_LF](../../../aspose.words/controlchar/CR_LF/).




### Examples

Shows how to save a .txt document with a custom paragraph break.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Paragraph 1.')
builder.writeln('Paragraph 2.')
builder.write('Paragraph 3.')
# 创建一个 "TxtSaveOptions" 对象，我们可以将其传递给文档的 "Save" 方法
# 以修改我们将文档保存为纯文本的方式。
txt_save_options = aw.saving.TxtSaveOptions()
self.assertEqual(aw.SaveFormat.TEXT, txt_save_options.save_format)
# 将 "ParagraphBreak" 设置为我们希望放在每段末尾的自定义值。
txt_save_options.paragraph_break = ' End of paragraph.\n\n\t'
doc.save(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.ParagraphBreak.txt', save_options=txt_save_options)
doc_text = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'TxtSaveOptions.ParagraphBreak.txt')
self.assertEqual('Paragraph 1. End of paragraph.\n\n\t' + 'Paragraph 2. End of paragraph.\n\n\t' + 'Paragraph 3. End of paragraph.\n\n\t', doc_text)
```

### See Also

* module [aspose.words.saving](../../)
* class [TxtSaveOptionsBase](../)

