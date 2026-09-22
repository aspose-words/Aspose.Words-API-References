---
title: "Aspose::Words::Document::get_SpellingChecked yöntemi"
linktitle: "get_SpellingChecked"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::get_SpellingChecked yöntemi. Belge C++'ta imla denetiminden geçirilmişse true döndürür."
type: docs
weight: 52000
url: /tr/cpp/aspose.words/document/get_spellingchecked/
---
## Document::get_SpellingChecked method


Belge yazım denetiminden geçirilmişse **true** döndürür.

```cpp
bool Aspose::Words::Document::get_SpellingChecked()
```


## Örnekler



İmla veya dilbilgisi doğrulamasını nasıl ayarlayacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// İmla hataları içeren dize.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->Add(System::MakeObject<Aspose::Words::Run>(doc, u"The speeling in this documentz is all broked."));

// Özellikleri false olarak ayarlarsak imla/dilbilgisi denetimi başlar.
// Microsoft Word'de Tüm hataları İnceleme -> İmla ve Dilbilgisi üzerinden görebiliriz.
// Microsoft Word'ün DOC ve RTF belge formatı için dilbilgisi/imla denetimini otomatik olarak başlatmadığını unutmayın.
doc->set_SpellingChecked(checkSpellingGrammar);
doc->set_GrammarChecked(checkSpellingGrammar);

doc->Save(get_ArtifactsDir() + u"Document.SpellingOrGrammar.docx");
```

## Ayrıca Bakınız

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
