---
title: "Aspose::Words::IWarningCallback::Warning metodu"
linktitle: "Uyarı"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::IWarningCallback::Warning metodu. Aspose.Words, belge yükleme veya kaydetme sırasında biçim kaybına veya veri bütünlüğüne yol açabilecek bir sorunla karşılaştığında bu metodu C++'da çağırır."
type: docs
weight: 4000
url: /tr/cpp/aspose.words/iwarningcallback/warning/
---
## IWarningCallback::Warning method


Aspose.Words, belge yüklenmesi veya kaydedilmesi sırasında biçimlendirme veya veri bütünlüğü kaybına neden olabilecek bir sorunla karşılaştığında bu yöntemi çağırır.

```cpp
virtual void Aspose::Words::IWarningCallback::Warning(System::SharedPtr<Aspose::Words::WarningInfo> info)=0
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

* Class [WarningInfo](../../warninginfo/)
* Interface [IWarningCallback](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
