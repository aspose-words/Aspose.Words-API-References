---
title: "Aspose::Words::WarningType enum"
linktitle: "WarningType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::WarningType enum. Aspose.Words tarafından C++'ta belge yükleme veya kaydetme sırasında verilen bir uyarının türünü belirtir."
type: docs
weight: 129000
url: /tr/cpp/aspose.words/warningtype/
---
## WarningType enum


Belge yüklenirken veya kaydedilirken Aspose.Words tarafından verilen uyarının türünü belirtir.

```cpp
enum class WarningType
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| DataLossCategory | 255 | Yükleme sonrasında belge ağacından veya kaydetme sonrasında oluşturulan belgeden bazı metin/karakter/görsel veya diğer veriler eksik olacaktır. |
| DataLoss | 1 | Genel veri kaybı, belirli bir kod yok. |
| MajorFormattingLossCategory | 65280 | Ortaya çıkan belge veya içindeki belirli bir konum, orijinal belgeye kıyasla önemli ölçüde farklı görünebilir. |
| MajorFormattingLoss | 256 | Genel büyük biçimlendirme kaybı, belirli bir kod yok. |
| MinorFormattingLossCategory | 16711680 | Ortaya çıkan belge veya içindeki belirli bir konum, orijinal belgeye kıyasla biraz farklı görünebilir. |
| MinorFormattingLoss | 65536 | Genel küçük biçimlendirme kaybı, belirli bir kod yok. |
| FontSubstitution | 131072 | [Font](../font/) değiştirildi. |
| FontEmbedding | 262144 | Belge kaydedilirken gömülü yazı tipi bilgilerinin kaybı. |
| UnexpectedContentCategory | 251658240 | Kaynak belgedeki bazı içerikler tanınamadı (yani desteklenmiyor), bu durum sorunlara yol açabilir veya veri/biçimlendirme kaybına neden olabilir. |
| UnexpectedContent | 16777216 | Genel beklenmeyen içerik, belirli bir kod yok. |
| İpucu | 268435456 | Potansiyel bir sorunu bildirir veya bir iyileştirme önerir. |


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
