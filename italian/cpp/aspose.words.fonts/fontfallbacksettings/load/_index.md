---
title: "Metodo Aspose::Words::Fonts::FontFallbackSettings::Load"
linktitle: "Carica"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Fonts::FontFallbackSettings::Load. Carica le impostazioni di fallback da un flusso XML in C++."
type: docs
weight: 5000
url: /it/cpp/aspose.words.fonts/fontfallbacksettings/load/
---
## FontFallbackSettings::Load(const System::SharedPtr\<System::IO::Stream\>\&) method


Carica le impostazioni di fallback da uno stream XML.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::Load(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| flusso | const System::SharedPtr\<System::IO::Stream\>\& | Flusso di input. |

## Esempi



Mostra come caricare e salvare le impostazioni di fallback dei caratteri da/a un flusso.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Carica un documento XML che definisce un insieme di impostazioni di fallback dei caratteri.
{
    auto fontFallbackStream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Font fallback rules.xml", System::IO::FileMode::Open);
    auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
    fontSettings->get_FallbackSettings()->Load(fontFallbackStream);

    doc->set_FontSettings(fontSettings);
}

doc->Save(get_ArtifactsDir() + u"FontSettings.LoadFontFallbackSettingsFromStream.pdf");

// Utilizza un flusso per salvare le attuali impostazioni di fallback dei caratteri del nostro documento come documento XML.
{
    auto fontFallbackStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"FallbackSettings.xml", System::IO::FileMode::Create);
    doc->get_FontSettings()->get_FallbackSettings()->Save(fontFallbackStream);
}
```

## Vedi anche

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FontFallbackSettings::Load(const System::String\&) method


Carica le impostazioni di fallback dei font da un file XML.

```cpp
void Aspose::Words::Fonts::FontFallbackSettings::Load(const System::String &fileName)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| nomeFile | const System::String\& | Nome file di input. |

## Esempi



Mostra come caricare e salvare le impostazioni di fallback dei caratteri da/a un documento XML nel file system locale.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Carica un documento XML che definisce un insieme di impostazioni di fallback dei caratteri.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_FallbackSettings()->Load(get_MyDir() + u"Font fallback rules.xml");

doc->set_FontSettings(fontSettings);
doc->Save(get_ArtifactsDir() + u"FontSettings.LoadFontFallbackSettingsFromFile.pdf");

// Salva le attuali impostazioni di fallback dei caratteri del nostro documento come documento XML.
doc->get_FontSettings()->get_FallbackSettings()->Save(get_ArtifactsDir() + u"FallbackSettings.xml");
```

## Vedi anche

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
## FontFallbackSettings::Load(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Fonts::FontFallbackSettings::Load(std::basic_istream<CharType, Traits> &stream)
```

## Vedi anche

* Class [FontFallbackSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
