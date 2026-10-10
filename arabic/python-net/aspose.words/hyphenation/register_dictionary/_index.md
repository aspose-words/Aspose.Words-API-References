---
title: Hyphenation.register_dictionary method
linktitle: register_dictionary method
articleTitle: register_dictionary method
second_title: Aspose.Words for Python
description: "aspose.words.Hyphenation.register_dictionary method"
type: docs
weight: 40
url: /ar/python-net/aspose.words/hyphenation/register_dictionary/
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
# قاموس التجزئة يحتوي على قائمة من السلاسل التي تحدد قواعد التجزئة للغة القاموس.
# عندما يحتوي المستند على أسطر نصية يمكن فيها تقسيم كلمة ومتابعتها في السطر التالي،
# ستبحث التجزئة في قائمة السلاسل في القاموس عن أجزاء تلك الكلمة.
# إذا كان القاموس يحتوي على جزء من الكلمة، فإن التجزئة ستقسم الكلمة عبر سطرين
# بحسب الجزء وتضيف شرطة إلى النصف الأول.
# سجّل ملف القاموس من نظام الملفات المحلي إلى الإعداد المحلي "de-CH".
aw.Hyphenation.register_dictionary('de-CH', MY_DIR + 'hyph_de_CH.dic')
self.assertTrue(aw.Hyphenation.is_dictionary_registered('de-CH'))
# افتح مستندًا يحتوي على نص بإعداد محلي يطابق إعداد قاموسنا،
# واحفظه بصيغة حفظ ذات صفحة ثابتة. سيُجرى تجزئة النص في ذلك المستند.
doc = aw.Document(MY_DIR + 'German text.docx')
self.assertTrue(all((node for node in doc.first_section.body.first_paragraph.runs if node.as_run().font.locale_id == 2055)))
doc.save(ARTIFACTS_DIR + 'Hyphenation.dictionary.registered.pdf')
# أعد تحميل المستند بعد إلغاء تسجيل القاموس،
# واحفظه إلى ملف PDF آخر، والذي لن يحتوي على نص مجزّأ.
aw.Hyphenation.unregister_dictionary('de-CH')
self.assertFalse(aw.Hyphenation.is_dictionary_registered('de-CH'))
doc = aw.Document(MY_DIR + 'German text.docx')
doc.save(ARTIFACTS_DIR + 'Hyphenation.dictionary.unregistered.pdf')
```

## See Also

* module [aspose.words](../../)
* class [Hyphenation](../)

