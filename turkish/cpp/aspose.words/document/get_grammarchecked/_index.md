---
title: "Aspose::Words::Document::get_GrammarChecked metodu"
linktitle: "get_GrammarChecked"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::get_GrammarChecked metodu. C++'ta belge dilbilgisi açısından kontrol edildiyse true döndürür."
type: docs
weight: 29000
url: /tr/cpp/aspose.words/document/get_grammarchecked/
---
## Document::get_GrammarChecked method


Belge dilbilgisi için kontrol edilmişse **true** döndürür.

```cpp
bool Aspose::Words::Document::get_GrammarChecked()
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
