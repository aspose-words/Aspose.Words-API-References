---
title: Hyphenation.is_dictionary_registered method
linktitle: is_dictionary_registered method
articleTitle: is_dictionary_registered method
second_title: Aspose.Words for Python
description: "Hyphenation.is_dictionary_registered method. Returns ``False`` if for the specified language there is no dictionary registered or if registered is Null dictionary, ``True`` otherwise."
type: docs
weight: 30
url: /ar/python-net/aspose.words/hyphenation/is_dictionary_registered/
---

## is_dictionary_registered(language) {#str}

Returns ``False`` if for the specified language there is no dictionary registered or if registered is Null dictionary, ``True`` otherwise.



```python
def is_dictionary_registered(self, language: str):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| language | str |  |

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

