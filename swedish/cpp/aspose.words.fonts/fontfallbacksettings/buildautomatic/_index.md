---
title: "Aspose::Words::Fonts::FontFallbackSettings::BuildAutomatic method"
linktitle: "BuildAutomatic"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::FontFallbackSettings::BuildAutomatic method. Automatiskt bygger fallback‑inställningarna genom att skanna tillgängliga teckensnitt i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.fonts/fontfallbacksettings/buildautomatic/
---
## FontFallbackSettings::BuildAutomatic method


Bygger automatiskt fallback‑inställningarna genom att skanna tillgängliga typsnitt.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::BuildAutomatic()
```


## Exempel



Visar hur man distribuerar fallback‑typsnitt över Unicode‑teckenkodintervall.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);
System::SharedPtr<Aspose::Words::Fonts::FontFallbackSettings> fontFallbackSettings = fontSettings->get_FallbackSettings();

// Konfigurera våra typsnittsinställningar så att de hämtar typsnitt endast från mappen \"MyFonts\".
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false);
fontSettings->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

// Att anropa metoden \"BuildAutomatic\" kommer att generera ett fallback‑schema som
// distribuerar tillgängliga typsnitt över så många Unicode‑teckenkoder som möjligt.
// I vårt fall har den bara åtkomst till ett fåtal typsnitt i mappen \"MyFonts\".
fontFallbackSettings->BuildAutomatic();
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettingsCustom.BuildAutomatic.xml");

// Vi kan också läsa in ett anpassat substitutionsschema från en fil som denna.
// Detta schema tillämpar teckensnittet "AllegroOpen" över Unicode‑blocken "0000-00ff", teckensnittet "AllegroOpen" över "0100-024f",
// och teckensnittet "M+ 2m" i alla andra intervall som andra teckensnitt i schemat inte täcker.
fontFallbackSettings->Load(get_MyDir() + u"Custom font fallback settings.xml");

// Skapa en dokumentbyggare och sätt dess teckensnitt till ett som inte finns i någon av våra källor.
// Våra teckensnittinställningar kommer att anropa reservschemat för tecken som vi skriver med det otillgängliga teckensnittet.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Name(u"Missing Font");

// Använd byggaren för att skriva ut varje Unicode‑tecken från 0x0021 till 0x052F,
// med beskrivande rader som delar upp Unicode‑blocken som vi definierade i vårt anpassade teckensnitt‑reservschema.
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

## Se även

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
