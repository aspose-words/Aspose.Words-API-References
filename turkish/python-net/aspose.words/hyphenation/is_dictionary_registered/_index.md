---
title: Hyphenation.is_dictionary_registered method
linktitle: is_dictionary_registered method
articleTitle: is_dictionary_registered method
second_title: Aspose.Words for Python
description: "Hyphenation.is_dictionary_registered method. Returns ``False`` if for the specified language there is no dictionary registered or if registered is Null dictionary, ``True`` otherwise."
type: docs
weight: 30
url: /tr/python-net/aspose.words/hyphenation/is_dictionary_registered/
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

