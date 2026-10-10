---
title: "Aspose::Words::Fonts::FontFallbackSettings::Save Methode"
linktitle: "Save"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FontFallbackSettings::Save Methode. Speichert die aktuellen Fallback‑Einstellungen in einen Stream in C++."
type: docs
weight: 8000
url: /de/cpp/aspose.words.fonts/fontfallbacksettings/save/
---
## FontFallbackSettings::Save(const System::SharedPtr\<System::IO::Stream\>\&) method


Speichert die aktuellen Fallback‑Einstellungen in einen Stream.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::Save(const System::SharedPtr<System::IO::Stream> &outputStream)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Ausgabestream. |

## Beispiele



Zeigt, wie man Schrift-Fallback-Einstellungen von/einem Stream lädt und speichert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Laden Sie ein XML-Dokument, das einen Satz von Schrift-Fallback-Einstellungen definiert.
{
    auto fontFallbackStream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Font fallback rules.xml", System::IO::FileMode::Open);
    auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
    fontSettings->get_FallbackSettings()->Load(fontFallbackStream);

    doc->set_FontSettings(fontSettings);
}

doc->Save(get_ArtifactsDir() + u"FontSettings.LoadFontFallbackSettingsFromStream.pdf");

// Verwenden Sie einen Stream, um die aktuellen Schrift-Fallback-Einstellungen unseres Dokuments als XML-Dokument zu speichern.
{
    auto fontFallbackStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"FallbackSettings.xml", System::IO::FileMode::Create);
    doc->get_FontSettings()->get_FallbackSettings()->Save(fontFallbackStream);
}
```

## Siehe auch

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FontFallbackSettings::Save(const System::String\&) method


Speichert die aktuellen Fallback‑Einstellungen in eine Datei.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::Save(const System::String &fileName)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | const System::String\& | Ausgabedateiname. |

## Beispiele



Zeigt, wie man Schrift-Fallback-Einstellungen von/einem XML-Dokument im lokalen Dateisystem lädt und speichert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Laden Sie ein XML-Dokument, das einen Satz von Schrift-Fallback-Einstellungen definiert.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_FallbackSettings()->Load(get_MyDir() + u"Font fallback rules.xml");

doc->set_FontSettings(fontSettings);
doc->Save(get_ArtifactsDir() + u"FontSettings.LoadFontFallbackSettingsFromFile.pdf");

// Speichern Sie die aktuellen Schrift-Fallback-Einstellungen unseres Dokuments als XML-Dokument.
doc->get_FontSettings()->get_FallbackSettings()->Save(get_ArtifactsDir() + u"FallbackSettings.xml");
```

## Siehe auch

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FontFallbackSettings::Save(std::basic_ostream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Fonts::FontFallbackSettings::Save(std::basic_ostream<CharType, Traits> &outputStream)
```

## Siehe auch

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
