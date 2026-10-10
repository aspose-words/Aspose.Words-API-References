---
title: Document.spelling_checked property
linktitle: spelling_checked property
articleTitle: spelling_checked property
second_title: Aspose.Words for Python
description: "Document.spelling_checked property. Returns ``True`` if the document has been checked for spelling."
type: docs
weight: 440
url: /zh/python-net/aspose.words/document/spelling_checked/
---

## Document.spelling_checked property

Returns ``True`` if the document has been checked for spelling.



```python
@property
def spelling_checked(self) -> bool:
    ...

@spelling_checked.setter
def spelling_checked(self, value: bool):
    ...

```

### Remarks

To recheck the spelling in the document, set this property to ``False``.



### Examples

Shows how to set spelling or grammar verifying.

```python
doc = aw.Document()
# 带有拼写错误的字符串。
doc.first_section.body.first_paragraph.runs.add(aw.Run(doc=doc, text='The speeling in this documentz is all broked.'))
# 如果我们将属性设置为 false，拼写/语法检查将启动。
# 我们可以在 Microsoft Word 中通过 Review -> Spelling & Grammar 查看所有错误。
# 请注意，Microsoft Word 不会自动对 DOC 和 RTF 文档格式启动语法/拼写检查。
doc.spelling_checked = check_spelling_grammar
doc.grammar_checked = check_spelling_grammar
doc.save(file_name=ARTIFACTS_DIR + 'Document.SpellingOrGrammar.docx')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

