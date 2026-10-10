---
title: "Aspose::Words::WarningInfo sınıfı"
linktitle: "WarningInfo"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::WarningInfo sınıfı. Aspose.Words tarafından belge yükleme veya kaydetme sırasında verilen bir uyarı hakkında bilgi içerir. Daha fazla bilgi edinmek için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 74000
url: /tr/cpp/aspose.words/warninginfo/
---
## WarningInfo class


Aspose.Words'in belge yükleme veya kaydetme sırasında verdiği bir uyarı hakkında bilgi içerir. Daha fazla bilgi edinmek için, [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/) belgeler makalesini ziyaret edin.

```cpp
class WarningInfo : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_Description](./get_description/)() const | Uyarının açıklamasını döndürür. |
| [get_Source](./get_source/)() const | Uyarının kaynağını döndürür. |
| [get_WarningType](./get_warningtype/)() const | Uyarının türünü döndürür. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Açıklamalar


Bu sınıfın örneklerini siz oluşturmazsınız. Bu sınıfın nesneleri Aspose.Words tarafından oluşturulur ve [Warning()](../iwarningcallback/warning/) metoduna geçirilir.

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
