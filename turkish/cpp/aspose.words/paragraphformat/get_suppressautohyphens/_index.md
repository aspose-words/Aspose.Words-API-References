---
title: "Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens metodu"
linktitle: "get_SuppressAutoHyphens"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens yöntemi. Belirtilen paragrafın, belge ayarlarında C++ içinde uygulanan herhangi bir hecelemeden muaf tutulup tutulmayacağını belirtir."
type: docs
weight: 38000
url: /tr/cpp/aspose.words/paragraphformat/get_suppressautohyphens/
---
## ParagraphFormat::get_SuppressAutoHyphens method


Geçerli paragrafın, belge ayarlarında uygulanan herhangi bir hecelemeden muaf olup olmayacağını belirtir.

```cpp
bool Aspose::Words::ParagraphFormat::get_SuppressAutoHyphens()
```


## Örnekler



Bir paragrafta hecelemeyi nasıl bastıracağınızı gösterir.
```cpp
Aspose::Words::Hyphenation::RegisterDictionary(u"de-CH", get_MyDir() + u"hyph_de_CH.dic");

ASSERT_TRUE(Aspose::Words::Hyphenation::IsDictionaryRegistered(u"de-CH"));

// Sözlüğümüzle aynı yerel ayara sahip metin içeren bir belge açın.
// Bu belgeyi sabit sayfa kaydetme formatında kaydettiğimizde, metni hecelemeye sahip olacaktır.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"German text.docx");

// Hecelemeyi devre dışı bırakmak için "SuppressAutoHyphens" özelliğini "true" olarak ayarlayabiliriz
// belirli bir paragraf için, belgenin geri kalanında etkin tutarken.
// Bu özelliğin varsayılan değeri "false"dır,
// bu, varsayılan olarak her paragrafın mevcutsa heceleme kullandığı anlamına gelir.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->set_SuppressAutoHyphens(suppressAutoHyphens);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.SuppressHyphens.pdf");
```

## Ayrıca Bakınız

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
