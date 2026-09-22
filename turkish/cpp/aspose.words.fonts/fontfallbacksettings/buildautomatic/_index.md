---
title: "Aspose::Words::Fonts::FontFallbackSettings::BuildAutomatic method"
linktitle: "BuildAutomatic"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontFallbackSettings::BuildAutomatic method. Kullanılabilir fontları tarayarak yedek ayarları otomatik olarak oluşturur C++'da."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fonts/fontfallbacksettings/buildautomatic/
---
## FontFallbackSettings::BuildAutomatic method


Mevcut yazı tiplerini tarayarak geri dönüş ayarlarını otomatik olarak oluşturur.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::BuildAutomatic()
```


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

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
