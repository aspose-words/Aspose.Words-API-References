---
title: "classe Aspose::Words::Fonts::FontFallbackSettings"
linktitle: "FontFallbackSettings"
second_title: "Riferimento API Aspose.Words per C++"
description: "classe Aspose::Words::Fonts::FontFallbackSettings. Specifica le impostazioni del meccanismo di fallback dei font. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.fonts/fontfallbacksettings/
---
## FontFallbackSettings class


Specifica le impostazioni del meccanismo di fallback dei caratteri. Per saperne di più, visita l'articolo di documentazione [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FontFallbackSettings : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [BuildAutomatic](./buildautomatic/)() | Crea automaticamente le impostazioni di fallback esaminando i font disponibili. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Load](./load/)(const System::String\&) | Carica le impostazioni di fallback dei font da un file XML. |
| [Load](./load/)(const System::SharedPtr\<System::IO::Stream\>\&) | Carica le impostazioni di fallback da uno stream XML. |
| [Load](./load/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [LoadMsOfficeFallbackSettings](./loadmsofficefallbacksettings/)() | Carica le impostazioni di fallback predefinite che imitano il fallback di Microsoft Word e utilizzano i font di Microsoft Office. |
| [LoadNotoFallbackSettings](./loadnotofallbacksettings/)() | Carica le impostazioni di fallback predefinite che utilizzano i font Google Noto. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&) | Salva le impostazioni di fallback correnti su uno stream. |
| [Save](./save/)(const System::String\&) | Salva le impostazioni di fallback correnti su un file. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| static [Type](./type/)() |  |

## Esempi



Mostra come distribuire i font di fallback attraverso gli intervalli di codici dei caratteri Unicode.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);
System::SharedPtr<Aspose::Words::Fonts::FontFallbackSettings> fontFallbackSettings = fontSettings->get_FallbackSettings();

// Configura le nostre impostazioni dei font per prelevare i font solo dalla cartella "MyFonts".
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false);
fontSettings->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

// Chiamare il metodo "BuildAutomatic" genererà uno schema di fallback che
// distribuisce i font disponibili su quanti più codici di caratteri Unicode possibile.
// Nel nostro caso, ha accesso solo a pochi font all'interno della cartella "MyFonts".
fontFallbackSettings->BuildAutomatic();
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettingsCustom.BuildAutomatic.xml");

// Possiamo anche caricare uno schema di sostituzione personalizzato da un file come questo.
// Questo schema applica il font "AllegroOpen" ai blocchi Unicode "0000-00ff", il font "AllegroOpen" a "0100-024f",
// e il font "M+ 2m" in tutti gli altri intervalli che gli altri font nello schema non coprono.
fontFallbackSettings->Load(get_MyDir() + u"Custom font fallback settings.xml");

// Crea un document builder e imposta il suo font su uno che non esiste in nessuna delle nostre fonti.
// Le nostre impostazioni dei font invocheranno lo schema di fallback per i caratteri che digitiamo usando il font non disponibile.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Name(u"Missing Font");

// Usa il builder per stampare ogni carattere Unicode da 0x0021 a 0x052F,
// con linee descrittive che dividono i blocchi Unicode che abbiamo definito nel nostro schema di fallback dei font personalizzato.
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

## Vedi anche

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
