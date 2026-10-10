---
title: "Aspose::Words::Layout::LayoutOptions::get_KeepOriginalFontMetrics yöntemi"
linktitle: "get_KeepOriginalFontMetrics"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Layout::LayoutOptions::get_KeepOriginalFontMetrics yöntemi. Yazı tipi ikamesinden sonra orijinal yazı tipi ölçümlerinin kullanılıp kullanılmayacağını gösteren bir göstergesi alır veya ayarlar. Varsayılan değer C++'da doğrudur."
type: docs
weight: 6500
url: /tr/cpp/aspose.words.layout/layoutoptions/get_keeporiginalfontmetrics/
---
## LayoutOptions::get_KeepOriginalFontMetrics method


Yazı tipi ikamesinden sonra orijinal yazı tipi ölçümlerinin kullanılıp kullanılmayacağını gösteren değeri alır veya ayarlar. Varsayılan **true**.

```cpp
bool Aspose::Words::Layout::LayoutOptions::get_KeepOriginalFontMetrics() const
```


## Örnekler



Mevcut yazı tipi kaynaklarından eksik bir yazı tipi için en yakın eşleşmeyi bulmak üzere özelliği nasıl ayarlayacağınızı gösterir.
```cpp
// Yazı tipi kaynaklarımızın hiçbirinde bulunmayan bir yazı tipiyle biçimlendirilmiş metin içeren bir belge açın.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.docx");

// Yazı tipi ikame uyarılarını işlemek için bir geri çağırma atayın.
auto warningCollector = System::MakeObject<Aspose::Words::WarningInfoCollection>();
doc->set_WarningCallback(warningCollector);

// Varsayılan bir yazı tipi adı ayarlayın ve yazı tipi ikamesini etkinleştirin.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(true);

// Yazı tipi ikamesinden sonra orijinal yazı tipi ölçümleri kullanılmalıdır.
doc->get_LayoutOptions()->set_KeepOriginalFontMetrics(true);

// Eksik bir yazı tipiyle bir belgeyi kaydedersek yazı tipi ikamesi uyarısı alacağız.
doc->set_FontSettings(fontSettings);
doc->Save(get_ArtifactsDir() + u"FontSettings.EnableFontSubstitution.pdf");

for (auto&& info : warningCollector)
{
    if (info->get_WarningType() == Aspose::Words::WarningType::FontSubstitution)
    {
        std::cout << info->get_Description() << std::endl;
    }
}
```

## Ayrıca Bakınız

* Class [LayoutOptions](../)
* Namespace [Aspose::Words::Layout](../../)
* Library [Aspose.Words for C++](../../../)
