---
title: Hyphenation.is_dictionary_registered method
linktitle: is_dictionary_registered method
articleTitle: is_dictionary_registered method
second_title: Aspose.Words for Python
description: "Hyphenation.is_dictionary_registered method. Returns ``False`` if for the specified language there is no dictionary registered or if registered is Null dictionary, ``True`` otherwise."
type: docs
weight: 30
url: /ru/python-net/aspose.words/hyphenation/is_dictionary_registered/
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
# Словарь переносов содержит список строк, определяющих правила переноса для языка словаря.
# Когда документ содержит строки текста, в которых слово может быть разбито и продолжено на следующей строке,
# перенос будет просматривать список строк словаря в поисках подстрок этого слова.
# Если словарь содержит подстроку, то перенос разделит слово на две строки
# по подстроке и добавит дефис к первой части.
# Зарегистрируйте файл словаря из локальной файловой системы для локали "de-CH".
aw.Hyphenation.register_dictionary('de-CH', MY_DIR + 'hyph_de_CH.dic')
self.assertTrue(aw.Hyphenation.is_dictionary_registered('de-CH'))
# Откройте документ, содержащий текст с локалью, соответствующей нашей локали словаря,
# и сохраните его в формат фиксированных страниц. Текст в этом документе будет перенесён.
doc = aw.Document(MY_DIR + 'German text.docx')
self.assertTrue(all((node for node in doc.first_section.body.first_paragraph.runs if node.as_run().font.locale_id == 2055)))
doc.save(ARTIFACTS_DIR + 'Hyphenation.dictionary.registered.pdf')
# Перезагрузите документ после отмены регистрации словаря,
# и сохраните его в другой PDF, в котором не будет перенесённого текста.
aw.Hyphenation.unregister_dictionary('de-CH')
self.assertFalse(aw.Hyphenation.is_dictionary_registered('de-CH'))
doc = aw.Document(MY_DIR + 'German text.docx')
doc.save(ARTIFACTS_DIR + 'Hyphenation.dictionary.unregistered.pdf')
```

### See Also

* module [aspose.words](../../)
* class [Hyphenation](../)

