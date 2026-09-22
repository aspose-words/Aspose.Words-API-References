---
title: "Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly metodu"
linktitle: "get_FindWholeWordsOnly"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly metodu. True, eski değerin C++'da bağımsız bir kelime olması gerektiğini gösterir."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.replacing/findreplaceoptions/get_findwholewordsonly/
---
## FindReplaceOptions::get_FindWholeWordsOnly method


True, oldValue'nun bağımsız bir kelime olması gerektiğini gösterir.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_FindWholeWordsOnly() const
```


## Örnekler



Yalnızca bağımsız kelimeler için bul-ve-değiştir işlemlerini nasıl değiştireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Jackson will meet you in Jacksonville.");

// "FindReplaceOptions" nesnesini kullanarak bul-ve-değiştir sürecini değiştirebiliriz.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// "FindWholeWordsOnly" bayrağını "true" olarak ayarlayarak bulunan metin başka bir kelimenin parçası değilse değiştirirsiniz.
// "FindWholeWordsOnly" bayrağını "false" olarak ayarlayarak çevresine bakılmaksızın tüm metni değiştirirsiniz.
options->set_FindWholeWordsOnly(findWholeWordsOnly);

doc->get_Range()->Replace(u"Jackson", u"Louis", options);

ASSERT_EQ(findWholeWordsOnly ? System::String(u"Louis will meet you in Jacksonville.") : System::String(u"Louis will meet you in Louisville."), doc->GetText().Trim());
```

## Ayrıca Bakınız

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
