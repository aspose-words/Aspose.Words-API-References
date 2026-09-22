---
title: "Aspose::Words::IWarningCallback arayüzü"
linktitle: "IWarningCallback"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::IWarningCallback arayüzü. Belgelerin yüklenmesi veya kaydedilmesi sırasında oluşabilecek bütünlük kaybı uyarılarını yakalamak için kendi özel yönteminizi çağırmak istiyorsanız bu arayüzü uygulayın."
type: docs
weight: 80000
url: /tr/cpp/aspose.words/iwarningcallback/
---
## IWarningCallback interface


Bu arayüzü, belge yükleme veya kaydetme sırasında ortaya çıkabilecek doğruluk kaybı uyarılarını yakalamak için kendi özel yönteminizi çağırmak istediğinizde uygulayın.

```cpp
class IWarningCallback : public virtual System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
| virtual [Warning](./warning/)(System::SharedPtr\<Aspose::Words::WarningInfo\>) | Aspose.Words, belge yüklenmesi veya kaydedilmesi sırasında biçimlendirme veya veri bütünlüğü kaybına neden olabilecek bir sorunla karşılaştığında bu yöntemi çağırır. |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
