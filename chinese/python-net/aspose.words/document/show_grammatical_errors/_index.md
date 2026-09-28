---
title: Document.show_grammatical_errors property
linktitle: show_grammatical_errors property
articleTitle: show_grammatical_errors property
second_title: Aspose.Words for Python
description: "Document.show_grammatical_errors property. Specifies whether to display grammar errors in this document."
type: docs
weight: 420
url: /zh/python-net/aspose.words/document/show_grammatical_errors/
---

## Document.show_grammatical_errors property

Specifies whether to display grammar errors in this document.


```python
@property
def show_grammatical_errors(self) -> bool:
    ...

@show_grammatical_errors.setter
def show_grammatical_errors(self, value: bool):
    ...

```

### Examples

Shows how to show/hide errors in the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# 插入两句包含错误的句子，这些错误会被检测到
# 由 Microsoft Word 中的拼写和语法检查器检测到。
builder.writeln('There is a speling error in this sentence.')
builder.writeln('Their is a grammatical error in this sentence.')
# 如果启用这些选项，则拼写错误将被下划线标记
# 在输出文档中以锯齿形红线标记，并以双蓝线突出显示语法错误。
doc.show_grammatical_errors = show_errors
doc.show_spelling_errors = show_errors
doc.save(file_name=ARTIFACTS_DIR + 'Document.SpellingAndGrammarErrors.docx')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

