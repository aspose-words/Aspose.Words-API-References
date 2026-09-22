---
title: "Aspose::Words::Underline enum"
linktitle: "Alt çizgi"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Underline enum. C++'da bir fonta uygulanan alt çizgi tipini belirtir."
type: docs
weight: 126000
url: /tr/cpp/aspose.words/underline/
---
## Underline enum


Bir yazı tipine uygulanan alt çizgi tipini gösterir.

```cpp
enum class Underline
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| None | 0 |  |
| Tek | 1 |  |
| Words | 2 |  |
| Çift | 3 |  |
| Noktalı | 4 |  |
| Kalın | 6 |  |
| Kesik | 7 |  |
| DashLong | 39 |  |
| DotDash | 9 |  |
| DotDotDash | 10 |  |
| Dalgalı | 11 |  |
| DottedHeavy | 20 |  |
| DashHeavy | 23 |  |
| DashLongHeavy | 55 |  |
| DotDashHeavy | 25 |  |
| DotDotDashHeavy | 26 |  |
| WavyHeavy | 27 |  |
| WavyDouble | 43 |  |


## Örnekler



Bir hiperlink alanının nasıl ekleneceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"For more information, please visit the ");

// Bir hiperlink ekleyin ve özel biçimlendirme ile vurgulayın.
// Hiperlink, URL'de belirtilen konuma götürecek tıklanabilir bir metin parçası olacaktır.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
builder->InsertHyperlink(u"Google website", u"https://www.google.com", false);
builder->get_Font()->ClearFormatting();
builder->Writeln(u".");

// Microsoft Word'de metindeki bağlantıya Ctrl + sol tıklama, yeni bir web tarayıcı penceresi aracılığıyla URL'ye götürür.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlink.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
