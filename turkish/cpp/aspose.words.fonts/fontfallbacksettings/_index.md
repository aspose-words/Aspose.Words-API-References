---
title: "Aspose::Words::Fonts::FontFallbackSettings sınıfı"
linktitle: "FontFallbackSettings"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontFallbackSettings sınıfı. Yazı tipi geri dönüş mekanizması ayarlarını belirtir. Daha fazla bilgi için C++'daki belge makalesini ziyaret edin."
type: docs
weight: 5000
url: /tr/cpp/aspose.words.fonts/fontfallbacksettings/
---
## FontFallbackSettings class


Yazı tipi geri dönüş mekanizması ayarlarını belirtir. Daha fazla bilgi için, [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) dokümantasyon makalesini ziyaret edin.

```cpp
class FontFallbackSettings : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [BuildAutomatic](./buildautomatic/)() | Mevcut yazı tiplerini tarayarak geri dönüş ayarlarını otomatik olarak oluşturur. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Load](./load/)(const System::String\&) | XML dosyasından yazı tipi geri dönüş ayarlarını yükler. |
| [Load](./load/)(const System::SharedPtr\<System::IO::Stream\>\&) | XML akışından geri dönüş ayarlarını yükler. |
| [Load](./load/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [LoadMsOfficeFallbackSettings](./loadmsofficefallbacksettings/)() | Microsoft Word geri dönüşünü taklit eden ve Microsoft Office yazı tiplerini kullanan önceden tanımlı geri dönüş ayarlarını yükler. |
| [LoadNotoFallbackSettings](./loadnotofallbacksettings/)() | Google Noto yazı tiplerini kullanan önceden tanımlı geri dönüş ayarlarını yükler. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&) | Mevcut geri dönüş ayarlarını akışa kaydeder. |
| [Save](./save/)(const System::String\&) | Mevcut geri dönüş ayarlarını dosyaya kaydeder. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |

## Örnekler



Geri dönüş yazı tiplerini Unicode karakter kod aralıkları arasında nasıl dağıtacağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);
System::SharedPtr<Aspose::Words::Fonts::FontFallbackSettings> fontFallbackSettings = fontSettings->get_FallbackSettings();

// Yazı tipi ayarlarınızı yalnızca "MyFonts" klasöründen kaynak alacak şekilde yapılandırın.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false);
fontSettings->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

// "BuildAutomatic" yöntemini çağırmak, bir geri dönüş şeması oluşturacaktır ki
// erişilebilir yazı tiplerini mümkün olduğunca çok Unicode karakter kodu arasında dağıtır.
// Bizim durumumuzda, yalnızca "MyFonts" klasöründeki birkaç yazı tipine erişebilir.
fontFallbackSettings->BuildAutomatic();
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettingsCustom.BuildAutomatic.xml");

// Böyle bir dosyadan özel bir ikame şeması da yükleyebiliriz.
// Bu şema, "AllegroOpen" yazı tipini "0000-00ff" Unicode blokları boyunca, "AllegroOpen" yazı tipini "0100-024f" boyunca uygular,
// ve şemadaki diğer yazı tiplerinin kapsamadığı tüm diğer aralıklar için "M+ 2m" yazı tipini kullanır.
fontFallbackSettings->Load(get_MyDir() + u"Custom font fallback settings.xml");

// Bir belge oluşturucu oluşturun ve yazı tipini, kaynaklarımızın hiçbirinde bulunmayan bir yazı tipine ayarlayın.
// Yazı tipimiz mevcut olmadığında, yazı tipimizle yazdığımız karakterler için geri dönüş şemasını devreye sokacaktır.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Name(u"Missing Font");

// Oluşturucuyu kullanarak 0x0021'den 0x052F'e kadar her Unicode karakterini yazdırın,
// özel yazı tipi geri dönüş şemamızda tanımladığımız Unicode bloklarını ayıran açıklayıcı satırlarla.
for (int32_t i = 0x0021; i < 0x0530; i++)
{
    switch (i)
    {
        case 0x0021:
            builder->Writeln(u"\n\n0x0021 - 0x00FF: \nBasic Latin/Latin-1 Supplement Unicode blocks in \"AllegroOpen\" font:");
            break;

        case 0x0100:
            builder->Writeln(u"\n\n0x0100 - 0x024F: \nLatin Extended A/B blocks, mostly in \"AllegroOpen\" font:");
            break;

        case 0x0250:
            builder->Writeln(u"\n\n0x0250 - 0x052F: \nIPA/Greek/Cyrillic blocks in \"M+ 2m\" font:");
            break;

    }

    builder->Write(System::String::Format(u"{0}", System::Convert::ToChar(i)));
}

doc->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettingsCustom.pdf");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
