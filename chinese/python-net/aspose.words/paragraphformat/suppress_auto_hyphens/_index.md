---
title: ParagraphFormat.suppress_auto_hyphens property
linktitle: suppress_auto_hyphens property
articleTitle: suppress_auto_hyphens property
second_title: Aspose.Words for Python
description: "ParagraphFormat.suppress_auto_hyphens property. Specifies whether the current paragraph should be exempted from any hyphenation which is applied in the document settings."
type: docs
weight: 380
url: /zh/python-net/aspose.words/paragraphformat/suppress_auto_hyphens/
---

## ParagraphFormat.suppress_auto_hyphens property

Specifies whether the current paragraph should be exempted from any hyphenation which
is applied in the document settings.


```python
@property
def suppress_auto_hyphens(self) -> bool:
    ...

@suppress_auto_hyphens.setter
def suppress_auto_hyphens(self, value: bool):
    ...

```

### Examples

Shows how to suppress hyphenation for a paragraph.

```python
aw.Hyphenation.register_dictionary(language='de-CH', file_name=MY_DIR + 'hyph_de_CH.dic')
self.assertTrue(aw.Hyphenation.is_dictionary_registered('de-CH'))
# 打开一个包含文本且区域设置与我们的词典匹配的文档。
# 当我们将此文档保存为固定页面格式时，其文本将出现连字符。
doc = aw.Document(file_name=MY_DIR + 'German text.docx')
# 我们可以将 "SuppressAutoHyphens" 属性设置为 "true" 来禁用连字符。
# 针对特定段落，同时保持其在文档其余部分仍然启用。
# 此属性的默认值为 "false"，
# 这意味着默认情况下，每个段落如果有可用的连字符就会使用。
doc.first_section.body.first_paragraph.paragraph_format.suppress_auto_hyphens = suppress_auto_hyphens
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.SuppressHyphens.pdf')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

