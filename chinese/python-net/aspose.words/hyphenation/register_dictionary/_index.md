---
title: Hyphenation.register_dictionary method
linktitle: register_dictionary method
articleTitle: register_dictionary method
second_title: Aspose.Words for Python
description: "aspose.words.Hyphenation.register_dictionary method"
type: docs
weight: 40
url: /zh/python-net/aspose.words/hyphenation/register_dictionary/
---

## register_dictionary(language, stream) {#str_bytesio}

Registers and loads a hyphenation dictionary for the specified language from a stream. Throws if dictionary cannot be read or has invalid format.


```python
def register_dictionary(self, language: str, stream: io.BytesIO):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| language | str | A language name, e.g. "en-US". See .NET documentation for "culture name" and RFC 4646 for details. |
| stream | io.BytesIO | A stream for the dictionary file in OpenOffice format. |

## register_dictionary(language, file_name) {#str_str}

Registers and loads a hyphenation dictionary for the specified language from file. Throws if dictionary cannot be read or has invalid format.


This method can also be used to register Null dictionary to prevent[Hyphenation.callback](../callback/) from being called repeatedly for the same language.



```python
def register_dictionary(self, language: str, file_name: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| language | str | A language name, e.g. "en-US". See .NET documentation for "culture name" and RFC 4646 for details. |
| file_name | str | A path to the dictionary file in Open Office format. |

## Examples

Shows how to register a hyphenation dictionary.

```python
# 连字符字典包含一系列字符串，用于定义该字典语言的连字符规则。
# 当文档包含的文本行中出现可以拆分并在下一行继续的单词时，
# 连字符功能会在字典的字符串列表中查找该单词的子串。
# 如果字典包含该子串，连字符功能将把单词拆分到两行
# 在该子串处拆分，并在前半部分添加连字符。
# 将本地文件系统中的字典文件注册到 "de-CH" 区域设置。
aw.Hyphenation.register_dictionary('de-CH', MY_DIR + 'hyph_de_CH.dic')
self.assertTrue(aw.Hyphenation.is_dictionary_registered('de-CH'))
# 打开一个文本的区域设置与我们的字典匹配的文档，
# 并将其保存为固定页保存格式。该文档中的文本将被连字符处理。
doc = aw.Document(MY_DIR + 'German text.docx')
self.assertTrue(all((node for node in doc.first_section.body.first_paragraph.runs if node.as_run().font.locale_id == 2055)))
doc.save(ARTIFACTS_DIR + 'Hyphenation.dictionary.registered.pdf')
# 在取消注册字典后重新加载文档，
# 并将其保存为另一个 PDF，该 PDF 将不包含连字符文本。
aw.Hyphenation.unregister_dictionary('de-CH')
self.assertFalse(aw.Hyphenation.is_dictionary_registered('de-CH'))
doc = aw.Document(MY_DIR + 'German text.docx')
doc.save(ARTIFACTS_DIR + 'Hyphenation.dictionary.unregistered.pdf')
```

## See Also

* module [aspose.words](../../)
* class [Hyphenation](../)

