---
title: Hyphenation.unregister_dictionary method
linktitle: unregister_dictionary method
articleTitle: unregister_dictionary method
second_title: Aspose.Words for Python
description: "Hyphenation.unregister_dictionary method. Unregisters a hyphenation dictionary for the specified language."
type: docs
weight: 50
url: /ru/python-net/aspose.words/hyphenation/unregister_dictionary/
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

