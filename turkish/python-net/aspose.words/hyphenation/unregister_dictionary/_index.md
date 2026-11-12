---
title: Hyphenation.unregister_dictionary method
linktitle: unregister_dictionary method
articleTitle: unregister_dictionary method
second_title: Aspose.Words for Python
description: "Hyphenation.unregister_dictionary method. Unregisters a hyphenation dictionary for the specified language."
type: docs
weight: 50
url: /tr/python-net/aspose.words/hyphenation/unregister_dictionary/
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
# Bir tireleme sözlüğü, sözlüğün dili için tireleme kurallarını tanımlayan dize listesini içerir.
# Bir belge, bir kelimenin bölünebilir ve bir sonraki satırda devam edebilir olduğu metin satırları içerdiğinde,
# tireleme, sözlüğün dize listesinde o kelimenin alt dizelerini arayacaktır.
# Sözlük bir alt dize içeriyorsa, tireleme kelimeyi iki satıra bölecektir
# alt dizeye göre ve ilk yarısına bir tire ekleyerek.
# Yerel dosya sisteminden bir sözlük dosyasını "de-CH" yerel ayarına kaydedin.
aw.Hyphenation.register_dictionary('de-CH', MY_DIR + 'hyph_de_CH.dic')
self.assertTrue(aw.Hyphenation.is_dictionary_registered('de-CH'))
# Sözlüğümüzle eşleşen bir yerel ayara sahip metin içeren bir belgeyi açın,
# ve sabit sayfa kaydetme formatına kaydedin. O belgedeki metin tirelenecektir.
doc = aw.Document(MY_DIR + 'German text.docx')
self.assertTrue(all((node for node in doc.first_section.body.first_paragraph.runs if node.as_run().font.locale_id == 2055)))
doc.save(ARTIFACTS_DIR + 'Hyphenation.dictionary.registered.pdf')
# Sözlüğün kaydını iptal ettikten sonra belgeyi yeniden yükleyin,
# ve başka bir PDF'ye kaydedin; bu PDF'de tirelenmiş metin olmayacaktır.
aw.Hyphenation.unregister_dictionary('de-CH')
self.assertFalse(aw.Hyphenation.is_dictionary_registered('de-CH'))
doc = aw.Document(MY_DIR + 'German text.docx')
doc.save(ARTIFACTS_DIR + 'Hyphenation.dictionary.unregistered.pdf')
```

### See Also

* module [aspose.words](../../)
* class [Hyphenation](../)

