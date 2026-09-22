---
title: "Aspose::Words::Font::get_NumberSpacing metodu"
linktitle: "get_NumberSpacing"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Font::get_NumberSpacing metodu. C++'da görüntülenen rakamın boşluk tipini alır veya ayarlar."
type: docs
weight: 30500
url: /tr/cpp/aspose.words/font/get_numberspacing/
---
## Font::get_NumberSpacing method


Görüntülenen sayının boşluk tipini alır veya ayarlar.

```cpp
Aspose::Words::NumSpacing Aspose::Words::Font::get_NumberSpacing()
```


## Örnekler



Sayının boşluk tipinin nasıl ayarlanacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Bu etki yalnızca MS Word'ün daha yeni sürümlerinde desteklenir.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2019);

builder->Write(u"1 ");
builder->Write(u"This is an example");

System::SharedPtr<Aspose::Words::Run> run = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0);
if (run->get_Font()->get_NumberSpacing() == Aspose::Words::NumSpacing::Default)
{
    run->get_Font()->set_NumberSpacing(Aspose::Words::NumSpacing::Proportional);
}

doc->Save(get_ArtifactsDir() + u"Fonts.NumberSpacing.docx");
```

## Ayrıca Bakınız

* Enum [NumSpacing](../../numspacing/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
