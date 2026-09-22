---
title: "Aspose::Words::Loading::LoadOptions::get_MswVersion method"
linktitle: "get_MswVersion"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::LoadOptions::get_MswVersion yöntemi. Belge yükleme işleminin belirli bir MS Word sürümüyle eşleşmesini belirtmeye olanak tanır. Varsayılan değer C++'da Word2019'dur."
type: docs
weight: 11000
url: /tr/cpp/aspose.words.loading/loadoptions/get_mswversion/
---
## LoadOptions::get_MswVersion method


Belge yükleme işleminin belirli bir MS Word sürümüyle eşleşmesini belirtmeye olanak tanır. Varsayılan değer [Word2019](../../../aspose.words.settings/mswordversion/)’dir.

```cpp
Aspose::Words::Settings::MsWordVersion Aspose::Words::Loading::LoadOptions::get_MswVersion() const
```


## Örnekler



Belge yükleme sırasında belirli bir Microsoft Word sürümünün yükleme prosedürünü taklit etmenin nasıl yapılacağını gösterir.
```cpp
// Varsayılan olarak, Aspose.Words belgeleri Microsoft Word 2019 spesifikasyonuna göre yükler.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();

ASSERT_EQ(Aspose::Words::Settings::MsWordVersion::Word2019, loadOptions->get_MswVersion());

// Bu belgenin varsayılan paragraf biçimlendirme stili eksik.
// Bu varsayılan stil, belgeyi Microsoft Word ya da Aspose.Words ile yüklediğimizde yeniden oluşturulacaktır.
loadOptions->set_MswVersion(Aspose::Words::Settings::MsWordVersion::Word2007);
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx", loadOptions);

// Stilin satır aralığı, Microsoft Word 2007 spesifikasyonuna göre yüklendiğinde bu değere sahip olacaktır.
ASSERT_NEAR(12.95, doc->get_Styles()->get_DefaultParagraphFormat()->get_LineSpacing(), 0.01);
```

## Ayrıca Bakınız

* Enum [MsWordVersion](../../../aspose.words.settings/mswordversion/)
* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
