---
title: FindReplaceOptions.find_whole_words_only property
linktitle: find_whole_words_only property
articleTitle: find_whole_words_only property
second_title: Aspose.Words for Python
description: "FindReplaceOptions.find_whole_words_only property. True indicates the oldValue must be a standalone word."
type: docs
weight: 50
url: /tr/python-net/aspose.words.replacing/findreplaceoptions/find_whole_words_only/
---

## FindReplaceOptions.find_whole_words_only property

True indicates the oldValue must be a standalone word.


```python
@property
def find_whole_words_only(self) -> bool:
    ...

@find_whole_words_only.setter
def find_whole_words_only(self, value: bool):
    ...

```

### Examples

Shows how to toggle standalone word-only find-and-replace operations.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Jackson will meet you in Jacksonville.')
# Bul ve değiştir sürecini değiştirmek için bir "FindReplaceOptions" nesnesi kullanabiliriz.
options = aw.replacing.FindReplaceOptions()
# "FindWholeWordsOnly" bayrağını "true" olarak ayarlayarak, bulunan metin başka bir kelimenin parçası değilse değiştirin.
# "FindWholeWordsOnly" bayrağını "false" olarak ayarlayarak, çevresine bakılmaksızın tüm metni değiştirin.
options.find_whole_words_only = find_whole_words_only
doc.range.replace(pattern='Jackson', replacement='Louis', options=options)
self.assertEqual('Louis will meet you in Jacksonville.' if find_whole_words_only else 'Louis will meet you in Louisville.', doc.get_text().strip())
```

### See Also

* module [aspose.words.replacing](../../)
* class [FindReplaceOptions](../)

