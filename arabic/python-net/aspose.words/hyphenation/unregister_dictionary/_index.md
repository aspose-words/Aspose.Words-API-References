---
title: Hyphenation.unregister_dictionary method
linktitle: unregister_dictionary method
articleTitle: unregister_dictionary method
second_title: Aspose.Words for Python
description: "Hyphenation.unregister_dictionary method. Unregisters a hyphenation dictionary for the specified language."
type: docs
weight: 50
url: /ar/python-net/aspose.words/hyphenation/unregister_dictionary/
---

## unregister_dictionary(language) {#str}

Unregisters a hyphenation dictionary for the specified language.


This is different from registering Null dictionary. Unregistering a dictionary enables callback for the specified language.


```python
def unregister_dictionary(self, language: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| language | str | A language name, e.g. "en-US". See .NET documentation for "culture name" and RFC 4646 for details. |

### Examples

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

### See Also

* module [aspose.words](../../)
* class [Hyphenation](../)

