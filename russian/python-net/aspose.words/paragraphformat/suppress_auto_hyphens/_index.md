---
title: ParagraphFormat.suppress_auto_hyphens property
linktitle: suppress_auto_hyphens property
articleTitle: suppress_auto_hyphens property
second_title: Aspose.Words for Python
description: "ParagraphFormat.suppress_auto_hyphens property. Specifies whether the current paragraph should be exempted from any hyphenation which is applied in the document settings."
type: docs
weight: 380
url: /ru/python-net/aspose.words/paragraphformat/suppress_auto_hyphens/
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
# Откройте документ, содержащий текст с локалью, соответствующей нашей словарной базе.
# При сохранении этого документа в формат фиксированных страниц его текст будет перенесён с дефисами.
doc = aw.Document(file_name=MY_DIR + 'German text.docx')
# Мы можем установить свойство \"SuppressAutoHyphens\" в \"true\", чтобы отключить переносы с дефисами
# для конкретного абзаца, оставив его включённым для остальной части документа.
# Значение по умолчанию для этого свойства — \"false\",
# что означает, что каждый абзац по умолчанию использует переносы, если они доступны.
doc.first_section.body.first_paragraph.paragraph_format.suppress_auto_hyphens = suppress_auto_hyphens
doc.save(file_name=ARTIFACTS_DIR + 'ParagraphFormat.SuppressHyphens.pdf')
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

