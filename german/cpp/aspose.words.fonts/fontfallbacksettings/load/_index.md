---
title: "Aspose::Words::Fonts::FontFallbackSettings::Load-Methode"
linktitle: "Laden"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FontFallbackSettings::Load-Methode. Lädt Fallback-Einstellungen aus einem XML-Stream in C++."
type: docs
weight: 5000
url: /de/cpp/aspose.words.fonts/fontfallbacksettings/load/
---
## FontFallbackSettings::Load(const System::SharedPtr\<System::IO::Stream\>\&) method


Lädt die Fallback‑Einstellungen aus einem XML‑Stream.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::Load(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Datenstrom | const System::SharedPtr\<System::IO::Stream\>\& | Eingabestream. |

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
## FontFallbackSettings::Load(const System::String\&) method


Lädt die Schriftart‑Fallback‑Einstellungen aus einer XML‑Datei.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::Load(const System::String &fileName)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | const System::String\& | Eingabedateiname. |

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
## FontFallbackSettings::Load(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Fonts::FontFallbackSettings::Load(std::basic_istream<CharType, Traits> &stream)
```

## Siehe auch

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
