---
title: "Aspose::Words::DocumentBase::get_WarningCallback yöntemi"
linktitle: "get_WarningCallback"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::DocumentBase::get_WarningCallback yöntemi. C++'ta veri veya biçimlendirme doğruluğu kaybına yol açabilecek bir sorun tespit edildiğinde çeşitli belge işleme prosedürleri sırasında çağrılır."
type: docs
weight: 10000
url: /tr/cpp/aspose.words/documentbase/get_warningcallback/
---
## DocumentBase::get_WarningCallback method


Veri veya biçimlendirme doğruluğunun kaybolmasına neden olabilecek bir sorun tespit edildiğinde çeşitli belge işleme prosedürleri sırasında çağrılır.

```cpp
System::SharedPtr<Aspose::Words::IWarningCallback> Aspose::Words::DocumentBase::get_WarningCallback() const
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

* Interface [IWarningCallback](../../iwarningcallback/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
