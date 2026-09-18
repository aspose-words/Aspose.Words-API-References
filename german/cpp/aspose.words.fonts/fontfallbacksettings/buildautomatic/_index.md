---
title: "Aspose::Words::Fonts::FontFallbackSettings::BuildAutomatic Methode"
linktitle: "BuildAutomatic"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FontFallbackSettings::BuildAutomatic Methode. Erstellt automatisch die Fallback‑Einstellungen, indem verfügbare Schriften in C++ gescannt werden."
type: docs
weight: 2000
url: /de/cpp/aspose.words.fonts/fontfallbacksettings/buildautomatic/
---
## FontFallbackSettings::BuildAutomatic method


Erstellt die Fallback‑Einstellungen automatisch, indem verfügbare Schriftarten gescannt werden.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::BuildAutomatic()
```


## Beispiele



Zeigt, wie Fallback‑Schriftarten über Unicode‑Zeichencodierungsbereiche verteilt werden können.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);
System::SharedPtr<Aspose::Words::Fonts::FontFallbackSettings> fontFallbackSettings = fontSettings->get_FallbackSettings();

// Konfigurieren Sie unsere Schriftarteinstellungen, um Schriftarten ausschließlich aus dem Ordner "MyFonts" zu beziehen.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false);
fontSettings->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

// Der Aufruf der Methode "BuildAutomatic" erzeugt ein Fallback‑Schema, das
// verfügbare Schriftarten über so viele Unicode‑Zeichencodes wie möglich verteilt.
// In unserem Fall hat es nur Zugriff auf die wenigen Schriftarten im Ordner "MyFonts".
fontFallbackSettings->BuildAutomatic();
fontFallbackSettings->Save(get_ArtifactsDir() + u"FontSettings.FallbackSettingsCustom.BuildAutomatic.xml");

// Wir können auch ein benutzerdefiniertes Ersetzungsschema aus einer Datei wie dieser laden.
// Dieses Schema wendet die Schriftart "AllegroOpen" auf die Unicode‑Blöcke "0000-00ff" an, die Schriftart "AllegroOpen" auf "0100-024f",
// und die Schriftart "M+ 2m" in allen anderen Bereichen, die von anderen Schriftarten im Schema nicht abgedeckt werden.
fontFallbackSettings->Load(get_MyDir() + u"Custom font fallback settings.xml");

// Erstellen Sie einen DocumentBuilder und setzen Sie dessen Schriftart auf eine, die in keiner unserer Quellen vorhanden ist.
// Unsere Schriftarteinstellungen rufen das Fallback‑Schema für Zeichen auf, die wir mit der nicht verfügbaren Schriftart eingeben.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->get_Font()->set_Name(u"Missing Font");

// Verwenden Sie den Builder, um jedes Unicode‑Zeichen von 0x0021 bis 0x052F auszugeben,
// mit beschreibenden Zeilen, die die Unicode‑Blöcke trennen, die wir in unserem benutzerdefinierten Schriftart‑Fallback‑Schema definiert haben.
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

## Siehe auch

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
